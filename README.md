# TSA_Practice

본 프로젝트는 FASTCAMPUS 강의 "파이썬을활용한시계열데이터분석A-Z올인원패키지 Online"을 통해 학습한 내용을 추후에 손쉽게 활용할 수 있도록 정리하고 실습하는 프로젝트이다.
개발 환경은 Colab을 활용한다.

--------------------------------

## 1. create_time_feature

시계열 데이터 특성을 활용하여 이미 가진 feature에서 시계열 패턴을 추출하는 코드 상세이다.  
해당 파일의 '0.Result Code' 셀을 활용하면 다음과 같은 시계열 패턴을 추출하여 feature로 추가할 수 있다.  

- **index를 시계열 데이터에 맞추어 세팅**
- **count_trend** : 타겟 데이터인 count의 Trend 패턴을 추출하여 추가한 feature
- **count_seasonal** : 타겟 데이터인 count의 Seasonal 패턴을 추출하여 추가한 feature
- **count_Day** : 타겟 데이터인 count의 1일 기준 이동평균을 구하여 추가한 feature
- **count_Week** : 타겟 데이터인 count의 7일 기준 이동평균 구하여 추가한 feature
- **count_diff** : 타겟 데이터인 count를 차분하여 랜덤워크 데이터에서 분석에 용이한 패턴을 추출한 feature
- **temp_group** : 구간을 나누어 활용할 수 있는 temp와 같은 데이터를 cut을 통해 구간으로 나누어 활용할 수 있는 feature
- **Year** : 해당 데이터의 연도
- **Quater** : 해당 데이터의 분기
- **Quater_ver2** : 해당 데이터의 시작연도부터 시작된 누적 분기값
- **Month** : 해당 데이터의 월
- **Day** : 해당 데이터의 일자
- **Hour** : 해당 데이터의 시간
- **DayofWeek** : 해당 데이터의 요일
- **count_lag1** : 타겟 데이터인 count를 shift하여 한 시점 이전의 count값
- **count_lag2** : 타겟 데이터인 count를 shift하여 두 시점 이전의 count값
- **Quater_Dummy#** : 카테고리 데이터를 활용하기 위해 get_dummies를 통해 onehot incoding을 수행한 feature

--------------------------------------

## 2. check_features_visually

시계열 데이터가 가지고있는 기존 feature들과 feature engineering을 통해 얻어진 feature들을 함께 활용하여 시각화 하고 이를 통해 데이터가 가진 특성을 이해할 수 있다. 

해당 실습 파일에서는 몇 가지의 feature들 만으로 scatter plot, box plot, cross table, correlation 등의 시각화를 진행하였지만  
실제 분석을 할 때는 되도록 충분히 많은 feature들의 조합을 확인하여 데이터에 대한 insight를 얻어내는 것이 중요하다.  

-----------------------------------

## 3. Evaluation_and_ErrorAnalysis_with_BaseModel

모델링에 대한 부분은 차후에 자세히 보기로하고 우선 간단한 모델이 예측한 결과 분석 방법을 알아본다.

### Evaluation part에는 간단하게 다음과 같은 내용이 있다.
- MAE, MSE, MAPE 등의 일반적인 지표를 활용하여 성능을 확인할 수 있.
- 상황에 따라 다른 지표들을 알아보고 활용할 수 있다.

### ErrorAnalysis part에는 다음과 같은 내용이 있다.
ErrorAnalysis를 통해 모델의 개선점이 있는지 확인할 수 있다.
ErrorAnalysis로 알아볼 수 있는 항목으로는 **정상성, 정규성, 자기상관, 등분산성**이 있으며
Error가 정상성을 가지고 정규성을 가지며 자기상관이 없고 등분산성을 가지도록 하는 모델이 이상적이라고 볼 수 있다.
