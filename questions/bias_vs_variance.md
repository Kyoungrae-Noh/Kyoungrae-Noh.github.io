---
layout: default
title: "Bias vs Variance"
permalink: /questions/bias_vs_variance/
---

# 📌 Bias vs Variance

## 📍 Bias (편향)
**Bias(편향)**는 모델이 훈련 데이터에 대해 너무 단순한 가정을 할 때 발생하며,  
일반적으로 **underfitting(과소적합)**의 원인이 됩니다.

- **Bias가 높은 모델 특징**
  - 데이터의 복잡한 패턴을 충분히 학습하지 못함
  - 훈련 데이터와 테스트 데이터 모두에서 높은 오류 발생
  - 선형 회귀와 같은 간단한 모델에서 자주 발생

---

## 📍 Variance (분산)
**Variance(분산)**는 모델이 훈련 데이터에 너무 적합하게 학습되어,  
새로운 데이터에 대한 일반화 성능이 낮아질 때 발생하며,  
일반적으로 **overfitting(과적합)**의 원인이 됩니다.

- **Variance가 높은 모델 특징**
  - 훈련 데이터에서는 낮은 오류지만, 테스트 데이터에서는 높은 오류
  - 데이터의 노이즈까지 학습하여 복잡한 모델 구조가 됨
  - 깊은 신경망 모델 또는 트리 기반 모델에서 발생할 가능성이 높음

---

## ⚖️ Bias-Variance Tradeoff (편향-분산 트레이드오프)

머신러닝 모델을 설계할 때 **Bias와 Variance의 균형**을 맞추는 것이 매우 중요합니다.  
이를 **Bias-Variance Tradeoff**라고 부르며,  
모델이 **너무 단순하지도, 너무 복잡하지도 않도록** 조절해야 합니다.

- **Bias가 너무 크면** → 모델이 패턴을 학습하지 못함 (**Underfitting** 발생)
- **Variance가 너무 크면** → 모델이 특정 데이터에 과적합함 (**Overfitting** 발생)
- 최적의 모델은 **적절한 Bias와 Variance의 균형을 맞춘 상태**임

---

## 🏆 해결 방법

Bias 또는 Variance 문제가 발생했을 때 해결할 수 있는 방법:

### ✅ Bias가 너무 높은 경우 (Underfitting 해결)
- 모델을 더 복잡하게 변경 (ex. 선형 → 비선형 모델 사용)
- 더 많은 Feature 추가 (특징 엔지니어링)
- 더 깊은 신경망 모델 사용
- 학습 시간 증가

### ✅ Variance가 너무 높은 경우 (Overfitting 해결)
- 더 많은 데이터 확보 (데이터 증강, 데이터 수집)
- Regularization 적용 (L1/L2 정규화, Dropout 등)
- Feature 수 줄이기 (불필요한 Feature 제거)
- 모델 복잡도 낮추기 (ex. 너무 깊은 네트워크 구조 간소화)

---

## 📌 결론
Bias와 Variance는 **서로 반대되는 개념**이므로,  
적절한 **Tradeoff**를 찾아 **일반화 성능이 좋은 모델**을 만드는 것이 중요합니다!  

[🏠 홈으로 돌아가기](../index.md)
