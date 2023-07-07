## 📑 프로젝트 소개
2017년에 IEEEInternational Conference on Image Processing (ICIP)에서 발표된
Simple online and realtime tracking with deep association metric 논문을 리뷰해보면서 
obiect tracking의 프레임 워크중 하나인 deep sort에 대해 자세히 공부하고 관련 코드에 대해 리뷰해보았습니다.
이 프로젝트는 구현보다는 obiect tracking에 대 해 더 자세히 공부하는것에 초점을 맞추고 있습니다

## 👏 팀 소개 

|이지호|이제희|박준하|김수연
|![image](https://github.com/khuda-3rd/README_example/assets/90135669/e5ebdc70-3dfa-493f-a865-3d14b2bc7685)|![image](https://github.com/khuda-3rd/README_example/assets/90135669/6f986eee-9e0d-48cb-b2f5-fa9cf785fb8e)|![image](https://github.com/khuda-3rd/README_example/assets/90135669/fcb6281e-6bdd-4f06-9cb7-eb5772c88803)|![image](https://github.com/khuda-3rd/README_example/assets/90135669/fcb6281e-6bdd-4f06-9cb7-eb5772c88803)|
|[개인 리포지토리](https://github.com/khuda-3rd)|[개인 리포지토리](https://github.com/khuda-3rd)|[개인 리포지토리](https://github.com/khuda-3rd)|[개인 리포지토리](https://github.com/khuda-3rd)|


## 🔎 핵심 기능 구현
### OBJECT TRACKING

![Untitled](https://github.com/LEE-JIHO-1016/KHUDA-Project/assets/76989907/0c5b865a-ffb8-4a8f-8a73-c2601aaed182)

일단 영상이 들어오면 한 부분에 물체가 있다는걸 인식 (Object Recognition)하고,

그 물체가 무엇인지(Objectt Classification)하고 정확한 위치를 찍어줌(Object Localization). 

OC와 OL이 합쳐지면 Object Detection, OD 가 된다. 추후 OD의 결과로 각 Box를 이전 Frame과 비교 하여 ID를 매칭시키고 여러가지 기술들을 사용 하는게 Object Tracking

두가지로 나눠어진다. 
![Untitled](https://github.com/LEE-JIHO-1016/KHUDA-Project/assets/76989907/075c2a5f-734b-4fb8-998e-e473cde1363e)


### DEEP SORT
Deep SORT(Deep Simple Online and Realtime Tracking)는 객체 추적(object tracking)을 위한 알고리즘입니다. 객체 추적은 비디오에서 프레임 간에 움직이는 객체를 식별하고 추적하는 작업을 의미합니다. Deep SORT는 이러한 객체 추적 작업을 실시간으로 수행할 수 있는 딥러닝 기반의 알고리즘입니다.
<br/> 

Deep SORT는 두 가지 주요 구성 요소인 객체 감지(object detection)와 객체 추적(object tracking)으로 구성됩니다. 객체 감지는 주어진 프레임에서 객체를 식별하는 작업을 수행하고, 객체 추적은 프레임 간에 객체의 이동을 추적하는 작업을 수행합니다.
<br/>

Deep SORT는 객체 감지를 위해 일반적으로 딥러닝 기반의 객체 감지 모델인 YOLO(You Only Look Once)나 SSD(Single Shot MultiBox Detector)와 같은 모델을 사용합니다. 이러한 모델은 이미지나 비디오에서 객체를 감지하고 경계 상자(bounding box)를 추출하는 데 사용됩니다.
<br/>

객체 추적 단계에서 Deep SORT는 추적 대상 객체와 프레임 간의 관계를 모델링하기 위해 딥러닝 기반의 Siamese 네트워크를 사용합니다. Siamese 네트워크는 추적 대상 객체의 특징을 학습하고 이를 사용하여 프레임 간에 객체의 유사성을 계산합니다. 이를 통해 객체 추적을 지속적으로 유지할 수 있습니다.
<br/>

또한 Deep SORT는 객체 추적의 정확성을 향상시키기 위해 Kalman 필터(Kalman filter)와 특징 기반의 데이터 연결(data association) 알고리즘을 사용합니다. Kalman 필터는 객체의 위치와 속도를 추적하고 예측하는 데 사용되며, 데이터 연결 알고리즘은 객체 감지와 추적 결과를 연결하여 추적의 일관성을 유지합니다. 헝가리안 알고리즘은 행렬 형태로 작업과 작업자 간의 비용을 표현하고, 최적의 할당을 찾기 위해 행과 열을 순서대로 스캔하면서 매칭을 결정하는 방식을 사용합니다.


## 📄 Reference
- [논문 링크](https://arxiv.org/abs/1703.07402)
- [레퍼지토리 링크](https://www.notion.so/KHUDA-2-Project-a5f5988d604547bcb3db227303fb2aec)
