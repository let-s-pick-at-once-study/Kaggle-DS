# 1st level. Costa-rican competition
- competition: [Costa Rican Household Poverty Level Prediction](https://www.kaggle.com/c/costa-rican-household-poverty-prediction)
- notebook: [A Complete Introduction and Walkthrough](https://www.kaggle.com/willkoehrsen/a-complete-introduction-and-walkthrough)

## Study Log
중요한 코드/새로운 코드/추가 자료를 정리해주세요.


#### 1. Understand the problem
- 데이터 구성 살펴보기: Target 분포, 칼럼별 분포 및 특징 시각화
```python
```

#### 2. Exploratory Data Analysis
```python
sns.lmplot()
annotate
np.triu()
pd.value_counts()
```

#### 3. Feature Engineering
```python
```

#### 4. Model Selection
- lda(다중공선성 탐지 가능)
- RFECV(모델 기반 피처 셀렉션)
- 앙상블 모델은 스케일링이 따로 필요없음, knn, svm 등은 스케일링이 필요
```python
cross_val_score() #성능평가
cv_model() #for문을 통해 k 개수 여러개 확인
```

#### 5. Model Optimization
- Hyperopt
```python
np.cumsum() #변수개수 임계값 설정
literal_eval() #모델 최적화
```

#### 6. Implementing Best model
```python
```

#### 7. Investigate predictions
```python
```

#### 8. Try new techniques
```python
```
