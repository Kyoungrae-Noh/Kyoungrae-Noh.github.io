<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Underfitting vs Overfitting</title>
    <link rel="stylesheet" href="../styles.css">
</head>
<body>
    <div class="container">
        <header>
            <h1>📌 과소적합(Underfitting)과 과대적합(Overfitting)</h1>
        </header>

        <section class="box underfitting">
            <h2>🔷 1. 과소적합 상태</h2>
            <p>모델이 데이터의 패턴을 충분히 학습하지 못하는 상태</p>
            <ul>
                <li>✅ 학습 데이터와 테스트 데이터 모두에서 성능이 낮음.</li>
                <li>✅ 너무 단순한 모델(ex: 선형 모델)이 복잡한 패턴을 학습하지 못할 때 발생.</li>
            </ul>

            <h3>🛠 해결법</h3>
            <ul>
                <li>✅ <strong>더 복잡한 모델 사용:</strong> 신경망 층을 늘리거나, 더 강력한 알고리즘 사용 (ex: 선형 모델 → 딥러닝).</li>
                <li>✅ <strong>더 많은 Feature 추가:</strong> 데이터에서 더 많은 정보를 활용하도록 Feature Engineering 수행.</li>
                <li>✅ <strong>더 많은 학습 데이터 확보:</strong> 학습량이 충분히 이루어지지 않았을 수도 있음.</li>
                <li>✅ <strong>데이터 전처리 개선:</strong> 정규화(Normalization) 및 표준화(Standardization) 적용.</li>
            </ul>
        </section>

        <section class="box overfitting">
            <h2>🔶 2. 과대적합 상태</h2>
            <p>모델이 훈련 데이터에 너무 최적화되어 테스트 데이터에서 성능이 떨어지는 현상</p>
            <ul>
                <li>✅ 훈련 데이터에서는 높은 성능을 내지만, 일반화가 안됨.</li>
            </ul>

            <h3>🛠 해결법</h3>
            <ul>
                <li>✅ <strong>정규화 적용 (Regularization):</strong> L1 / L2 정규화 (Lasso, Ridge) 또는 Dropout 적용.</li>
                <li>✅ <strong>더 많은 데이터 확보:</strong> 데이터가 적을 경우, 모델이 특정 패턴을 외워버릴 가능성이 높음.</li>
                <li>✅ <strong>모델 복잡도 줄이기:</strong> 신경망 층 수, 뉴런 수 줄이기.</li>
                <li>✅ <strong>Early Stopping 사용:</strong> 검증 데이터의 성능이 더 이상 증가하지 않으면 학습 중단.</li>
                <li>✅ <strong>Batch Normalization:</strong> 신경망 뉴런의 값들이 너무 커지거나 작아지지 않도록 정규화.</li>
                <li>✅ <strong>앙상블 학습 적용:</strong> 여러 모델을 결합하여 과적합을 방지하는 방법 (Random Forest, Bagging, Boosting).</li>
            </ul>
        </section>

        <section class="conclusion">
            <h2>📌 결론</h2>
            <ul>
                <li>🔹 **과소적합은 모델이 너무 단순하여 충분한 학습을 하지 못하는 문제**</li>
                <li>🔹 **과대적합은 모델이 너무 복잡하여 훈련 데이터에 과적합하는 문제**</li>
                <li>🔹 **적절한 Regularization, Feature Engineering, 모델 구조 조정이 필요**</li>
            </ul>
        </section>

        <a href="../index.html" class="button">🏠 Back to Home</a>
    </div>
</body>
</html>
