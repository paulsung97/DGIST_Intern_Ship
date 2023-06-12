# Dgist_Intern_Ship

**활동:** 2022.12.26-2023.01.31

**연구실:** Department of Electrical Engineering and Computer Science, Communication and Signal Processing Laboratory

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

- ptx_dBm을 각각 17, 23, 29로 변경 후 시각화

### 코드

### 시각화

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/78bc4cda-c50d-4ff7-a4f5-526a07d86235/Untitled.png)

## <결론>

위 환경에서는 ptx_dBm의 값이 23을 기준으로 3씩 증가하거나 감소할 때의 수신율을 확인한 결과입니다. ptx_dBm 값이 증가하면 송신 전력이 높아져 수신율이 높아지는 것을 알 수 있습니다.

## <실험 2번>

- 메시지 크기를 100, 150, 200, 250로 변경 후 시각화

mcs = 3, mcs = 12

### 코드

### 시각화

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1a8c3d17-79d2-4678-b4fc-4d2a39d76097/Untitled.png)

## <결과>

위 실험을 통해 메시지 크기가 증가함에 따라 수신율이감소하는 것을 알 수 있습니다. 또한 mcs 값이 커질수록 데이터를 많이 전송할 수 있지만 통신 오류에 더 취약해질 수 있습니다. 따라서 동일한 메시지 크기를 보낼 때, mcs 값이 3인 경우에 비해 mcs 값이 12인 경우에는 통신 오류로 인해 낮은 수신율을 나타냅니다.

## <실험 3번>

mcs 값을 8, 13, 18로 변경 후 시각화

[mcs: 전송 속도 결정]

### 코드

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2e45718f-a829-4c85-89eb-dc959fcf23f5/Untitled.png)

**- mcs = 8**

**- mcs = 13**

**- mcs = 18**

### 시각화

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2866c9cc-0910-4ff4-b25a-3461b1e7e8dc/Untitled.png)

## <결과>

1. mcs = 8: 0.972200
2. mcs = 13: 0.959112
3. mcs = 18: 0.730109

메시지 크기가 300인 경우 mcs 값만 변경한 실험 결과입니다. 이 실험을 통해 한 번에 전송할 수 있는 데이터 양을 늘릴수록 수신율이 낮아짐을 확인할 수 있습니다.

따라서 고정된 환경에서 mcs 값이 8, 13, 18인 경우, mcs 값이 8일 때 가장 높은 수신율을 나타내는 것을 알 수 있습니다.
