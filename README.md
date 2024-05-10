# Face-Detection
- 목적 : 버스의 CCTV 영상 안의 얼굴을 인식하여 비식별화를 진행
- 얼굴을 인식할 수 있는 여러 모델이 계속 발전하고 있는 중
- 성능이 좋은 모델을 선택하는 것이 어려움.
- 인터넷의 여러 글을 참고하여 RetinaFace_Resnet과 YOLO V8을 선택하였음.
- 실행 속도(범용 노트북) RetinaFace_Renet : 3.5시간 / 2500장, YOLO V8 : 40분 / 2500장 
- https://learnopencv.com/what-is-face-detection-the-ultimate-guide/#RetinaFace-(May-2019)
- https://www.youtube.com/watch?v=_eSArKZBWmE
- https://github.com/noorkhokhar99/face-detection-yolov8
- 두 모델을 순차적으로 실행하여 결과를 얻었는데 2500장 이미지 중 10장 내외로 인식 못하는 얼굴이 있었음.
- 더 나은 모델을 찾아야 함.
- YOLO V8은 여러 파라미터 조절로 인식율을 조절할 수 있음.
  - confidence 기본 값은 0.25이고 대부분은 0.1로 실행. 더 낮은 값으로 해도 인식 안되는 것을 개선하지 못함.
- 조명이 비춰 얼굴에 점박이가 있는 것은 인식이 잘 안됨.
- 여러 번 모델 적용하고 confidence 값을 낮춰도 인식 안되는 것은 수작업으로 진행함. (ROI_Blur)

  
