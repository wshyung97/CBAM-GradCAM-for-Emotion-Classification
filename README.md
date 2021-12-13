# CBAM+GradCAM for Emotion Classification

CAM & Attention을 활용한 딥러닝의 표정 분류법 분석

by Wooseok Hyung

## 1. Model Training

https://github.com/Jongchan/attention-module 의 코드에서 FER+ Dataset에 맞게 코드를 수정하여 사용하였음.

Code 예시: 

python train_mydata.py --prefix V_R20_lr01_E50 --print-freq 88 --lr 0.1  (Vanilla ResNet-20 학습)

python train_mydata.py --prefix C_R20_lr01_E50 --print-freq 88 --lr 0.1 --att-type CBAM (ResNet-20 + CBAM 학습)

코드 실행시 checkpoints 폴더에 checkpoint와 model_best에 대한 model이 저장된다.

또한, 기존 코드에서 수정하여 epoch에 따른 train과 vaildation의 accuracy & loss를 numpy array 형식의 .npy 확장자로 저장이 된다.

## 2. Grad-CAM 사용

https://github.com/jacobgil/pytorch-grad-cam 의 Library을 사용하였다.

(설치법: pip install grad-cam)

사용한 코드는 Grad-CAM.ipynb 참고.

## 3. Accurcy & Loss 시각화

사용한 코드는 Visualizaion.ipynb 참고, 결과물은 result 폴더를 확인하면 된다.
