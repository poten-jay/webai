# 딥러닝
---

커리큘럼 : https://docs.google.com/spreadsheets/d/1hfR1UXSYW_krYgVU4FFWBP38BOib88bZxRjCVHmgRkU/edit#gid=90564784

동영상 강의: https://opentutorials.org/course/4570

슬라이드: https://docs.google.com/presentation/d/1U1vitklSoXVFDckVM9AoB010Qsnk78dXqJNpXTHLFGU/edit#slide=id.g882dfa8ce9_0_253

노트북: https://colab.research.google.com/drive/105U4KoMN7fPB2FwxFFa119AP_5jaVyx4#scrollTo=9iCV80vrjMy_

핑 : https://docs.google.com/spreadsheets/d/1xKkYtre7_xBOXXDBDkRPQLoRZvcHWGD5ZBEbmZH7Acs/edit#gid=337704553

---

## 분류와 회귀문제를 푸는 알고리즘

Decision tree 

Random Forest

KNN

SVM

Nural Network <= 딥러닝

---

Nural Network (인공 신경망) 

1950년대 등장 -> 외면 -> 80년대 주목 -> 외면 -> 다시금 주목

---

머신러닝 : 컴퓨터가 스스로 계획하고 답을 찾음

프로그래밍 : 사람이 계획하고 만들어 냄

---

## 지도학습의 빅비쳐

1. 과거의 데이터를 준비한다.
2. 모델의 구조를 만든다.
3. 데이터로 모델을 학습(FIT)합니다.
4. 모델을 이용합니다.

---
< model.ipynb >

### 표를 다루는 도구 Pandas

### 레모네드 판매 예측

### 보스턴 집값 예측

### 학습의 실제

### 아이이스 품종 분류

---

## 신경망의 완성 : 히든레이어

input layer -> hidden layer -> output layer  
  x1 - x13  ->   h1 - h5    ->     y  
       (13 * 5 = 65)       (5 * 1)     => 70 번의 계산

h1 = w1 * x1 + w2 * x2 .... w13 * x13 + b   => 의 히든 레이어 수식

y = w1 * h1 + w2 * h2 .... w5 * h5 + b => 의 y 레이어 수식

따라서 이는 연쇄적인 하나의 거대한 신경망이 된다.

### 실습

< model.ipynb >

---


---

---

활성화 함수 (Activation)








