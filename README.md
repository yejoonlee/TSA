# TSA_Practice

본 프로젝트는 FASTCAMPUS 강의 "파이썬을활용한시계열데이터분석A-Z올인원패키지 Online"을 통해 학습한 내용을 추후에 손쉽게 활용할 수 있도록 정리하고 실습하는 프로젝트이다.
개발 환경은 Colab을 활용한다.

==============================

## 1. create_time_feature

시계열 데이터 특성을 활용하여 이미 가진 feature에서 시계열 패턴을 추출하는 코드 상세이다.
해당 파일의 '0.Result Code' 셀을 활용하면 다음과 같은 시계열 패턴을 추출하여 feature로 추가할 수 있다.

- index를 시계열 데이터에 맞추어 세팅
- count_trend : 타겟 데이터인 count의 Trend 패턴을 추출하여 추가한 feature
- count_seasonal : 타겟 데이터인 count의 Seasonal 패턴을 추출하여 추가한 feature
- count_Day : 타겟 데이터인 count의 1일 기준 이동평균을 구하여 추가한 feature
- count_Week : 타겟 데이터인 count의 7일 기준 이동평균 구하여 추가한 feature
- count_diff : 타겟 데이터인 count를 차분하여 랜덤워크 데이터에서 분석에 용이한 패턴을 추출한 feature
- temp_group : 구간을 나누어 활용할 수 있는 temp와 같은 데이터를 cut을 통해 구간으로 나누어 활용할 수 있는 feature
- Year : 해당 데이터의 연도
- Quater : 해당 데이터의 분기
- Quater_ver2 : 해당 데이터의 시작연도부터 시작된 누적 분기값
- Month : 해당 데이터의 월
- Day : 해당 데이터의 일자
- Hour : 해당 데이터의 시간
- DayofWeek : 해당 데이터의 요일
- count_lag1 : 타겟 데이터인 count를 shift하여 한 시점 이전의 count값
- count_lag2 : 타겟 데이터인 count를 shift하여 두 시점 이전의 count값
- Quater_Dummy# : 카테고리 데이터를 활용하기 위해 get_dummies를 통해 onehot incoding을 수행한 feature
