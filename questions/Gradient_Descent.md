---
layout: default
title: "Gradient Descent"
---

# 📌 경사하강법 (Gradient Descent)

최적화하고자 하는 함수 \( J(\theta) \)가 주어졌을 때, 그 함수의 기울기(Gradient, \( \nabla J(\theta) \))를 이용해 변수를 조정하여 최소값을 찾는 과정입니다.

## 📌 경사하강법 공식

\[
\theta := \theta - \alpha \nabla J(\theta)
\]

- **θ:** 학습할 파라미터 (weight, bias)
- **α:** Learning rate
- **\( \nabla J(\theta) \):** 손실 함수의 기울기 (Gradient)

---

## 📘 경사하강법은 언제 사용되는가?

최적화가 필요한 **모든 머신러닝 및 딥러닝 모델**에서 사용됩니다.

- **선형회귀 & 로지스틱 회귀:** 가중치를 최적화하여 비용함수를 최소화할 때.
- **신경망 학습 (Deep Learning):** 역전파(Backpropagation)와 함께 경사하강법을 사용하여 가중치를 업데이트.
- **SVM, PCA 등의 다양한 ML 알고리즘:** 복잡한 최적화 문제에서도 사용됨.
- **비용함수 미분이 가능한 경우:** 기울기를 구할 수 있을 때 효과적으로 사용됨.

---

## 🔢 경사하강법의 종류

### 📍 1. 배치 경사하강법 (Batch Gradient Descent)

전체 데이터를 한 번에 기울기를 계산하고 업데이트.

- **장점:** 안정적이지만 데이터가 많을 경우 계산량이 많아 느려질 수 있음.
- **공식:**
  
  \[
  \theta := \theta - \alpha \frac{1}{m} \sum_{i=1}^{m} \nabla J(\theta)
  \]
  
  - *m: 모든 샘플의 개수*

---

### 📍 2. 확률적 경사하강법 (Stochastic Gradient Descent; SGD)

하나의 샘플만 사용하여 기울기를 계산하고 업데이트.

- **장점:** 빠르지만 노이즈가 커서 최적점 근처에서 계속 진동.
- **공식:**
  
  \[
  \theta := \theta - \alpha \nabla J(\theta)
  \]

---

### 📍 3. 미니배치 경사하강법 (Mini-batch Gradient Descent)

여러 개의 샘플(Mini-batch)로 기울기를 계산하고 업데이트.

- **배치 방법과 확률적 방법의 장점을 적절히 조합한 방식.**
- **공식:**
  
  \[
  \theta := \theta - \alpha \frac{1}{k} \sum_{i=1}^{k} \nabla J(\theta)
  \]

  - *k: 미니배치 크기 (보통 32 ~ 256)*

---

## 📌 결론

- **경사하강법은 머신러닝과 딥러닝에서 최적화를 위한 핵심 알고리즘**
- **Batch, Stochastic, Mini-batch** 세 가지 방식이 존재하며, 상황에 맞게 선택 가능
- **모델 학습의 속도와 안정성을 조절하기 위해 Learning rate 등의 하이퍼파라미터 조정이 중요**

---

[🏠 홈으로 돌아가기](../index.md)
