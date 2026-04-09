<div align="center">

# BiSF-Net

BiSF-Net: Bidirectional Spatial-Frequency Extraction and Fusion Network for Underwater Image Enhancement
</div>

## Overview
<p align="center">
    <img src="frame.png" width="80%" style="border-radius: 15px">
</p>

## Requirements 
Please install the corresponding libraries according to the versions listed below. For other detailed versions, refer to requirements.txt.
- python==3.8.20
- torch==2.2.0
- torchvision==0.17.0
- opencv-python==4.13
- einops==0.8.1
- basicsr==1.4.2
- lpips==0.1.4
- mmcv==2.2.0
- mmengine==0.10.7
## Datasets setting 


### Train

An example of training on UIEB
```
 python train.py -d UIEB --cuda --b 32 --ckpt-save-path ../ckpts --nb-epochs 500  
```
### Test
An example of testing on UIEB
```
 python src/test_PSNR.py --dataset-name UIEB --path ./data/UIEB/test   
```


