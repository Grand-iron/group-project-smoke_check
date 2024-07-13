MobileNetv2는 105개의 layer를 갖고 있다. 경량화를 통해 연산 속도가 빠르고, 계산 자원과 메모리 사용이 크게 줄어들어 모바일 디바이스 같은 제한적 환경에서도 활용 가능하다.
주요 특징으로는 Inverted Residual과 Linear Bottleneck이 있다. Inverted Residual은 저차원 입력을 고차원으로 확장해 특징을 추출한 후, 다시 저차원으로 만드는 구조이며, Linear Bottleneck은 확장 및 축소에 있어 사용되는 비선형 활성화 함수ReLu의 정보 손실 문제를 해결하는 데 중요한 역할을 한다.
