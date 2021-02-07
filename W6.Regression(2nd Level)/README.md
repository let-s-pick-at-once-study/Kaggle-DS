# 2nd level. Zillow Prize: Zillow’s Home Value Prediction (Zestimate)
- competition: [Zillow Prize: Zillow’s Home Value Prediction](https://www.kaggle.com/c/zillow-prize-1)
- notebook
  - [Simple Exploration Notebook - Zillow Prize](https://www.kaggle.com/sudalairajkumar/simple-exploration-notebook-zillow-prize)
  - [XGBoost, LightGBM, and OLS and NN](https://www.kaggle.com/aharless/xgboost-lightgbm-and-ols-and-nn)

## Study Log
중요한 코드/새로운 코드/추가 자료를 정리해주세요.

#### 1. Understand the problem
- `value_counts()` 중첩 사용
- `numpy.arange([start, ] stop, [step, ] dtype=None)` :범위를 생성할 수 있다.(sequence)
- `sns.jointplot()` :feature와 target의 분포를 확인하고 관계를 대략적으로 파악할 수 있다.
- `np.argsort()`
- `pd.read_csv(parse_dates=[])` :`parse_dates` 옵션으로 datetime변수 타입을 미리 지정할 수 있다.(여러개 가능)

#### 2. Exploratory Data Analysis
- [] 리스트 내 if 두개 중첩, and로 묶지 않은점도 신기
- ggplot 대체 -> plotline

#### 3. Feature Engineering
- 이상치 처리 : 범주형은 특정 값을 넣어라 or Simpleimputer 의 fill_value로
  - missing_values: 결측치는 무엇인지(ex: NaN, 0, -1)
  - fill_value: 결측값을 무엇으로 대체할지, 값을 특정한다

#### 4. Model Selection
- **XGBoost**에서 feature importance
  1. `xgbmodel.plot_importance`: F score는 중요한 feature로 선택된 횟수 총합을 의미한다. 여기서 중요도 기준은 gini계수
    - [참고](https://3months.tistory.com/169)
  2. `xgbmodel.feature_importances_`: 원래 알고 있는 gini계수 기반의 feature importance 반환
    - [참고](https://machinelearningmastery.com/feature-importance-and-feature-selection-with-xgboost-in-python/)

#### 5. Model Optimization
- 모델 별 parameters
##### LightGBM
```python
params['max_bin'] = 10
params['learning_rate'] = 0.0021 # shrinkage_rate
params['boosting_type'] = 'gbdt'
params['objective'] = 'regression'
params['metric'] = 'l1'          # or 'mae'
params['sub_feature'] = 0.345    # feature_fraction (small values => use very different submodels)
params['bagging_fraction'] = 0.85 # sub_row
params['bagging_freq'] = 40
params['num_leaves'] = 512        # num_leaf
params['min_data'] = 500         # min_data_in_leaf
params['min_hessian'] = 0.05     # min_sum_hessian_in_leaf
params['verbose'] = 0
params['feature_fraction_seed'
```
