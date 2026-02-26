# CRWKV: A Spatially Consistent Causal RWKV Model for Multiple Exposure Correction

This is the official PyTorch code for the paper "[CRWKV: A Spatially Consistent Causal RWKV Model for Multiple Exposure Correction]".

#### 

> **Abstract:** Exposure correction is a fundamental yet challenging task in computational photography, requiring simultaneous restoration of global illumination and local structural details under diverse lighting conditions. Transformer-based models achieve strong performance on dense prediction tasks by modeling long-range dependencies, but their quadratic complexity limits real-time applicability and often underutilizes the inherent 2D structure of images. Recurrent alternatives such as RWKV provide linear-time sequence modeling with causal consistency; however, their 1D formulation is insufficient for capturing multi-scale spatial dependencies in high-fidelity image restoration. To address these limitations, we propose CRWKV, a causality-consistent recurrent key-value framework tailored for exposure correction. CRWKV extends RWKV with 2D causal reasoning across complementary domains, including wavelet, Fourier, and spatial representations. Through multi-level discrete wavelet decomposition and learnable radial frequency splits in the Fourier domain, the model establishes progressive causal dependencies from coarse global context to fine local details. Low-frequency components emphasize illumination and color consistency, while high-frequency components focus on texture and edge restoration. The proposed causal propagation enlarges the receptive field without incurring the quadratic cost of self-attention. Extensive experiments demonstrate that CRWKV achieves state-of-the-art performance on benchmark datasets, surpassing existing Transformer-based and recurrent methods in PSNR, SSIM, and LPIPS while maintaining significantly lower computational complexity.


## Contents

- [√] [Datasets](https://github.com/NJUPT-IPR-XuLintao/UPT-Flow/blob/main/README.md#-datasets)
- [] Training
- [] [Testing](https://github.com/NJUPT-IPR-XuLintao/UPT-Flow/blob/main/README.md#-testing)
- [] [Results](https://github.com/NJUPT-IPR-XuLintao/UPT-Flow/blob/main/README.md#-results)
- [] [Acknowledgements](https://github.com/NJUPT-IPR-XuLintao/UPT-Flow/blob/main/README.md#-acknowledgements)

## 1.Datasets

1、LOLv2 (real & synthetic): Wenhan Yang, Haofeng Huang, Wenjing Wang, Shiqi Wang, and Jiaying Liu. "Sparse Gradient Regularized Deep Retinex Network for Robust Low-Light Image Enhancement", TIP, 2021. [[Baiduyun (extracted code: l9xm)]](https://pan.baidu.com/s/1U9ePTfeLlnEbr5dtI1tm5g) [Google Drive](https://drive.google.com/file/d/1dzuLCk9_gE2bFF222n3-7GVUlSVHpMYC/view?usp=sharing) 

2、LOL-v1: Please refer to [RetinexNet(BMVC2018)](https://github.com/weichen582/RetinexNet)

3、SICE: Please refer to [SICE(TIP2018)](https://github.com/csjcai/SICE)

4、ME: Please refer to [ME(CVPR2021)](https://github.com/mahmoudnafifi/Exposure_Correction)

## 2.Create Environment
1、Python 3.10.12  
2、Pytorch 2.6.0

```

## Acknowledgements
The codes are based on [URWKV]([https://github.com/caiyuanhao1998/Retinexformer](https://github.com/FZU-N/URWKV)), [FreqMamba](https://github.com/aSleepyTree/FreqMamba), and [Uformer](https://github.com/ZhendongWang6/Uformer). Please also follow their licenses. Thanks for their awesome works.
