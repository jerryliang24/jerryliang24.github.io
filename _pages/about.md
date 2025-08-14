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

  I am Zhiyuan Liang, an intern at <a href=""> Tencent</a> supervised by Dr. <a href="https://kaiwang960112.github.io/">Kai Wang</a>. 

  I'm extraodinarily fortunate to work as an intern at <a href="https://ai.comp.nus.edu.sg/"> NUS HPC AI Lab</a> for a fruitful year, under the supervision of Prof.<a href="https://www.comp.nus.edu.sg/~youy/">Yang You</a>, and advised by Dr. <a href="https://kaiwang960112.github.io/">Kai Wang</a> and <a href="https://wangbo-zhao.github.io/">Wangbo Zhao</a>.
  Before that, I worked as an intern at UNC Chapel Hill under the supervision of Prof <a href="https://www.huaxiuyao.io/"> Huaxiu Yao </a>. 

  My research interest lies in **Parameter Generation** and **Multimodal Understanding**, obtaining higher level of intelligence from the angle of weight space learning, and exploring the unified learning paradigm across various modalities.
  I'm actively seeking for PhD opportuninties.



# 🔥 News
- *2025.06*: 🎉I received bachelor degree from USTC! 
- *2025.07*: 🌟 Our new work, Drag-and-Drop LLMs, customizes LLMs in seconds without tuning! Check our [paper](https://arxiv.org/abs/2506.16406) and [code](https://github.com/jerryliang24/Drag-and-Drop-LLMs)! 
- *2025.08*: 🐧 I join Tencent as an intern in multimodal understanding and parameter generation!

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='https://github.com/jerryliang24/jerryliang24.github.io/blob/main/DnD/static/images/pipeline.jpg?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**Drag-and-Drop LLMs: Zero-Shot Prompt-to-Weights**](https://arxiv.org/abs/2506.16406) <img src='https://img.shields.io/github/stars/jerryliang24/Drag-and-Drop-LLMs.svg?style=social&label=Star' alt="sym" height="100%">

**Zhiyuan Liang $^{\dagger}$**, 
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
Zhangyang Wang $^{\dagger}$, 
Kai Wang $^{\dagger}$ (**$^{\dagger}$ project lead**)

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

Mengxuan Wu $^{*}$,  Zekai Li $^{*\dagger}$,  **Zhiyuan Liang $^{*}$**,  Moyang Li,  Xuanlei Zhao,  Samir Khaki,  Zheng Zhu,  Xiaojiang Peng,  Konstantinos N. Plataniotis,  Kai Wang $^{\ddagger}$,  Wangbo Zhao $^{\ddagger}$,  Yang You (**\* equal contribution,  $\dagger$ project lead,  $\ddagger$ corresponding author**)

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

<!-- # 🎖 Honors and Awards
- *2021.10*  -->

# 📖 Educations
- *2021.09 - 2025.06*, Bachelor Degree in Artifical Intelligence's Talent Class, University of Science and Technology of China. 

<!-- # 💬 Invited Talks
- *2021.06*,  -->

# 💻 Internships
- *2024.05 - 2024.10*, University of North Carolina at Chapel Hill, Research Intern. Mentor: [Huaxiu Yao](https://www.huaxiuyao.io/).
- *2024.08 - 2025.08*, National University of Singapore, Research Intern. Mentor: [Yang You](https://www.comp.nus.edu.sg/~youy/). Advisor: [Kaiwang](https://kaiwang960112.github.io/), [Wangbo Zhao](https://wangbo-zhao.github.io/).
- *2024.08 - now* Tencent, Intern in Multimodal Understanding and Parameter Generation. Mentor: [Kai Wang](https://kaiwang960112.github.io/).