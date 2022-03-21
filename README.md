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


