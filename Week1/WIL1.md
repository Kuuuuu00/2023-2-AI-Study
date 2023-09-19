스터디를 하면서 배운 내용

딥러닝에 대한 기본적인 정의.
알고리즘을 학습 시키는 중에 잘목 예측하는 정도에 대한 지표인 Loss function이 중요해 보였다..!
Loss function에는 3가지가 있는데... MSE, Cross Entropy, MLE (아직 잘 모르겠다)

Optimization (최적화)
Loss fuction을 줄이기 위한 기법으로 Gradient Descent Method. 보통 Adam 사용

Regularization(조직화..?)
학습을 방해하여 성능을 높이는 것. ealry stopping, parameter norm penalty 등

test set에서 과적합(overfitting)을 방지하는게 중요한 과정..!

비선형 함수... 활성함수... 선형대수학을 안배워서 그런가 잘 이해 못함

generalization gap을 줄이는 방향으로..!

CNN = 합성곱 신경망

RGB 이미지 데이터는 height width depth 3개의 채널로 되어있다.
CNN 파라미터 계산에 대한 내용이 있는데, 이론적 내용이라 계산을 어떻게 하는지는 아직 잘 모르겠음.
= 과제 예제를 풀면서 어느정도 알 거 같아졌다!!

O = (I - K + 2P)/S + 1
W = K^2 * C * N