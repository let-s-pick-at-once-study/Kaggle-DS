# 3rd level. Home Credit Default Risk
* introduction: home credit default risk competition
- competition: [Home Credit Default Risk](https://www.kaggle.com/c/home-credit-default-risk)
- notebook: [introduction: home credit default risk competition](https://www.kaggle.com/willkoehrsen/start-here-a-gentle-introduction)

## Study Log
중요한 코드/새로운 코드/추가 자료를 정리해주세요.

#### 1. Data
```python
```

#### 2. Exploratory Data Analysis
- 이상치: 관계 확인 해서 변수 
- 결측치
```python
SimpleImputer #sklearn.impute 라이브러리
```
- 시각화
```python
tight_layout(h_pad=4.5)
kdeplot()
```
- eda
```python
select_dtype
pd.align
pd.cut
np.linspace(start, stop, num=50)
pd.unique()
pd.value_counts()
pd.count_values()
```

#### 3. Feature Engineering
```python
```

#### 4. Baseline
```python
lr.predict_proba #결과 예측
rf.predict_proba #test셋
```
