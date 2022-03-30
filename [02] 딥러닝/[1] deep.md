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

---

### 레모네드 판매 예측

```python
# 모델 구성
X = tf.keras.Input(shape=[1])
Y = tf.keras.layers.Dense(1)(X)
model = tf.keras.Model(X, Y)
model.compile(loss='mse')
```
하나의 뉴런을 표현한 코드 (가장 기본이자 핵심)

shape=[1] 과 Dense(1) 을 이해하면 된다.

독립변수가 1 이므로 shape 이 1, 종속변수가 1 이므로 Dense 가 1.

```python
# 모델 학습(fit)
model.fit(독립, 종속, epochs=1000)
```
epochs=1000 은 1000번을 학습

---

### 손실의 의미 (Loss)

```python
# 모델 학습(fit)
model.fit(독립, 종속, epochs=10)
```
위 코드를 실행하면

Epoch 1/10
1/1 [==============================] - 0s 4ms/step - loss: 2548.6941
Epoch 2/10
1/1 [==============================] - 0s 4ms/step - loss: 2452.2352
Epoch 3/10
1/1 [==============================] - 0s 3ms/step - loss: 2332.4521
Epoch 4/10
1/1 [==============================] - 0s 3ms/step - loss: 2256.9451
Epoch 5/10
1/1 [==============================] - 0s 2ms/step - loss: 2139.0323
Epoch 6/10
1/1 [==============================] - 0s 2ms/step - loss: 2001.8462
Epoch 7/10
1/1 [==============================] - 0s 2ms/step - loss: 1951.3548
Epoch 8/10
1/1 [==============================] - 0s 3ms/step - loss: 1842.3458
Epoch 9/10
1/1 [==============================] - 0s 4ms/step - loss: 1752.8543
Epoch 10/10
1/1 [==============================] - 0s 3ms/step - loss: 1611.1125

출력이 나오게 된다. 10번의 학습 동안 로스율이 줄어들게 된다.

loss : 학습이 미쳤을때, 얼마나 정답에 가까원 지는지 보여준다. 

-> 모델을 구성해서 나온 값을 종속변수(원래 값) 과 비교하여 나타낸 값

-> (예측 - 결과)^2 : loss (Error^2 : square error) 

-> 평균이 0 에 가까워 질때 까지 반복 학습 (mse : meen square error)  
   (mse 는 분산과 모양이 비슷)

- loss 값이 0에 가까워진다 : 모든 예측값이 실제 값과 비슷해 진다.  
- 따라서 모델학습은 '최적화' 라고도 한다.
- 회귀모델이서 mse를 지표로 사용

---

### 레모네드 판매 예측 (실습)
< model.ipynb >

1. 라이브러리 로딩
2. 데이터 준비
3. 모델 준비
4. 모델에 데이터 학습
5. 모델 이용

---

### 보스턴 집값 예측

---

### 수식과 퍼셉트론 (보스턴 집값 기준)

```python
X = Input(shape=[13])
Y = Dense(1)(X)
model = Model(X, Y)
model.compile(loss='mse')
```
13개의 종속변수 (shape=[13]) 와 1개의 독립변수 (Dense(1)) 이므로,

y = W1X1 + W2X2 + W3X3 + ... + W13X13 + b   로 표현이 가능하다.

여기서 b 는 편향을 의미 : 편향(bias) : 종속변수가 전부다 0 일때, 디폴트로 가지는 값  
다시말해, 집이 종속변수들에 아무 해당이 안되어도 지값은 디폴트로 b 만금 가격이 나온다.

---

만약 종속변수가 12개, 독립변수가 2개라면 코드작성은 다음과 같다.

```python
X = Input(shape=[12])
Y = Dense(2)(X)
model = Model(X, Y)
model.compile(loss='mse')
```

이때는, 2개의 퍼셉트론이 병렬로 연결된 모습을 가진다.

y1 = W1X1 + W2X2 + W3X3 + ... + W12X12 + b  
y2 = W1X1 + W2X2 + W3X3 + ... + W12X12 + b

독립변수가 2개가 되면, 찾아야 하는 값은 y1의 w값 12개 와 bias + y2의 w값 12개 와 bias = 총 26개의 값을 찾아야 한다. (두 수식은 완전히 독립적이다.)

b의 초기값 생성은 데이터가 복잡해 진다면 지정해 줘야 한다. (현재는 랜덤으로 정해진다.)

---

### 보스턴 집값 예측 (실습)

---

### 학습의 실제

---

### 아이리스 품종 분류

setosa, virginica, verbosa 3종류에 대한 식 (원핫 인코딩을 해서 0, 1로 표현됨)

y1 = W1X1 + W2X2 + W3X3 + W4X4 + b
y2 = W1X1 + W2X2 + W3X3 + W4X4 + b
y3 = W1X1 + W2X2 + W3X3 + W4X4 + b

---

### 원핫인코딩 (범주형 변수 사용시 해줘야함)

범주형 데이터를 식에서 사용할 수 있도록 0, 1 로 표현하는 컬럼을 새로 만들어 사용

```python
# 원핫인코딩 (범주형 변수를 자동으로 원핫인코딩 해줌)
아이리스 = pd.get_dummies(아이리스)
```
---

### softmax (활성화 함수 : (Activation))

필요 이유 : 분류 예측을 위해 softmax 나 sigmoid 를 사용한다.  
분류를 확률로 표현하기 위한 수식 (추후 자세히 배움)

3개의 식이 있지만, 이는 -문한대 ~ +무한대 사이의 값을 가진다. 따라서 활성화 함수로 보정해 준다.

y1 = softmax(W1X1 + W2X2 + W3X3 + W4X4 + b)
y2 = softmax(W1X1 + W2X2 + W3X3 + W4X4 + b)
y3 = softmax(W1X1 + W2X2 + W3X3 + W4X4 + b)

softmax 를 통해 0과 1사이에 값으로 보정한다.

분류모델은 : logistic regression

* loss
- 분류 : crossentropy
- 회귀 : mse

---

### 신경망의 완성 : 히든레이어

input layer -> hidden layer -> output layer  
x1 - x13    ->   h1 - h5    ->     y  
필요수식: (14 * 5 = 70)    (6 * 1)     => 76 개의 수식 필요 (bias 포함)

h1 = w1 * x1 + w2 * x2 .... w13 * x13 + b   => 의 히든 레이어 수식

y = w1 * h1 + w2 * h2 .... w5 * h5 + b => 의 y 레이어 수식

따라서 이는 연쇄적인 하나의 거대한 신경망이 된다.

---

### 실습

< model.ipynb >

---

## 추가 학습

### ex) 부동산 구매

변수 => 가격  |  도시  |  역세권  |  평수  |  마당  |  년수  등등..  

히든 => 향후상승 가능성  |  피  |  학군 ... 등  : 3개

히든레이어의 변수들은 사람은 이해가 가능하다. 하지만, 컴퓨터는 특징을 찾아 내지만 이를 사람이 해석하기 힘들다. 사람은 단지 3개의 새로운 특징을 찾아라고 컴퓨터에 명령한다.  

이는 모델이 직접 특징을 찾는다. : 딥러닝 -> 특징 자동 추출기

- 특징 찾기 : 전통적인 머신러닝은 사람이 선택하고, 조합해서 새로운 특징을 사람이 직접 함 (비지도 학습 등) => feature engineering 

- 특징 차기 : 딥러닝은 결과를 가장 잘 설명할 수 있는 특징들을 찾아낸다. (사람이 찾아내는 특징보다 훨신 더 잘 찾아내게 된다.)

---

### 특징공학

|x|y|
|-|-|
|1|1|
|2|4|
|3|9|
|4|16|

라면, 이는 y= Wx + b  이다.

다만, y = (2 + x)^2 + 8 를 설명하려 한다면,

|x|y|
|-|-|
|1|17|
|2|24|
|3|33|
|4|44|

로 표현되어 규칙성을 잃어버린다. 이런경우 새로운 피쳐(특징)를 추가해서 선형모델을 만든다.


|x^2|x|y|
|-|-|-|
|1|1|...|
|4|2|...|
|9|3|...|
|16|4|...|

x^2 와 x 를 입력으로 하는 선형을 만들어 내는 것이다.  
y = W1x^2 + W2x + b

머신러닝에서는 이러한 피쳐의 추가를 사람이 해야 하지만, 딥러닝에서는 깊게 쌓으면 모델이 특징을 찾아낸다.


---









