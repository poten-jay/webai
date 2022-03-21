# webai

---

22-03-17 
[1]

머신러닝 입문


핑 : https://docs.google.com/spreadsheets/d/1xKkYtre7_xBOXXDBDkRPQLoRZvcHWGD5ZBEbmZH7Acs/edit#gid=337704553

지식지도 : https://seomal.com/map/1

생활코딩 인강 : https://opentutorials.org/course/4548

커리큘럼 : docs.google.com/spreadsheets/d/1hfR1UXSYW_krYgVU4FFWBP38BOib88bZxRjCVHmgRkU/edit#gid=90564784

Teachable Machine : https://teachablemachine.withgoogle.com/

---

[2]

f12 - console - speechSynthesis.speak(new SpeechSynthesisUtterance(''));  

 '  '  안에 글을 넣으면 음성 지원됨

시각화 도구 -> 표, 좌표평면

[표] 

아무리 복잡한 데이터라도 일단 표 안에 속박시킬 수 있다면, 단정하게 정리 정돈할 수 있습니다.
표를 옮겨담으면 컴퓨터가 가진 엄청난 저장 용량과 처리 속도를 이용해서 강력한 표 로봇을 만들 수 있다.

열 ^ column : 특성 (featrure), 속성(atribute), 변수(variable), field  
행 > row : 개채 (instance), 관측치(observed value), 기록(record), 사례(example), 경우(case)

---
[변수] variable

독립변수 : 원인이 되는 열

종속변수 : 결과가 되는 열

ex)
x = 1  
x = 2 => x 는 설정하기에 따라 변한다. x 는 변수라 한다.

column : 날짜, 요일, 온도, 판매량  
 -> 일때, 온도는 판매량기준 독립변수 (원인) 이고, 판매량은 종속변수(경과)
 
---
[상관관계]  
한쪽의 값이 바뀌었을 때, 다른 쪽의 값도 바뀐다면, 두 개의 특성은 ‘서로 관련이 있다’고 추측  
 ( 온도와 판매량은 상관관계가 있다.)

[인과관계]  
 ‘온도’는 ‘원인’이고, ‘판매량’은 ‘결과’

다만, 상관관계 > 인과관계 (상관관계가 인과관계를 포함한다.  
(모든 인과관계는 상관관계이다.but 모든 상관관계는 이과관계가 아니다.)

---
[머신러닝 (machine learning) (기계학습)]

지도학습 (supervised learning) : 분류, 회귀  
 -> 정답이 있는 문제를 해결 (데이터로 컴퓨터를 학습시켜서 모델을 만드는 방식)

비지도학습 (unsupervised learning) : 군집화, 변환, 연관  
 -> 무언가에 대한 관찰을 통해 새로운 의미나 관계를 밝혀내는 것 (데이터의 성격을 파악하거나 데이터를
잘 정리정돈 하는 것에 주로 사용)

강화학습 (reinforcement learning) : 더 좋은답 찾아가기  
 -> 더 좋은 보상을 받기 위한 수련 (경험을 통해 “더 좋은 답”을 찾아가는 것)

---

[지도학습 ]

지도학습 = 역사

과거에 있었던 사건이 원인과 결과로 기록되었다면, 역사를 알면 사건이 일어났을 때, 그 결과로 예측

 -> 과거의 데이터로부터 학습해서 결과를 예측하는 데에 주로 사용  
 -> 과거 데이터로 훈련해 모델을 만들다.


* 학습  
지도학습을 하기 위해서는 우선 과거의 데이터가 있어야 합니다.  
그리고 그 데이터를 독립변수(원인)와 종속변수(결과)로 분리해야 합니다.

만들어진 모델을 => 공식 이라고 하면,

머신러닝은 => 공식의 대중화

---
2022-03-18

[지도학습] - [회귀]  
          - [분류]

---

[회귀 (regression)]  -> 예측하고 싶을때.

예측하고 싶은 결과가 숫자라면 => 지도학습의 회귀로 해결

* 사례  
독립변수        종속변수            학습시킬 데이터 만드는 방법  

공부시간        시험점수            사람들의 공부시간을 입력받고 점수를 확인한다.  
온도            레모네이드 판매량   온도와 그날의 판매량을 기록한다.  
역세권, 조망    집 값               집과 역까지의 거리, 수치화된 조망 평점, 집 값  
온실 기체량     기온 변화량         과거에 배출된 온실 기체량과 기온의 변화량을 기록한다  
자동차 속도     충돌시 사망률       충돌시 속도와 사상자를 기록한다  
나이            키                 학생들의 나이에 따른 키를 기록한다  

"가지고 있는 데이터에 독립변수와 종속변수가 있고, 종속변수가 숫자일 때 회귀를 이용한다."

---

[분류 (classification)]

추측하고 싶은 결과가 문자나 이름이라면 => 지도학습의 분류로 해결

* 사례  
독립변수        종속변수            학습시킬 데이터 만드는 방법  

공부시간        합불                사람들의 공부시간 + 합불여부
x-ray 종량 크기 악성종양 여부        의학적 양성, 음성이 확인된 사진과 영상데이터 수집
품종, 산도, 연도 와인의 등급         소믈리에를 통해 확인된 와인등급과 품종, 산도 등

"가지고 있는 데이터에 독립변수와 종속변수가 있고, 종속변수가 이름일 때 분류를 이용한다."

---

[양적데이터] - ‘양적(量的, Quantitative)'  
 - 면적, 온도, 판매량 등  
 - 종속변수가 양적 데이터라면 회귀


[범주형데이터] - ‘범주(範疇, Categorical)'  
 - 계절, 날씨, 휴가지 등  
 - 종속변수가 범주형 데이터라면 분류

---

[비지도학습] - [군집화]  
            - [연관규칙학습]
            - [비지도 학습 정리]

---

[군집화 (clustering)]

비슷한 것들끼리 모아서 적당한 그룹을 만들 것입니다. 이렇게 그룹을 만드는 것이 군집화

어떤 대상들을 구분해서 그룹을 만드는 것이 군집화라면, 분류는 어떤 대상이 어떤 그룹에 속하는지를 판단.

ex) 1000만명의 회원의 배달사업 - 100개의 배달본부를 전국에 만드려고 한다.  
    적절히 분포되어 있는 100개의 그룹을 만들어야 한다.  
    이때, 숫자나 표를 보고 군집화 하는 것은 쉽지 않다.  

    100개의 cluster + 1000만 관측 => 군집화 => 100개 cluster  

군집화 => 서로 가까운 관측치를 찾아주는 기법 (비슷한 행(관측치)을 그룹핑)

---

[연관규칙학습 (Association rule learing)]

 - 서로 연관된 특징을 찾아내는 것 (장바구니 학습)

ex) 라면을 구입한 사람은 계란을 구입할 확률이 높다.  
    즉, 라면과 계란은 서로 연관성이 높다.

이 연관성을 파악하면, 고객이 미처 구입하지 못했지만, 구입할 가능성이 높은 상품 추천

연관규칙 => 서로 연관있는 데이터를 찾아주는 기법 (비슷한 열(특성)을 그룹핑)

---

[비지도학습]

비지도      탐험            변수 | 변수 | 변수  
지도학습    역사            독립변수 | 종속변수

비지도학습은 탐험적 : 독립변수와 종속변수의 구분이 중요하지 않습니다.  
지도학습은 역사적 : 원인과 결과를 바탕으로 결과를 모르는 원인이 발생했을 때, 원인인 독립변수와 결과인 종속변수가 꼭 필요

---

[강화학습 (reinforcement learning)]

지도학습    - 배움 (배움을 통해서 실력을 키우는 것)  
강화학습    - 경험 (경험을 통해서 실력을 키워가는 것)

ex) 게이머의 강화학습  
  1. 우선 게임은 게이머에게 현재의 상태를 보여줍니다. 캐릭터는 어디에 있고, 장애물은 어디에 있는지 알려줍니다.  
  2. 동시에 현재의 점수도 알려줍니다. 게이머는 이 값이 높아지는 것이 상이고, 장애물에 부딪히는 것이 벌입니다.  
  3. 관찰의 결과에 따라서 어떤 상태에서 어떻게 행동해야 더 많은 상을 받고, 더 적은 벌을 받을 수 있는지를 알게 됩니다.  
  4. 즉, 판단력이 강화된 것입니다.  
  5. 판단에 따라서 행동을 합니다.  
  6. 그 행동은 게임에 변화를 주게 됩니다.

과정을 강화학습에서 사용하는 용어로만 바꾸면

 - 게임 => 환경(environment)  
 - 게이머 => 에이전트(agent)  
 - 게임화면 => 상태(state)  
 - 게이머의 조작 => 행동(action)  
 - 상과 벌 => 보상(reward)  
 - 게이머의 판단력 => 정책(policy)

강화학습에서는 더 많은 보상을 받을 수 있는 정책을 만드는 것이 핵심

강화학습으로 자동차의 주차 능력을 훈련 : 처음에는 계속 사고를 치다가 나중에는 사고 없이 정확하게 주차에 성공하는 것

---

[통계 시각화]

평균 (mean) : 모든값 / 값을 갯수
중앙값 (median) : 갯수를 세어 중앙에 있는 값
최빈값 ()

---

[사분위수 (Quartile)]

[boxplot] (https://youtu.be/GndrnY42IkE)


    |---------------[         |        ]---------------|
최소값                                               최대값
                  1분위      2분위     3분위          

---

[산점도 (scatter plot)]

어떤 분포를 가지는지 알 수 있다.  
outlier 를 알 수 있다.  

---

22-03-21

Orange3 -sample example - data  
https://docs.google.com/spreadsheets/d/118Nln_zAaFKP8E2fxmqQmEWDmo1goLUzTQrIFS6or1Y/edit#gid=0

Orange3 -sample example - prediction  
https://docs.google.com/spreadsheets/d/1pCRcLrA4JPD4GxQgUz5nnf85CVBOfvGBZM6xYKYeEDY/edit#gid=0

boston housing price  
https://docs.google.com/spreadsheets/d/12aiC80s5SN-_8jI6PkBJSDRLO2GayzyjQCAkHPCbTJM/edit#gid=905700562

IRIS dataset  
https://docs.google.com/spreadsheets/d/1FqgxczfjFmO6EVVbyyfFzs9XEsfAzazN3qcedY46xWI/edit#gid=864120505

Comparing Supervised Learning Algorithms - KR  
https://docs.google.com/spreadsheets/d/1maZvvWro6CYVAsS3Sf8tapFW1b2sZOgldoiSK5D8xlU/edit#gid=0

---

오랜지3 이용하여 codiv 분석

https://orangedatamining.com/blog/2020/2020-04-02-covid-19-basic/

https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv


---





