# titanic-ml-survival-prediction
Titanic Survival Prediction using Tabular ML &amp; LightGBM

# 타이타닉 생존 예측 머신러닝 프로젝트

## 프로젝트 소개
타이타닉 승객 데이터를 활용해 다양한 사회·경제적 특성이 생존 여부에 어떤 영향을 미치는지 분석하고, 구조화된(tabular) 데이터를 기반으로 생존 예측 머신러닝 모델을 구축했습니다.  

이 프로젝트를 통해 데이터 전처리, 모델 비교, 하이퍼파라미터 튜닝 등 머신러닝 전체 파이프라인을 경험하는 것을 목표로 했습니다.

---

## 데이터셋
- Kaggle Titanic Dataset 사용
- 승객 나이, 성별, 좌석 등급, 요금 등 다양한 특성 포함
- 목표 변수(Target): 생존 여부 (Survived)

---

## 주요 수행 내용

### 1. 데이터 전처리
- SimpleImputer, IterativeImputer(DecisionTreeRegressor 기반)로 결측치 처리
- 범주형 변수 인코딩 및 IQR 기반 이상치 제거
- 클래스 불균형을 고려한 label encoding 전략 실험

### 2. 모델 비교 실험
다양한 모델 성능 비교:
- Logistic Regression (L1 / L2)
- Decision Tree
- Random Forest
- XGBoost
- LightGBM

### 3. 모델 최적화
- 5-Fold Cross Validation 적용
- GridSearchCV 기반 하이퍼파라미터 튜닝
- LightGBM을 최종 모델로 선정

### 4. 성능 평가
- Accuracy
- F1-score
- ROC-AUC

---

## 결과
- 최종 모델: **LightGBM**
- 5-Fold Cross Validation 기준
  - Accuracy: **0.90**
  - F1-score: **0.95**
  - ROC-AUC: **0.79**

전처리 전략과 feature engineering이 모델 성능에 큰 영향을 미친다는 것을 확인했습니다.

---

## 배운 점
- 머신러닝 성능은 모델보다 데이터 전처리의 영향을 크게 받는다.
- 클래스 불균형 문제는 모델 평가 지표에 큰 영향을 준다.
- Cross Validation과 GridSearch는 안정적인 모델 평가에 필수적이다.
- Feature importance 분석을 통해 tabular 데이터 해석 능력을 기를 수 있었다.

---

## 사용 기술
- Python
- Scikit-learn
- LightGBM
- Pandas / NumPy / Matplotlib

---

## Contributors
김민지
김서영
안다희
임가윤

---

## Contact
김서영 | AI Undergraduate @ Ewha
GDG Ewha AI Member
Email: sy1214ei@gmail.com

