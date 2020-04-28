## 회의 개요

>4월 28일 주간 회의 진행 (멀티캠퍼스 역삼)

1. 주간 진행사항 계획
2. 각자 코드 분석
   - 코드1 : https://github.com/michalfaber/keras_Realtime_Multi-Person_Pose_Estimation
   - 코드2 : https://github.com/dmlc/gluon-cv/
3. 05.01(금)  코드 공유 및 스터디

## 회의 내용

>구현된 코드 리뷰 & 향후 발전 방향 모색 

1. 코드 리뷰
   - 코드1 : 속도는 비교적 빠른편이지만, 관절 keypoints 개수가 적음 => 척추,발 부분 keypoints 추가 필요
   
   - 코드2 : 실시간 detection의 정확도는 좋으나, 속도가 느림 => 속도 개선 필요
   
2. 기술 스터디
   - **제공 코드 : OpenCV 환경에서 웹캠 속도 개선을 위한 코드**
     
     - [Basic motion detection and tracking with Python and OpenCV](https://www.pyimagesearch.com/2015/05/25/basic-motion-detection-and-tracking-with-python-and-opencv/)
     - [Real-time object detection with deep learning and OpenCV](https://www.pyimagesearch.com/2017/09/18/real-time-object-detection-with-deep-learning-and-opencv/)
   - 기술 구현 계획
     
     - 각자 웹캠에서 기술 구현 후 개선 사항 스터디 진행
     
       

## 결정사항

>기타 사항

1. 05.01(금) 개인 당 15분씩 분석한 코드 공유
2. 가능하다면 pyinstaller를 통해 .exe 파일 생성을 목표로 함



