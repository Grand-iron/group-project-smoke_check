EfficientNetV2 모델 (3 x 224 x 224)

구성:
MBConv (Mobile Inverted Bottleneck Convolution) 블록의 반복적 사용.
BatchNormalization -> Activation -> Conv2D 과정 반복 후 Dropout -> add (이미지 사이즈를 줄여가며 반복)

특징 (이론):
점진적으로 이미지 크기를 증가시켜서 학습 속도를 높이는 방식으로, 이전 버전에 비해 최대 6.8배 작은 모델 크기를 가질 수 있으며 정확도가 높다. 그러나 이미지 크기와 정규화를 동적으로 조정해야 하기 때문에 초기 설정과 학습 과정에 있어 상대적으로 유연성이 낮고 복잡하다는 단점이 있다.

구현 결과:
1epoch 기준 137s 1s/step 의 속도로 진행 되었으며, 이미지 분류 성능은 점차 증가하는 모습은 보였지만 정확도가 정체현상을 68%에서 보인다.
predict결과는 학습셋 검증셋과 똑같은 결과를 보인다.
