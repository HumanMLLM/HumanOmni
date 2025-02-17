# HumanOmni: Human-Centric Omnimodal Large Language Model

[![ModelScope](https://img.shields.io/badge/ModelScope-HumanOmni-blue)](https://modelscope.cn/models/myroot/HumanOmni-7B)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-HumanOmni-yellow)](https://huggingface.co/StarJiaxing/HumanOmni-7B)
[![arXiv](https://img.shields.io/badge/arXiv-2405.15111-red)](https://arxiv.org/abs/2501.15111)

<div align="center">
  <img src="figures/arch.png" width="800"/>
</div>

## Introduction
**HumanOmni** is the industry's first human-centric omnimultimodal large language model designed to achieve comprehensive understanding in human-centric scenes.
1) **Domain-specific capability**: Trained on 2.4M human-centric video clips with 14M instructions
2) **Adaptive fusion**: Features three specialized branches with instruction-guided dynamic fusion
3) **Audio-visual synergy**: Integrates environmental audio cues with visual understanding
   
## Model Downloads
<div align="center">

| **Model** | **#Total Params** | **Download** |
| :------------: | :------------: | :------------: |
| HumanOmni | 7B | [🤗 HuggingFace](https://huggingface.co/StarJiaxing/HumanOmni-7B)   |

</div>


### Upcoming Releases
+ 2B-Lite 
+ 72B-Expert 

## Performance
Here are some performance benchmarks of HumanOmni across various tasks:

<div align="center">
  <figure>
    <img src="figures/result-emotion.png" alt="Emotion Understanding Task Results" width="400"/>
    <figcaption>Fig 1: Performance on the emotion understanding task.</figcaption>
  </figure>
  <figure>
    <img src="figures/result-dfec.png" alt="Dynamic Facial Expression Caption Task Results" width="400"/>
    <figcaption>Fig 2: Performance on the dynamic facial expression caption task.</figcaption>
  </figure>
  <figure>
    <img src="figures/result-mvbench.png" alt="Movement and Pose Understanding Task Results" width="400"/>
    <figcaption>Fig 3: Performance on the action and pose understanding task.</figcaption>
  </figure>
</div>

## Environment Setup

To set up the recommended environment for HumanOmni, follow these instructions:

### Recommended Environment
- **Python**: >=3.10
- **CUDA**: >=12.1
- **PyTorch**: >=2.2 (with CUDA support)
- **Transformers**: >=4.45
- **Accelerate**: >=0.30.1
