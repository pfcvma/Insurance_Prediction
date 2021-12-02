# Insurance_Prediction


##### 딥러닝을 통한 보험 시뮬레이션 : 손해율과 손해율의 변동성을 최소화

##### 1) 농산물의 가격 데이터 수집
>농산물 유통정보 KAMIS에서 현행 농작물 포함 32종류 농산물에 대해 총 21년(2000~2020)간의 가격 데이터를 수집

##### 2) 농산물 가격 데이터 기반 딥러닝
>* Feature Engineering : 과거 5개월 간의 데이터를 바탕으로 다음 달 가격을 예측
>
>* LSTM : RNN 모델의 장기 의존성 문제를 보완한 모델로 장기 기억, 단기 기억이 가능

##### 3) 딥러닝으로 도출된 가격 그래프 (고구마, 양파 등)
>2017년 이전의 데이터를 기준으로 딥러닝을 수행한 뒤 2017년 이후의 가격 데이터를 산출
>
>* 회귀분석 : 예측값과 실제값을 0~1까지의 분포로 정규화한 값의 차이인 MSE 값 = 0.001

##### 손해율과 손해율의 변동성 개선
>* 시계열 군집화(DTW) 알고리즘 : 가격 변동이 유사한 작물들끼리 군집화(예: 가장 유사한 가격 그래프를 나타낸 ‘녹두+들깨’ 묶음을 프로그램이 발견하여 분류)한 뒤 가격 변동이 반대의 움직임을 보이는 군집끼리 묶어 변동성을 상쇄하면 32품목을 모두 동시에 포함하는 것보다 더 낮은 변동성과 손해율을 도출

