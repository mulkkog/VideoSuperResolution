# Video Super-Resolution

A paper list of video super-resolution using deep learning.

<br>


## Background

Super-resolution (SR) aims to recover a high-resolution (HR) image from a low-resolution (LR) image which has fewer pixels, higher compression, or both. It is known as an inverse problem as it is the opposite way of modeling degradation caused by unknown functions. It is very challenging and inherently ill-posed since several high-resolution images can be generated from the given low-resolution counterpart.

The SR can be mainly divided into single image super-resolution (SISR), and video super-resolution (VSR), depending on the number of frames processed. SISR methods exploit spatial information in one LR image to enhance the high-frequency details, whereas VSR exploits additional temporal information as it uses neighboring frames. In particular, VSR considers temporal smoothness.

<br>


## Performance Table
Peformance: BI degradation, Vid4 (Y channel), 4x upscaling


| Method 		| Params (M)  	| Performance (PSNR/SSIM)  | Code  | Published In  |
|:-------------	|:------------:	|:------------:	|:----------:|:----------:|
| Bicubic    	| -    			| 23.78/0.6347	| -                | -                |
| VSRNet    	| 0.2    		| 24.81/0.7020	| [-](url)    | [IEEE Transactions on Computational Imaging'16](https://ieeexplore.ieee.org/abstract/document/7444187)    |
| VESPCN    	| 0.9    		| 25.35/0.7560	| [-](url)    | [CVPR'17](https://openaccess.thecvf.com/content_cvpr_2017/papers/Caballero_Real-Time_Video_Super-Resolution_CVPR_2017_paper.pdf)    |
| FRVSR    		| 5.1    		| 26.69/0.8103	| [-](https://github.com/msmsajjadi/FRVSR)    | [CVPR'18](https://arxiv.org/abs/1801.04590)    |
| DUF    		| 5.8    		| 27.33/0.8319	| [Tensorflow](https://github.com/yhjo09/VSR-DUF)    | [CVPR'18](https://openaccess.thecvf.com/content_cvpr_2018/papers/Jo_Deep_Video_Super-Resolution_CVPR_2018_paper.pdf)    |
| RLSP    		| 4.2    		| 27.55/-		| [PyTorch, Tensorflow](https://github.com/dariofuoli/RLSP)    | [arXiv'19](https://arxiv.org/pdf/1909.08080v1.pdf)    |
| RBPN    		| 12.1    		| 27.12/0.8180	| [PyTorch](https://github.com/alterzero/RBPN-PyTorch)    | [CVPR'19](https://openaccess.thecvf.com/content_CVPR_2019/papers/Haris_Recurrent_Back-Projection_Network_for_Video_Super-Resolution_CVPR_2019_paper.pdf)    |
| EDVR    		| 20.6    		| 27.35/0.8264	| [PyTorch](https://github.com/XPixelGroup/BasicSR)    | [CVPRW'19](https://arxiv.org/pdf/1905.02716v1.pdf)    |
| TOFlow    	| 1.4    		| 25.89/0.7651	| [Torch](https://github.com/anchen1011/toflow)    | [IJCV'19](url)    |
| RRN    		| 3.4    		| 27.69/0.8488	| [PyTorch](https://github.com/junpan19/RRN)    | [BMVC'20](https://arxiv.org/pdf/2008.05765v2.pdf)    |
| TDAN    		| 2.2    		| 26.42/0.7890	| [PyTorch](https://github.com/YapengTian/TDAN-VSR-CVPR-2020)    | [CVPR'20](url)    |
| SOF-VSR    	| 1.0    		| 26.00/0.772	| [PyTorch](https://github.com/The-Learning-And-Vision-Atelier-LAVA/SOF-VSR)    | [IEEE Transactions on Image Processing'20](https://arxiv.org/pdf/2001.02129v1.pdf)    |
| VSRT    		| 32.6   		| 27.36/0.8258	| [PyTorch](https://github.com/caojiezhang/VSR-Transformer)    | [arXiv'21](https://arxiv.org/pdf/2106.06847.pdf)    |
| BasicVSR    	| 6.3    		| 27.24/0.8251 	| [PyTorch](https://github.com/XPixelGroup/BasicSR)    | [CVPR'21](https://openaccess.thecvf.com/content/CVPR2021/papers/Chan_BasicVSR_The_Search_for_Essential_Components_in_Video_Super-Resolution_and_CVPR_2021_paper.pdf)    |
| IconVSR    	| 8.7    		| 27.39/0.8279	| [PyTorch](https://github.com/XPixelGroup/BasicSR)    | [CVPR'21](https://openaccess.thecvf.com/content/CVPR2021/papers/Chan_BasicVSR_The_Search_for_Essential_Components_in_Video_Super-Resolution_and_CVPR_2021_paper.pdf)    |
| GOVSR    		| 7.1    		| -			    | [PyTorch](https://github.com/psychopa4/OVSR)    | [ICCV'21](https://openaccess.thecvf.com/content/ICCV2021/papers/Yi_Omniscient_Video_Super-Resolution_ICCV_2021_paper.pdf)    |
| VRT    		| 35.6    		| 27.93/0.8425	| [PyTorch](https://github.com/jingyunliang/vrt)    | [arXiv'22](https://arxiv.org/pdf/2201.12288v2.pdf)    |
| BasicVSR++	| 7.3    		| 27.79/0.8400	| [PyTorch](https://arxiv.org/pdf/2104.13371.pdf)    | [CVPR'22](https://github.com/ckkelvinchan/BasicVSR_PlusPlus)    |
| ETDM    		| 8.4    		| -			    | [PyTorch](https://github.com/junpan19/ETDM)    | [CVPR'22](https://arxiv.org/pdf/2204.07114.pdf)    |
| Zhou et al.	| 17.0    		| 27.90/0.8380	| [PyTorch](https://github.com/redrock303/Revisiting-Temporal-Alignment-for-Video-Restoration)    | [CVPR'22](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhou_Revisiting_Temporal_Alignment_for_Video_Restoration_CVPR_2022_paper.pdf)    |
| RVRT    		| 10.8    		| 27.99/0.8462	| [PyTorch](https://github.com/jingyunliang/rvrt)    | [NeurIPS'22](https://arxiv.org/pdf/2206.02146.pdf)    |

<br>


## Datasets

| Name | Usage  | Resolution  | Site  | 
|:----------|:----------|:----------|:----------|
| REalistic and Dynamic Scenes dataset (REDS)   | Train/Test    | 720 × 1280    | [download](https://seungjunnah.github.io/Datasets/reds.html)    | 
| Vimeo90K    | Train/Test    | 448 × 256     | [download](http://toflow.csail.mit.edu/)    | 
| Vid4    | Test    | walk (740x480), foliage (740x480)<br>city (704x576), calendar (720x576)    | [download](https://drive.google.com/file/d/1ZuvNNLgR85TV_whJoHM7uVb-XW1y70DW/view)    |





