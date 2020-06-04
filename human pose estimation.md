##### [AI 콜로퀴움 2] Human Pose Estimation 기술의 발전과 미래(이경무 교수)

링크 동영상:https://www.youtube.com/watch?v=GBpnsFfLt2Q



### 컴퓨터비전 문제

-------------

1. object detection & recognition

2. Scene understanding

3. 3D reconstruction

4. tracking

5. image/video restoration

6. segmentation

   

### 딥러닝과 컴퓨터비전

---------------------------

AlexNet - 획기적인 결과를 보여줌



### 휴먼포즈추정 문제란?

-----

RGB영상 또는 거리(depth)영상으로부터 주요 신체 분위(joint)의 위치를 찾는 문제

정의된 신체모델 사용



### 응용분야

------------------------------------

HCI, AR/VR 핵심기술

자율자동차, 로봇, 게임, 의료, 스포츠, 감시 장치



### Human Pose가 왜 어려운가

--------------------

- self and External occulsion

- arms and legs foreshortenig

- varying illumination

- clothing variation

- motion blur

  

### Marker vs. Markerless 시스템

------

Marker 기반 motion capture system: 특수 마커(marker) 부착 및 센싱 기반의 신체 joint 위치 추정기술

스튜디오환경에서 영화, 게임, AR/VR 등 특수효과에 주로 사용



##### marker의 단점

- high cost - 최소 $10000
- 특수 장비, 복장 및 환경의 제약성



### Markerless 시스템

----------------------------------

Markerless 포즈추정 시스템: RGB 카메라 또는 depth 카메라를 이용하여 마커 없이 신체 joint 위치 추정

Low cost, 일반환경에서 다양한 응용에 사용가능



### Markerless 포즈 추정 기법

---------------------------------



### Makerless 휴먼포즈 추정 문제의 종류

--------------------------

![image-20200604111938149](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20200604111938149.png)



2D pose는 연구가 많이 되어있지만, 3D pose는 아직 진행중



### 딥러닝 이전의 휴먼포즈 추정기법

----------------------------------------------



#### 초창기 접근 방법

-------------------

- pictorial structure
- 사람의 신체를 신체부위 (part)와 관계(spring)으로 모델링
- 영상에서 해당 부위를 매칭함으로써 포즈 추정
- 최초의 휴먼포즈 추정 기법



### 거리정보(depth) 기반 포즈 추정 기법

--------------------

Microsoft kinect Xbox - 착용장비없이 게임을 플레이할 수 있다. 



##### 사업적 성공실패

- 프라이버시 문제
- 기술을 이용할만한 다양한 소프트웨어 부재





### 딥러닝 기반 휴먼포즈 추정 기법

----------------------------------------

DeepPose: 최초의 딥러닝 기반 2D 휴먼포즈 추정

입력 RGB 영상에 대해 CNN-regressor를 이용하여 점진적으로 신체 joint의 2D 좌표를 추정



### Heatmap 이용

----------------

Heatmap을 사용한 휴먼 포즈 추정 기법

좌표 대신 joint가 나타날 확률(heatmap)을 추정함으로써 정확도 향상

그래프 모델과 CNN을 결합함으로써 joint들간의 위치관계 사용

여전히 신체구조적 정보 부족



contect, receptive field, local & global feature

------------------

컨텍스트(context)와 신체 구조 정보의 활용

CPM: Body joint들의 공간적 관계 정보 학습을 위하여 큰 receptive field을 이용

순차적으로 receptive field를 키우고 contex정보를 이용하여 joint추정의 정확도를 높임



### 전역과 지역 특징정보의 활용

----------------



### Multi person 2D pose

------

딥러닝 기반 2D 멀티 휴먼 포즈 추정 기법

openpose: 최초의 딥러닝기반 2D 멀티 휴먼 포즈추정 기법

Bottom-up 방식: 입력영상 내의 모든 2D joint들을 추정한 후, joint들간의 관계성 (part affinity field)정보를 이용하여 개별 사람의 포즈 검출







### Refinement 기법 - PoseFix

-------------------------------------------------------------

PoseFix: 기존 시스템의 에러를 줄이는 후처리 시스템

대부분의 휴먼포즈 추정시스템은 공통적인 에러특성을 가지고 있음

실제 에러특성 확률 모델을 이용 가상의 에러 데이터를 합성, refine network 학습



### 3D Human Pose

------------------------------------

V2V PoseNet: 입력과 출력을 모두 Voxel로 표현함으로써 성능향상



### RGB기반 2D포즈로부터 3D 포즈 추정 기법

-------------------------------

최초의 single 휴먼 3D 포즈추정기법

3D 포즈 추정문제를 '2D 포즈 추정' + 'Lifting' 문제로 분리 해결



### RGB기반 3D 다중 휴먼 포즈 추정기법

-----------------

최초의 end-to-end 다중 휴먼 3D pose estimation 기법

카메리 기반 실제 거리 정보 추정 

단일영상에서의 대상 사람의 실제 거리 측정의 모호성 존재

학습을 통하여 대상의 나이,자세 등을 파악 영상내 크기와 실제 거리와의 모호성을 해결





### 3D Shape and Pose

-------------------------

단일 RGB영상으로부터 인체의 3D shape과 포즈 정보를 동시에 추정하는 최초의 기법

Parametric human 모델(SMPL) 사용



### Model-free 3D 형상 및 포즈 추정 기법

------------------

end-to-end model free, 직접 3D 메쉬모델 포즈 추정

sota 성능



### 결론 및 전망

--------------------------------

- 휴먼포즈 인식 추정 기술은 최근 5-6년간 딥러닝 기술에 힘입어 획기적인 발전을 이룸

- 기술의 성숙도에 따라 다양한 응용분야에서의 새로운 비즈니스가 창출될 것으로 예상

- 특히 AR/VR, 로봇, 의료분야에서의 폭발적 성장이 예상됨




##### 향후과제

- 행동인식 및 예측문제에 적용
- 원거리, 극한 상황에서의 휴먼 포즈 인식 문제해결
- 3D 포즈 생성 및 전이 문제
- 실시간 엣지 컴퓨팅 기술 확보
- 응용분야별 대용량 실제 데이터셋 확보 필요
- 다양한 사회문제 대응, 새로운 비즈니스 창출







