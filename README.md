# CBAM-GradCAM-for-Emotion-Classification

CAM & Attention을 활용한 딥러닝의 표정 분류법 분석

by Wooseok Hyung

## 1. Model Training

https://github.com/Jongchan/attention-module 의 코드에서 FER+ Dataset에 맞게 코드를 수정하여 사용하였음.

Code 예시: 

python train_mydata.py --prefix V_R20_lr01_E50 --print-freq 88 --lr 0.1  (Vanilla ResNet-20 학습)

python train_mydata.py --prefix C_R20_lr01_E50 --print-freq 88 --lr 0.1 --att-type CBAM (ResNet-20 + CBAM 학습)
