<div align="center">

# BiSF-Net

BiSF-Net: Bidirectional Spatial-Frequency Extraction and Fusion Network for Underwater Image Enhancement
</div>

## Overview
<p align="center">
    <img src="image/Overall framework.png" width="80%" style="border-radius: 15px">
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
<数据集根目录>/
├── test/                 # 测试集目录
│   └── [测试图片文件]    # 仅存放测试输入图片（无标注/GT文件）
├── train/                # 训练集目录
│   ├── gt/               # 训练集真值/标注图片目录
│   │   └── [训练GT图片]
│   ├── input/            # 训练集输入图片目录
│   │   └── [训练输入图片]
│   └── traindata_list.txt # 训练集文件列表（由extract_name.py自动生成）
├── valid/                # 验证集目录
│   ├── gt/               # 验证集真值/标注图片目录
│   │   └── [验证GT图片]
│   ├── input/            # 验证集输入图片目录
│   │   └── [验证输入图片]
│   └── validdata_list.txt # 验证集文件列表（由extract_name.py自动生成）
├── traindata_list.txt     # 根目录训练集列表副本（由extract_name.py生成）
└── validdata_list.txt     # 根目录验证集列表副本（由extract_name.py生成）

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


