# 머신러닝(Machine Learning) 정리

## 머신러닝 기본 개념
참고 사이트 : https://www.iso.org/artificial-intelligence/machine-learning

머신러닝(Machine Learning)은 **명시적인 프로그래밍 없이 데이터로부터 학습하여 예측 또는 분류를 수행하는 인공지능의 한 분야**입니다. 즉, 데이터를 기반으로 패턴을 인식하고 이를 바탕으로 새로운 데이터에 대해 판단하는 기술입니다.

- **전통적인 프로그래밍**: 규칙(알고리즘) + 데이터 → 결과  
- **머신러닝 방식**: 데이터 + 결과 → 규칙(모델)을 학습
<img width="1370" height="756" alt="스크린샷 2025-07-11 121320" src="https://github.com/user-attachments/assets/92524ab4-e619-4551-bea1-a2153fdf27aa" />

---

<img width="1380" height="758" alt="image" src="https://github.com/user-attachments/assets/5075dc85-60f3-4765-a01d-744f5a200b68" />

> 관련 사이트 : https://www.iso.org/artificial-intelligence/machine-learning



---

## 머신러닝의 기본 3가지 모델

머신러닝은 학습 방식에 따라 다음의 세 가지 유형으로 나눌 수 있습니다.

### 1. 지도학습(Supervised Learning)
- **특징**: 입력 데이터와 정답(레이블)을 기반으로 학습
- **목표**: 주어진 입력에 대해 올바른 출력을 예측
- **예시**: 이메일 스팸 분류, 가격 예측, 이미지 분류

### 2. 비지도학습(Unsupervised Learning)
- **특징**: 정답(레이블) 없이 입력 데이터만으로 학습
- **목표**: 데이터 내 숨겨진 구조나 패턴 발견
- **예시**: 고객 군집화, 이상 탐지, 차원 축소

### 3. 강화학습(Reinforcement Learning)
- **특징**: 환경과 상호작용하며 보상 기반으로 학습
- **목표**: 장기적인 보상을 최대화하는 행동 학습
- **예시**: 게임 AI, 로봇 제어, 자율주행

---

## ML 기반 데이터 분석 (ML Based Data Analysis)

머신러닝을 이용한 데이터 분석 과정은 다음과 같습니다:

1. **문제 정의**  
   - 예측하려는 값은 무엇인가?  
   - 회귀, 분류, 군집 중 어떤 문제인가?

2. **데이터 수집**  
   - 내부/외부 소스에서 관련 데이터 확보  
   - 웹 크롤링, API, 센서 등 다양한 방법 활용

3. **데이터 전처리**  
   - 결측치 처리, 이상치 제거  
   - 정규화, 인코딩 등 데이터 정제 작업

4. **특징 선택 및 추출**  
   - 중요한 변수 선택  
   - 변수 조합 또는 변형을 통해 성능 향상

5. **모델 선택 및 학습**  
   - 적절한 알고리즘 선택 (예: SVM, Random Forest, XGBoost 등)  
   - 학습 데이터로 모델 학습

6. **평가 및 튜닝**  
   - 검증 데이터로 성능 측정 (Accuracy, F1-score 등)  
   - 하이퍼파라미터 튜닝

7. **예측 및 해석**  
   - 새 데이터에 대해 예측 수행  
   - 결과 해석 및 비즈니스 적용

---

## 머신러닝 과정 주요 용어 정리

| 용어             | 설명 |
|------------------|------|
| 데이터셋 (Dataset) | 모델이 학습하는 데이터 집합 |
| 특성 (Feature)    | 입력 변수, 모델이 학습하는 정보 |
| 레이블 (Label)    | 정답 데이터 (지도학습에서 필요) |
| 훈련 데이터 (Training Data) | 모델 학습에 사용되는 데이터 |
| 테스트 데이터 (Test Data)   | 모델 평가에 사용되는 데이터 |
| 오버피팅 (Overfitting)     | 학습 데이터에만 과도하게 맞춰져 일반화 성능 저하 |
| 정규화 (Normalization)     | 데이터의 스케일을 일정하게 조정 |
| 하이퍼파라미터 (Hyperparameter) | 학습 전 설정해야 하는 모델 외부 변수 (예: 학습률) |

---

## 지도학습 vs 비지도학습 vs 강화학습 비교

| 항목               | 지도학습 (Supervised) | 비지도학습 (Unsupervised) | 강화학습 (Reinforcement) |
|--------------------|------------------------|-----------------------------|---------------------------|
| 입력 데이터         | 특징 + 정답(레이블)     | 특징만 있음                 | 상태 정보                 |
| 출력 결과          | 예측값 (분류/회귀)      | 군집, 패턴                  | 행동 또는 정책             |
| 학습 방법          | 정답 기반 오류 최소화   | 패턴 발견 또는 군집화       | 보상 최대화를 위한 시도와 오류 |
| 주요 알고리즘       | SVM, 결정트리, KNN 등    | K-Means, PCA, DBSCAN 등     | Q-Learning, DQN 등         |
| 활용 예시          | 이메일 분류, 가격 예측   | 고객 세분화, 이상 탐지      | 게임 AI, 로봇 제어         |

---

# 머신러닝 분류기(Classifiers) 정리

## 분류(Classification)란?

분류는 **입력 데이터가 어떤 범주(category)나 클래스(class)에 속하는지를 예측**하는 **지도학습(Supervised Learning)** 문제입니다.

- 예시:
  - 이메일이 스팸인지 아닌지 분류
  - 이미지가 고양이인지 개인지 분류
  - 고객이 이탈할지 유지될지 예측



---

## 분류기 학습 및 예측 공통 예제 (scikit_learn)
```bash
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score
from sklearn.ensemble import RandomForestClassifier

# 데이터 로드
X, y = load_iris(return_X_y=True)

# 데이터 분할
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# 스케일링 (일부 분류기에 필요)
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# 분류기 정의 및 학습
clf = RandomForestClassifier()
clf.fit(X_train, y_train)

# 예측 및 평가
y_pred = clf.predict(X_test)
print("Accuracy:", accuracy_score(y_test, y_pred))
```

### 1. **로지스틱 회귀(Logistic Regression)**

- **특징**: 선형 모델로서, 확률 기반 이진 분류 수행
- **장점**: 해석 용이, 빠름
- **단점**: 선형 결정 경계만 표현 가능
- **사용 예시**: 이진 분류, 질병 진단

```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression()
```

## Classification Performance Measures : Precision and Recall
<img width="1374" height="766" alt="image" src="https://github.com/user-attachments/assets/812caa27-d097-4281-a822-a081910d850d" />

# 분류 모델 평가 지표: Precision(정밀도) & Recall(재현율)

머신러닝에서 모델이 얼마나 잘 예측했는지 평가할 때, 정확도(accuracy) 외에도 **정밀도(precision)**와 **재현율(recall)**이라는 중요한 지표가 있음

---

## 용어 먼저 알아보기

| 용어             | 뜻 |
|------------------|----|
| **Positive**     | 모델이 **"맞다"**, **"해당된다"**고 예측한 것 |
| **Negative**     | 모델이 **"아니다"**, **"해당되지 않는다"**고 예측한 것 |
| **True**         | 예측이 **정답**인 경우 |
| **False**        | 예측이 **틀림**인 경우 |

---

## 혼동 행렬 (Confusion Matrix)

|               | 예측: 스팸(Positive) | 예측: 정상 메일(Negative) |
|---------------|---------------------|----------------------------|
| **실제: 스팸**    | ✅ **True Positive (TP)**  | ❌ **False Negative (FN)** |
| **실제: 정상**    | ❌ **False Positive (FP)** | ✅ **True Negative (TN)**  |

- **TP**: 스팸을 스팸이라고 잘 맞힘
- **FP**: 정상 메일을 스팸으로 잘못 판단
- **FN**: 스팸인데 정상으로 놓침
- **TN**: 정상 메일을 정상이라고 잘 맞힘

---


# Colab에서 실습
> https://colab.research.google.com/drive/1rdJVAkb5E2QTAmZoxPNT5xNYF7n8kJw-?authuser=0#scrollTo=LHKKdzJcbMZ9









