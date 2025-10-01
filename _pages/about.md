---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

  I am Zhiyuan Liang, who just graduated from <a href="https://www.ustc.edu.cn/">USTC</a>. 

  I'm extraodinarily fortunate to work as an intern at <a href="https://ai.comp.nus.edu.sg/"> NUS HPC AI Lab</a> for a fruitful year, under the supervision of Prof.<a href="https://www.comp.nus.edu.sg/~youy/">Yang You</a>, and advised by Dr. <a href="https://kaiwang960112.github.io/">Kai Wang</a> and Dr. <a href="https://wangbo-zhao.github.io/">Wangbo Zhao</a>.
  Before that, I worked as an intern at UNC Chapel Hill under the supervision of Prof <a href="https://www.huaxiuyao.io/"> Huaxiu Yao </a>. 
  Before that, I was fortunate to start my journey of research at the <a href="https://data-science.ustc.edu.cn">Lab of Data Science</a> supervised by Prof.<a href="https://xiangwang1223.github.io/">Xiang Wang</a> and Prof.<a href="https://hexiangnan.github.io/">Xiangnan He</a>.

  My research interest lies in **Parameter Generation** and **Multimodal Understanding**, obtaining higher level of intelligence from the angle of weight space learning, and exploring the unified learning paradigm across various modalities.
  I'm actively seeking for PhD opportuninties.



# 🔥 News
- *2025.09*: 🥳 DnD and other 2 papers accpeted to NeurIPS 2025! Thanks all collaborators! 
- *2025.08*: 🐧 I join Tencent as an intern in multimodal understanding and parameter generation!
- *2025.07*: 🌟 Our new work, Drag-and-Drop LLMs, customizes LLMs in seconds without tuning! Check our [paper](https://arxiv.org/abs/2506.16406) and [code](https://github.com/jerryliang24/Drag-and-Drop-LLMs)! 
- *2025.06*: 🎉 I received bachelor degree from USTC! 

# 📝 Selected Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NeurIPS 2025</div><img src='https://github.com/jerryliang24/jerryliang24.github.io/blob/main/DnD/static/images/pipeline.jpg?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**Drag-and-Drop LLMs: Zero-Shot Prompt-to-Weights**](https://arxiv.org/abs/2506.16406) <img src='https://img.shields.io/github/stars/jerryliang24/Drag-and-Drop-LLMs.svg?style=social&label=Star' alt="sym" height="100%">

**Zhiyuan Liang†**, 
Dongwen Tang, 
Yuhao Zhou, 
Xuanlei Zhao, 
Mingjia Shi，

Wangbo Zhao, 
Zekai Li, 
Peihao Wang, 
Konstantin Schürholt, 
Damian Borth

Michael M. Bronstein,
Yang You, 
Zhangyang Wang†, 
Kai Wang† (**† project lead**)

We introduce Drag-and-Drop LLMs (DnD) 🥳, a prompt-conditioned parameter generator that enables training-free adaptation of large language models. It features: 
  - Producing task-specific LoRA matrices from **unlabeled task prompts**.
  - Generating weights for novel tasks in seconds, achieving up to **12,000×** lower overhead.
  - Outperforming the strongest training LoRAs by up to **30%** on various zero-shot benchmarks.

<div style="display: inline">
    <a href="https://arxiv.org/abs/2506.16406"> <strong>[paper]</strong></a>
    <a href="https://github.com/jerryliang24/Drag-and-Drop-LLMs"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> Modern Parameter-Efficient Fine-Tuning (PEFT) methods such as low-rank adaptation (LoRA) reduce the cost of customizing large language models (LLMs), yet still require a separate optimization run for every downstream dataset. We introduce **Drag-and-Drop LLMs (DnD)**, a prompt-conditioned parameter generator that eliminates per-task training by mapping a handful of unlabeled task prompts directly to LoRA weight updates. A lightweight text encoder distills each prompt batch into  condition embeddings, which are then transformed by a cascaded hyper-convolutional decoder into the full set of LoRA matrices. Once trained in a diverse collection of
prompt-checkpoint pairs, DnD produces task-specific parameters in seconds, yielding i) up to
**12,000$\times$** lower overhead than full fine-tuning, ii) average gains up to **30\%** in performance over the strongest training LoRAs on unseen common-sense reasoning, math, coding, and multimodal benchmarks, and iii) robust cross-domain generalization despite never seeing the target data or labels. Our results demonstrate that prompt-conditioned parameter generation is a viable alternative to gradient-based adaptation for rapidly specializing LLMs.
Our project is available at https://jerryliang24.github.io/DnD. </p>
    </div>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='https://github.com/NUS-HPC-AI-Lab/DyVM/blob/master/Asset/pipeline.png?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**Dynamic Vision Mamba**](https://arxiv.org/abs/2504.04787) <img src='https://img.shields.io/github/stars/NUS-HPC-AI-Lab/DyVM.svg?style=social&label=Star' alt="sym" height="100%">


Mengxuan Wu\*, Zekai Li\*†, **Zhiyuan Liang\***,  Moyang Li,  Xuanlei Zhao,  Samir Khaki,  Zheng Zhu,  Xiaojiang Peng,  Konstantinos N. Plataniotis,  Kai Wang‡,  Wangbo Zhao‡,  Yang You (**\* equal contribution,  † project lead,  ‡ corresponding author**)

We introduce **Dynamic Vision Mamba (DyVM)** 🚀, a dynamic inference framework for Mamba-based vision models that significantly reduces computation while preserving performance. It features:  
  - **Token-level efficiency**: Customized token pruning with sequence rearrangement to maintain consistency between training and inference.  
  - **Block-level adaptivity**: Dynamic selection of SSM blocks per image, reducing redundancy based on input complexity.  
  - **Strong efficiency-accuracy trade-off**: Achieves **35.2% FLOPs reduction** with only **1.7% accuracy drop** on Vim-S, and generalizes across architectures and vision tasks.
<div style="display: inline">
    <a href="https://arxiv.org/abs/2504.04787"> <strong>[paper]</strong></a>
    <a href="https://github.com/NUS-HPC-AI-Lab/DyVM"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> Mamba-based vision models have gained extensive atten
tion as a result of being computationally more efficient
 than attention-based models. However, spatial redundancy
 still exists in these models, represented by token and block
 redundancy. For token redundancy, we analytically find
 that early token pruning methods will result in inconsis
tency between training and inference or introduce extra
 computation for inference. Therefore, we customize to
ken pruning to fit the Mamba structure by rearranging the
 pruned sequence before feeding it into the next Mamba
 block. For block redundancy, we allow each image to se
lect SSM blocks dynamically based on an empirical ob
servation that the inference speed of Mamba-based vision
 models is largely affected by the number of SSM blocks.
 Our proposed method, Dynamic Vision Mamba (DyVM),
 effectively reduces FLOPs with minor performance drops.
 We achieve a reduction of 35.2% FLOPs with only a loss
 of accuracy of 1.7% on Vim-S. It also generalizes well
 across different Mamba vision model architectures and dif
ferent vision tasks. Our code will be made public at
 https://github.com/NUS-HPC-AI-Lab/DyVM. </p>
    </div>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NeurIPS 2025</div><img src='https://github.com/jerryliang24/jerryliang24.github.io/blob/main/assets/figures/HASTE.jpg?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**REPA Works Until It Doesn't: Early-Stopped, Holistic Alignment Supercharges Diffusion Training**](https://arxiv.org/abs/2505.16792) <img src='https://img.shields.io/github/stars/NUS-HPC-AI-Lab/HASTE.svg?style=social&label=Star' alt="sym" height="100%">

Ziqiao Wang∗, Wangbo Zhao∗, Yuhao Zhou, Zekai Li, **Zhiyuan Liang**, Mingjia Shi, Xuanlei Zhao, Pengfei Zhou, Kaipeng Zhang†, Zhangyang Wang, Kai Wang†, Yang You (**\* equal contribution, † corresponding author**)

 Representation alignment
 (REPA) that matches Diffusion Transformer (DiT) hidden features to a self-supervised encoder
 (e.g. DINO)—dramatically accelerates the early epochs but plateaus or even de
grades performance later. We trace this failure to a capacity mismatch in gradient directions of repsentation and denoising task, and introduce **HASTE** (Holistic Alignment with Stage-wise
 Termination for Efficient training), a two-phase DiT training schedule that keeps the help and
 drops the hindrance. 
On ImageNet 256×256, it a 28× reduction in optimization steps. HASTE also improves text-to-image DiTs on MS-COCO, demonstrating to be a simple yet principled recipe
 for efficient diffusion training across various tasks.

<div style="display: inline">
    <a href="https://arxiv.org/abs/2505.16792"> <strong>[paper]</strong></a>
    <a href="https://github.com/NUS-HPC-AI-Lab/HASTE"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p>  Diffusion Transformers (DiTs) deliver state-of-the-art image quality, yet their
        training remains notoriously slow. A recent remedy—representation alignment
        (REPA) that matches DiT hidden features to those of a non-generative teacher
        (e.g. DINO)—dramatically accelerates the early epochs but plateaus or even de
        grades performance later. We trace this failure to a capacity mismatch: once
        the generative student begins modelling the joint data distribution, the teacher’s
        lower-dimensional embeddings and attention patterns become a straitjacket rather
        than a guide. We then introduce HASTE (Holistic Alignment with Stage-wise
        Termination for Efficient training), a two-phase schedule that keeps the help and
        drops the hindrance. Phase I applies a holistic alignment loss that simultaneously
        distills attention maps (relational priors) and feature projections (semantic anchors)
        from the teacher into mid-level layers of the DiT, yielding rapid convergence.
        Phase II then performs one-shot termination that deactivates the alignment loss,
        once a simple trigger such as a fixed iteration is hit, freeing the DiT to focus on
        denoising and exploit its generative capacity. HASTE speeds up training of diverse
        DiTs without architecture changes. On ImageNet 256×256, it reaches the vanilla
        SiT-XL/2 baseline FID in 50epochs and matches REPA’s best FID in 500epochs,
        amounting to a 28× reduction in optimization steps. HASTE also improves text
        to-image DiTs on MS-COCO, demonstrating to be a simple yet principled recipe
        for efficient diffusion training across various tasks. Our code is available here.  </p>
    </div>
</div>

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ICLR 2025</div><img src='https://github.com/Raibows/CREAM/blob/main/figures/overview.jpg?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**Cream: Consistency regularized self-rewarding language models**](https://arxiv.org/abs/2410.12735) <img src='https://img.shields.io/github/stars/Raibows/CREAM.svg?style=social&label=Star' alt="sym" height="100%">

Zhaoyang Wang, Weilei He, **Zhiyuan Liang**, Xuchao Zhang, Chetan Bansal, Ying Wei, Weitong Zhang, Huaxiu Yao

**Consistency Regularized sElf-rewarding lAnguage Model (CREAM)** is a self-rewarding framework that improves LLM alignment without human-labeled preference data. It addresses the key issue of reward bias in iterative self-training by:  
  - Formulating a generalized iterative preference fine-tuning framework with explicit consistency regularization.  
  - Leveraging reward stability across iterations to produce more reliable preference labels.  
  - Achieving superior alignment performance and higher reward consistency, even as smaller LLMs (e.g., 7B) face diminishing returns from standard self-rewarding.  

<div style="display: inline">
    <a href="https://arxiv.org/abs/2410.12735"> <strong>[paper]</strong></a>
    <a href="https://github.com/Raibows/CREAM"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p>  LLM-as-a-Judge to iteratively improve the alignment performance without the
 need of human annotations for preference data. These methods commonly utilize
 the same LLM to act as both the policy model (which generates responses) and
 the reward model (which scores and ranks those responses). The ranked responses
 are then used as preference pairs to train the LLM via direct alignment technolo
gies (e.g. DPO). However, it is noteworthy that throughout this process, there is
 no guarantee of accuracy in the rewarding and ranking, which is critical for en
suring accurate rewards and high-quality preference data. Empirical results from
 relatively small LLMs (e.g., 7B parameters) also indicate that improvements from
 self-rewarding may diminish after several iterations in certain situations, which
 we hypothesize is due to accumulated bias in the reward system. This bias can
 lead to unreliable preference data for training the LLM. To address this issue, we
 first formulate and analyze the generalized iterative preference fine-tuning frame
work for self-rewarding language model. We then introduce the regularization
 to this generalized framework to mitigate the overconfident preference labeling
 in the self-rewarding process. Based on this theoretical insight, we propose a
 Consistency Regularized sElf-rewarding lAnguage Model (CREAM) that lever
ages the consistency of rewards across different iterations to regularize the self
rewarding training, helping the model to learn from more reliable preference data.
 With this explicit regularization, our empirical results demonstrate the superior
ity of CREAM in improving both reward consistency and alignment performance.
 The code is publicly available at https://github.com/Raibows/CREAM. </p>
    </div>
</div>

</div>
</div>

<!-- # 🎖 Honors and Awards
- *2021.10*  -->

# 📖 Educations
- *2021.09 - 2025.06*, Bachelor Degree in Artifical Intelligence's Talent Class, University of Science and Technology of China. 

<!-- # 💬 Invited Talks
- *2021.06*,  -->

# 💻 Internships
- *2023.03 - 2024.06*, University of Science and Technology of China, Undergraduate Research Intern. Mentor: [Xiang Wang](https://xiangwang1223.github.io/), [Xiangnan He](https://hexiangnan.github.io/).
- *2024.05 - 2024.10*, University of North Carolina at Chapel Hill, Research Intern. Mentor: [Huaxiu Yao](https://www.huaxiuyao.io/).
- *2024.08 - 2025.08*, National University of Singapore, Research Intern. Mentor: [Yang You](https://www.comp.nus.edu.sg/~youy/). Advisor: [Kaiwang](https://kaiwang960112.github.io/), [Wangbo Zhao](https://wangbo-zhao.github.io/).