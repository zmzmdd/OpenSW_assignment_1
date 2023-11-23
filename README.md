﻿# 환경 구축 방법
1. anaconda에서 가상환경 생성
    conda create -n [가상환경 명] python==3.7
    conda activate [가상환경 명]

2. git clone https://github.com/matterport/Mask_RCNN
3. pip install keras==2.1.2
4. pip install tensorflow-gpu==1.15.5
5. pip install -U scikit-image==0.16.2
6. pip install protobuf==3.20.*
7. Mask_RCNN - model - balloon - datasets - logs 와 같이 폴더를 만든다(git clone으로 생성된 Mask_RCNN 폴더에)
8. 아래의 파일을 다운 받아 Mask_RCNN 폴더에 복사
    https://github.com/matterport/Mask_RCNN/releases/download/v2.1/mask_rcnn_balloon.h5
    https://github.com/matterport/Mask_RCNN/releases/download/v1.0/mask_rcnn_coco.h5
9. https://github.com/matterport/Mask_RCNN/releases/download/v2.1/balloon_dataset.zip -> datasets 폴더에 압축해제
    model - balloon - datasets 폴더에 train과 val 폴더가 있어야 한다
10. python balloon.py --dataset ../../model/balloon/datasets --weights ../../mask_rcnn_balloon.h5 --logs ../../model/balloon/logs --image ../../model/balloon/datasets/val/3800636873_ace2c2795f_b.jpg splash
10-1. 3800636873_ace2c2795f_b.jpg 이 부분에 val 폴더 내에있는 다른 사진의 이름을 넣으면 그 사진으로 inference 가능   
