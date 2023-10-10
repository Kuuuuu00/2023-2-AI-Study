4주차 배운 것

Object Detection

RGB image 를 넣으면 라벨과 바운딩 박스로 출력!

image classification은 대상이 무엇인지 식별하는 것 sigle lable

 object detection은 rgb 이미지에서 여러 대상을 구별해서 정보값으로

 softmax Loss(식별할 떄)와 L2 Loss(위치정보)를 더해서 Weighted Sum Loss

 Sliding Window를 이미지 상 옆으로 옮겨가면서 

1000개의 이미지 클래스가 있으면 총 1001개

sliding window의 사이즈를 다르게 하면 총 가능한 박스수 
= H(H+1)/2 * W(W+1)/2
이므로 이미지 사이즈가 커지면 Image Classification 필요 가짓수가 엄청나게 늘어남.

-> 모든 경우의 수 따지기는 무리

Selective Search 알고리즘으로 영역 제한
-> Region-Based CNN 
  1. ROI 뽑기 
  2. warping(roi를 Conv Net에 넣기 위해 찌그러 뜨리는 것) 
  3. Compute CNN features 
  4. Classify (Linear SVM)

  IOU 는 같은 object를 가르키고 있는 bbox를 제거하는데 쓰임(NMS)

TP = 모델의 positive 예측과 실제 상황이 일치

  precision = TP + / TP + FP (모델의 positive 예측 합)
  Recall = TP / TP + FN (실제 상황의 positive)


Fast R-CNN

1번의 CNN

CNN 먼저하고 Resize 
ConvNet 돌리고 feature map을 뽑아
ROI Pooling 하여 class와 bbox 뽑아냄


Faster R-CNN

CNN 통과시켜 feature map 뽑기
ROI Pooling 

사이에 
RPN 추가 (selective search 대신 사용하는 region proposal 방법)

