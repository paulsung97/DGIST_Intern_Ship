# Dgist_Intern_Ship

**활동:** 2022.12.26-2023.01.31

**연구실:** Department of Electrical Engineering and Computer Science, Communication and Signal Processing Laboratory

**최종 발표:** Yolov7 모델을 이용한 해상도 채널 상태에 따른 mAP, Latency 평가


**기술 스택:** YOLOv7, MATLAB, Python, R programming


**수료증:**
[23년_동계_수료증-73.pdf](https://github.com/paulsung97/Dgist_Intern_Ship/files/11725724/23._._.-73.pdf)

## 연구 논문:
#### [Adaptive Transmit Power Control Algorithm for Sensing-Based Semi-Persistent Scheduling in C-V2X Mode 4 Comm.pdf](https://github.com/paulsung97/Dgist_Intern_Ship/files/11725686/Adaptive.Transmit.Power.Control.Algorithm.for.Sensing-Based.Semi-Persistent.Scheduling.in.C-V2X.Mode.4.Comm.pdf)
#### [How_many_vehicles_in_the_LTE-V2V_awareness_range_with_half_or_full_duplex_radios.pdf](https://github.com/paulsung97/Dgist_Intern_Ship/files/11725704/How_many_vehicles_in_the_LTE-V2V_awareness_range_with_half_or_full_duplex_radios.pdf)



# V2X

V2X(Vehicle-to-Everything)는 차량 간 연결 통신을 의미하며, V2X 메시지를 통해 실시간으로 속도, 위치, 방향 등의 정보를 교환합니다. 이를 통해 주행 안정성, 교통 효율, 연료 효율 등을 향상시킬 수 있습니다. V2X 메시지는 자율주행의 수준이 높아질수록 많은 센서 데이터가 들어오므로 메시지 용량도 증가합니다. 이를 해결하기 위해 엣지 컴퓨팅 기술이 사용됩니다. 엣지 컴퓨팅은 사용자 또는 데이터 소스의 물리적 위치 또는 그 근처에서 컴퓨팅을 수행하는 것을 말합니다. 엣지 컴퓨팅을 사용하면 사용자는 더 빠르고 안정적인 서비스를 받을 수 있고 기업은 유연한 하이브리드 클라우드 컴퓨팅의 이점을 얻을 수 있습니다. 엣지 컴퓨팅은 기업이 여러 위치에서 공통의 리소스 풀을 사용하여 데이터 연산 및 처리를 분산시키는 방법 중 하나입니다.

기지국(Base station, BS)은 사용자와의 연결을 위해 거점에 설치됩니다. BS를 중심으로 통신 범위가 원 형태로 설정되며, 사용자가 범위를 벗어날 경우 다음 BS와 사용자를 연결하기 위해 Handover이 이루어집니다. 그러나 통신 범위는 무한하지 않으며, 거리가 멀어질수록 파워 감소로 인해 통신이 감쇄됩니다. BS는 연결뿐만 아니라 자원 할당도 담당합니다. 동일한 자원이 동시에 할당되면 통신이 불가능한 손실(Loss)이 발생할 수 있습니다. 이러한 문제를 방지하기 위해 자원 할당은 BS에서 수행됩니다. 이러한 형태를 BS의 중앙 집중식 방식이라고 합니다. BS를 통해 자원 할당과 데이터 전송을 수행하는 방식을 Uu 인터페이스라고 합니다.

PC5 인터페이스는 sidelink 통신을 지원하며, 자원 할당 방식에 따라 mode 3과 mode 4로 나뉩니다. mode 3은 BS가 필수적이지만, mode 4는 기기들 간의 side link를 통해 통신합니다. mode 4의 경우, BS가 없어서 리소스 할당 기능이 없으므로 통신이 겹칠 가능성이 있고 통신 신뢰성이 낮아질 수 있습니다. 자동차의 수에 따라 통신 겹침의 차이가 있습니다. 자동차가 많을 경우 리소스 사용이 많아져 통신 겹칠 확률이 높아집니다. C-V2X mode 4의 통신 성능을 분석하기 위해 MATLAB 기반의 LTEV2Vsim 시뮬레이터를 사용하였습니다.
## <실험 내용>

- ptx_dBm을 각각 20, 23, 26으로 변경 후 시각화
- 메시지 크기를 100, 150, 200, 250, 300으로 변경 후 시각화
- mcs를 8, 13, 18로 변경 후 시각화

### 초기 고정값

- 시뮬레이션 시간 = 100초
- 도로 길이 = 1000m
- 도로 너비 = 5m
- 도로 차선 = 2
- 차량 수 = 100대

※ 위 내용에 따라 실험을 독립적으로 수행합니다.

## <실험 1번>

- ptx_dBm을 각각 20, 23, 26로 변경 후 시각화

### 시각화

![Untitled](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/ba739e54-0ea5-40d8-b0d1-66722ce55624)


## <결론>

위 환경에서는 ptx_dBm의 값이 23을 기준으로 3씩 증가하거나 감소할 때의 수신율을 확인한 결과입니다. ptx_dBm 값이 증가하면 송신 전력이 높아져 수신율이 높아지는 것을 알 수 있습니다.

## <실험 2번>

- 메시지 크기를 100, 150, 200, 250로 변경 후 시각화

mcs = 3, mcs = 12

### 시각화


![Untitled](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/19ce7722-35bf-4899-ba0e-774a69c3f5db)

## <결과>

위 실험을 통해 메시지 크기가 증가함에 따라 수신율이감소하는 것을 알 수 있습니다. 또한 mcs 값이 커질수록 데이터를 많이 전송할 수 있지만 통신 오류에 더 취약해질 수 있습니다. 따라서 동일한 메시지 크기를 보낼 때, mcs 값이 3인 경우에 비해 mcs 값이 12인 경우에는 통신 오류로 인해 낮은 수신율을 나타냅니다.

## <실험 3번>

mcs 값을 8, 13, 18로 변경 후 시각화

[mcs: 전송 속도 결정]

### 코드
![Untitled](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/c71a7d1f-4da5-4030-901b-104f234029a0)


### 시각화

![Untitled](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/ca1bf9d1-5fa9-413f-90b4-a7a7907223c0)


## <결과>

1. mcs = 8: 0.972200
2. mcs = 13: 0.959112
3. mcs = 18: 0.730109

메시지 크기가 300인 경우 mcs 값만 변경한 실험 결과입니다. 이 실험을 통해 한 번에 전송할 수 있는 데이터 양을 늘릴수록 수신율이 낮아짐을 확인할 수 있습니다.

따라서 고정된 환경에서 mcs 값이 8, 13, 18인 경우, mcs 값이 8일 때 가장 높은 수신율을 나타내는 것을 알 수 있습니다.

# Yolov7 모델을 이용한 해상도 채널 상태에 따른 mAP, Latency 평가

![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/4ed42054-6ee9-46f6-b0d6-6a2922d4c190)
<br>
<br>
학습 모델의 정확도 평가를 확인해 보겠습니다. 전체적으로 Recall 값은 0.65, Precision 값은 0.75, mAP@0.5는 0.72, mAP@0.5:0.95는 0.42라는 결과가 나왔습니다.
<br>
<br>

![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/8a99273a-a38d-40f9-923d-4023cae47647)
<br>
<br>
"metrics/recall" 그래프는 재현율 그래프입니다. 재현율은 이미지 대상 전체 중 모델이 예측한 대상의 비율을 나타냅니다. 즉, 전체 대상에 대해 탐지를 해낸 값을 그래프로 표현한 것입니다. 그래프를 보면 꾸준히 증가하는 형태로 모델이 잘 탐지한 것을 확인할 수 있습니다. True Positive(TP)는 모델이 잘 탐지한 개수이며, False Negative(FN)는 모델이 놓친 개수로, FN은 낮고 TP는 높은 값을 가지고 있습니다. 이 모델의 탐지율은 약 65% 정도라고 할 수 있습니다.
<br>
<br>


![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/462087ab-dc42-4b65-a054-6f0138a8c34c)
<br>
<br>
"metrics/precision" 그래프는 정밀도 그래프입니다. 이 그래프는 모델이 탐지한 대상 중에서 실제로 제대로 탐지한 비율을 나타냅니다. 이 그래프를 통해 모델이 얼마나 정확하게 탐지했는지에 대한 비율을 확인할 수 있습니다. 이 모델의 정밀도는 약 75% 정도라고 할 수 있습니다. 
recall과 precision 그래프를 통해 물체를 탐지할 확률은 65% 정도이며, 탐지한 물체를 제대로 인식할 확률은 75% 정도인 것을 알 수 있습니다.
<br>
<br>


![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/e25735f7-bc0e-4057-bd81-403b68d649ef)
<br>
<br>
"metrics/mAP" 값과 "metrics/precision" 값을 적분한 값을 기반으로 전체적인 정확도를 나타내는 mAP 정확도에 대해 알아보겠습니다. 
먼저 "metrics/mAP@0.5"에 대해 알아보겠습니다. 이 그래프는 IoU (Intersection over Union) 값이 0.5인 경우의 mAP를 나타냅니다. 이는 객체를 50%만 잡아도 정답으로 인정하는 정확도를 의미합니다. 해당 그래프를 통해 전체적인 흐름을 빠르게 확인할 수 있으며, 약 72%의 정확도로 객체를 탐지할 수 있음을 알 수 있습니다.
<br>
<br>

![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/7427c4cf-a855-4327-aa19-7546e1513894)
<br>
<br>
정확도를 가장 자세히 표현한 metrics/mAP 0.5:0.95에 대해 확인하겠습니다. 이 그래프는 분자 영역에 색칠 돼 있는 부분이 0.5부터 0.95 사잇값을 1%에서 100%로 수치화시켜 처리한 그래프를 의미합니다. 이 그래프 또한 증가하는 양상을 보이지만, 정확도 면에서 metrics/mAP 0.5에 비해 모델은 탐지율이 42% 정도의 성능을 보여주고 있다는 것을 확인할 수 있었습니다.
<br>
<br>
![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/3c3bcc58-4062-4b4c-b355-5b2ea9210bd5)
<br>
<br>
제작한 모델을 통해 10,000개의 Test 이미지 데이터셋을 활용해 측정을 진행 하였습니다. 실험은 총 2개를 진행하였고, 먼저 첫 번째 실험은 이미지 크기에 따른 mAP값에 차이를 확인하였으며 이미지는 1280x720 ~ 320x180 크기까지 총 7가지 크기에 따른 mAP값을 측정하였습니다. 
다음 실험은 해상도 채널 상태에 따른 mAP 값 및 레이턴시를 측정하였습니다. 이는 1280x720 사진을 기준으로 두었으며, 40~100m 까지 의 거리에 따른 해상도 채널 상태의 변화를 측정해 보았습니다.
<br>
<br> 
![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/64b09f3c-2dc5-4ebc-bd78-e1892caba1e8)
<br>
<br>
첫 번째 실험인 이미지 크기에 따른 mAP값의 차이를 확인하는 그래프입니다. 이미지의 사이즈가 클수록 정확한 이미지를 담고 있기에 탐지율이 높은 것을 알 수 있었습니다.
<br>
<br>
![image](https://github.com/paulsung97/Dgist_Intern_Ship/assets/63456050/220fd2f3-d00e-47b4-8177-0e310860ad04)
<br>
<br>
100m의 거리에 따른 Test 이미지셋을 모델이 탐지하는 장면입니다. mAP 0.179 값을 도출하는 과정의 장면이며, 보시는 그림 1번 사진은 실제 위치에 존재하는 것에 대한 label 데이터 이며 그림 2번 사진은 모델이 직접 예측한 이미지입니다.
<br>
<br>
