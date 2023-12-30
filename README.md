# Insurance_Prediction

##### <  한국보험신문, 일본보험매일신문, 중국은행보험보 주최 보험산업 발전을 위한 2021 대학생 아이디어 공모전 - 한국보험신문사장상 수상작 : 딥러닝을 활용한 ‘농민의 웃음을 되찾다 : 풍년보험 상품제안’ >
> 분석 코드: 본 Repository 참고
>
> 발표자료: [농민의 웃음을 되찾다 : 풍년보험 상품제안](https://drive.google.com/file/d/1y1-0T1Na9l9fSXNgPSgsRLgc5an6mids/view?usp=sharing)

<br>


#### Deep Learning-Based Insurance Product Loss Ratio Prediction Simulation(Modern Portfolio Theory Implementation): 현대 포트폴리오 이론을 기반으로 다양한 자산 간 상관 관계를 고려한 보험 포트폴리오를 구성

##### 목적 : 손해율과 손해율의 변동성을 예측하고 두 값을 최소화하기 위함.

##### 1) 농산물의 가격 데이터 수집
>농산물 유통정보 KAMIS에서 현행 농작물 포함 32종류 농산물에 대해 총 21년(2000~2020)간의 가격 데이터를 수집

##### 2) 농산물 가격 데이터 기반 딥러닝
>* Feature Engineering : 과거 5개월 간의 데이터를 바탕으로 다음 달 가격을 예측
>
>* LSTM : RNN 모델의 장기 의존성 문제를 보완한 모델로 장기 기억, 단기 기억이 가능

##### 3) Deep Learning으로 도출된 가격 그래프 (고구마, 양파 등)
>2017년 이전의 데이터를 기준으로 Deep Learning을 수행한 뒤 2017년 이후의 가격 데이터를 산출
>
>* 회귀분석 : 예측값과 실제값을 0~1까지의 분포로 정규화한 값의 차이인 MSE 값 = 0.001

##### 4) 손해율과 손해율의 변동성 개선
>* 시계열 군집화(DTW) 알고리즘 : 가격 변동이 유사한 작물들끼리 군집화(예: 가장 유사한 가격 그래프를 나타낸 ‘녹두+들깨’ 묶음을 프로그램이 발견하여 분류)한 뒤 가격 변동이 반대의 움직임을 보이는 군집끼리 묶어 변동성을 상쇄하면 32품목을 모두 동시에 포함하는 것보다 더 낮은 변동성과 손해율을 도출

