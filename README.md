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

| **Model** | **#Total Params** | **Download-Huggingface** | **Download-ModelScope** |
| :------------: | :------------: | :------------: | :------------: |
| HumanOmni-Instruct | 7B | [![Hugging Face](https://img.shields.io/badge/HuggingFace-HumanOmni-yellow)](https://huggingface.co/StarJiaxing/HumanOmni-7B)  | [![ModelScope](https://img.shields.io/badge/ModelScope-HumanOmni-blue)](https://modelscope.cn/models/myroot/HumanOmni-7B) |
| HumanOmni-Base | 7B | [![Hugging Face](https://img.shields.io/badge/HuggingFace-HumanOmni-yellow)](https://huggingface.co/StarJiaxing/HumanOmni-7B)  | [![ModelScope](https://img.shields.io/badge/ModelScope-HumanOmni-blue)](https://modelscope.cn/models/myroot/HumanOmni-7B)

</div>


### Upcoming Releases
+ 2B-Lite 
+ 72B-Expert 

## Performance
Here are some performance benchmarks of HumanOmni across various tasks:

## Performance

Emotion Understanding:

| Method                          | Modalities | DFEW (UAR) | DFEW (WAR) | MAFW (UAR) | MAFW (WAR) |
|----------------------------------|------------|-------------|-------------|-------------|-------------|
| **Specialized models for emotion-related tasks** |            |             |             |             |             |
| Wav2Vec2.0                   | A          | 36.15       | 43.05       | 21.59       | 29.69       |
| HuBERT                       | A          | 35.98       | 43.24       | 25.00       | 32.60       |
| DFER-CLIP                     | V          | 59.61       | 71.25       | 38.89       | 52.55       |
| MAE-DFER                      | V          | 63.41       | 74.43       | 41.62       | 54.31       |
| HiCMAE                        | AV         | 63.76       | 75.01       | 42.65       | 56.17       |
| Emotion-LLaMA                 | AV         | 64.21       | 77.06       | -           | -           |
| MMA-DFER                         | AV         | 66.85       | 77.43       | 44.25       | 58.45       |
| **Other models**                 |            |             |             |             |             |
| Qwen2-VL-7B                  | V          | 43.08       | 52.83       | 31.67       | 45.89       |
| Qwen2-VL-72B                  | V          | 39.24       | 45.12       | 42.61       | 46.07       |
| VITA                          | AV         | 21.36       | 32.07       | 14.05       | 33.38       |
| InternLM-XComposer-2.5-OL     | AV         | 44.23       | 51.29       | 33.78       | 46.81       |
| GPT4-O                       | AV         | 50.57       | 57.19       | 38.29       | 48.82       |
| **HumanOmni**                    | AV         | **74.86**   | **82.46**   | **52.94**   | **68.40**   |

Results on DFEC:

## Performance

Comparison of different methods on the DFEC benchmark:

| Method                          | Correctness | Detail | Context | Temporal | CIDEr  | Rouge-L | AutoDQ  |
|----------------------------------|-------------|--------|---------|----------|--------|---------|---------|
| **Vision large language model** |             |        |         |          |        |         |         |
| VideoLLaMA                    | 3.60        | 3.67   | 3.84    | 3.50     | 0.189  | 0.196   | 0.303   |
| VideoChat                     | 3.47        | 3.52   | 3.92    | 3.38     | 0.251  | 0.192   | 0.344   |
| VideoChat2                    | 3.70        | 3.56   | 4.16    | 3.52     | 0.202  | 0.229   | 0.311   |
| Chat-UniVI                    | 3.64        | 3.63   | 4.21    | 3.61     | 0.189  | 0.231   | 0.396   |
| LLaVA-Next-Video              | 4.19        | 4.07   | 4.39    | 4.04     | 0.250  | 0.249   | 0.395   |
| ShareGPT4Video                | 4.24        | 4.13   | 4.35    | 4.09     | 0.192  | 0.205   | 0.394   |
| LLaMA-VID                     | 3.95        | 4.01   | 4.22    | 3.71     | 0.195  | 0.231   | 0.339   |
| VideoLLaMA2                   | 4.17        | 4.02   | 4.47    | 3.93     | 0.253  | 0.266   | 0.344   |
| PLLaVA                        | 4.21        | 4.15   | 4.37    | 4.08     | 0.268  | 0.250   | 0.393   |
| ST-LLM                        | 4.00        | 3.98   | 4.31    | 3.94     | 0.213  | 0.238   | 0.321   |
| Tarsier                       | 3.59        | 3.50   | 4.07    | 3.41     | 0.143  | 0.185   | 0.415   |
| LLaVA-OneVision              | 3.68        | 3.47   | 4.10    | 3.42     | 0.115  | 0.165   | 0.379   |
| FaceTrack-MM                 | 4.42        | 4.30   | 4.60    | 4.26     | 0.418  | 0.473   | 0.483   |
| Qwen2-VL-72B                 | 4.28        | 4.14   | 4.55    | 4.08     | 0.241  | 0.314   | 0.449   |
| Qwen2-VL-7B                  | 4.23        | 4.16   | 4.52    | 4.02     | 0.204  | 0.233   | 0.422   |
| Qwen2-VL-2B                  | 4.01        | 3.98   | 4.37    | 3.88     | 0.202  | 0.221   | 0.406   |
| Claude3.5-Sonnet             | 4.13        | 4.01   | 4.49    | 4.05     | 0.243  | 0.228   | 0.442   |
| **Omni-modality large language model** |      |        |         |          |        |         |         |
| GPT4-O                       | 4.22        | 3.97   | 4.48    | 3.90     | 0.264  | 0.213   | 0.432   |
| VITA                         | 3.98        | 3.74   | 4.11    | 3.59     | 0.191  | 0.224   | 0.366   |
| InternLM-XComposer-2.5-OL    | 3.91        | 3.70   | 4.12    | 3.54     | 0.113  | 0.164   | 0.382   |
| **HumanOmni**                    | **4.58**    | **4.41**| **4.70**| **4.41** | 0.412  | 0.468   | **0.523**|



## Environment Setup

To set up the recommended environment for HumanOmni, follow these instructions:

### Recommended Environment
- **Python**: >=3.10
- **CUDA**: >=12.1
- **PyTorch**: >=2.2 (with CUDA support)
- **Transformers**: >=4.45
- **Accelerate**: >=0.30.1
