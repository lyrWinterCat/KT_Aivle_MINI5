# 📢 VOC 기반 고객 해지 예측 프로젝트
## 📝 프로젝트 개요
본 프로젝트는 **VOC(Voice of Customer, 고객의 소리) 데이터를 활용하여 고객 해지 여부를 예측**하는 AI 모델을 개발하는 것을 목표로 합니다.  
기업에서 VOC 데이터를 분석하여 **고객 불만 유형을 파악하고, 해지 가능성이 높은 고객을 사전에 식별하여 이탈을 방지하는 마케팅 전략**을 수립할 수 있습니다.

### 🎯 **목표**
✅ 고객 VOC 데이터를 기반으로 **해지 여부를 예측**  
✅ 머신러닝/딥러닝 모델을 활용하여 **해지 방어 전략 수립**  
✅ VOC 패턴을 분석하여 **서비스 개선 방향 도출**  

---

## 🚀 프로젝트 수행 과정

### **1️⃣ 데이터 전처리**
- **결측치 처리 (Missing Value Handling)**
  - `dropna()`, `fillna()` 등의 기법을 활용하여 데이터의 결측치를 제거하거나 보간법으로 채움  
  - 주요 방법: **평균/중앙값 대체, KNN Imputation, Iterative Imputation**
- **카테고리형 변수 변환**
  - **라벨 인코딩(Label Encoding)** → 고유값을 정수로 변환 (예: A→0, B→1)
  - **원핫 인코딩(One-Hot Encoding)** → 컬럼을 여러 개로 나누어 이진 변환
- **정규화(Normalization) vs 표준화(Standardization)**
  - **MinMaxScaler**: 데이터 값을 0~1 범위로 변환
  - **StandardScaler**: 평균을 0, 표준편차를 1로 변환

### **2️⃣ 모델 학습**
- **머신러닝 모델**
  - **Random Forest**: 여러 개의 의사결정 트리를 조합하여 예측력을 향상하는 앙상블 모델
  - **XGBoost (Extreme Gradient Boosting)**: 그래디언트 부스팅 기반의 강력한 트리 모델
  - **LightGBM (Light Gradient Boosting Machine)**: XGBoost보다 빠르고 가벼운 모델
- **딥러닝 모델**
  - **Dense Layer 기반 신경망 모델 (MLP, Multi-Layer Perceptron)**
  - 입력층 → 은닉층 (ReLU 활성화 함수) → 출력층 (Softmax/Sigmoid) 구조

### **3️⃣ 성능 평가**
- **Confusion Matrix (혼동 행렬)**
  - 모델의 예측 결과를 정리한 행렬로 **정확도(Accuracy)**, **정밀도(Precision)**, **재현율(Recall)** 계산
- **Precision-Recall Curve**
  - 불균형 데이터에서 모델의 성능을 평가할 때 중요한 지표
- **Feature Importance (특성 중요도 분석)**
  - 모델이 예측할 때 가장 중요한 영향을 미치는 변수 확인

---

## 🔥 실행 방법

```bash
1️⃣ 필수 라이브러리 설치
pip install -r requirements.txt

2️⃣ 데이터 분석 및 모델 학습
python train.py

3️⃣ 모델 평가 및 예측
python evaluate.py

```

---
 
# 📉 고객 이탈 예측 프로젝트
## 📝 프로젝트 개요
본 프로젝트는 **통신사 고객 데이터를 활용하여 고객 이탈(Churn) 여부를 예측**하는 AI 모델을 개발하는 프로젝트입니다.  
기업에서는 고객 이탈 예측 모델을 활용하여 **이탈 가능성이 높은 고객을 조기에 식별하고, 맞춤형 마케팅 전략을 적용**하여 이탈률을 줄일 수 있습니다.

### 🎯 **목표**
✅ **통신사 고객 데이터 분석 및 이탈 패턴 식별**  
✅ 머신러닝/딥러닝 기반 **고객 이탈 예측 모델 개발**  
✅ **이탈 방지 마케팅 전략 도출**  

---

## 🚀 프로젝트 수행 과정

### **1️⃣ 데이터 전처리**
- **결측치 처리 (Missing Value Handling)**
  - `dropna()`, `fillna()` 등의 기법을 활용하여 결측 데이터를 보완
- **데이터 인코딩**
  - **라벨 인코딩**: 고객 유형(일반, VIP) 같은 범주형 데이터를 정수로 변환
  - **원핫 인코딩**: 인터넷 서비스(광랜, 5G) 같은 데이터를 이진 벡터로 변환
- **데이터 스케일링 (Normalization & Standardization)**
  - **MinMaxScaler** (0~1 사이 값으로 변환)
  - **StandardScaler** (평균 0, 분산 1로 변환)

### **2️⃣ 모델 학습**
- **머신러닝 모델**
  - **Random Forest**: 고객 이탈 예측에서 많이 활용되는 모델로, 변수 간 관계를 분석하여 예측
  - **XGBoost / LightGBM**: 많은 데이터를 처리할 때 빠르고 효과적
- **딥러닝 모델**
  - **Multi-Layer Perceptron (MLP, 다층 퍼셉트론)**

### **3️⃣ 성능 평가**
- **Accuracy (정확도)**
  - 전체 데이터 중 모델이 맞춘 비율
- **Precision (정밀도) & Recall (재현율)**
  - **정밀도(Precision)**: "이탈 고객"이라고 예측한 것 중 실제 이탈 고객의 비율
  - **재현율(Recall)**: 실제 이탈 고객 중에서 모델이 "이탈"이라고 예측한 비율
- **ROC Curve & AUC Score**
  - 모델이 분류를 얼마나 잘 수행하는지 시각화

---

## 🔥 실행 방법

```bash
1️⃣ 필수 라이브러리 설치
pip install -r requirements.txt

2️⃣ 데이터 분석 및 모델 학습
python train.py

3️⃣ 모델 평가 및 예측
python evaluate.py
```

---





