# 3rd level. Home Credit Default Risk
* introduction: home credit default risk competition


* 이상치 - 관계 확인 해서 변수 
* 결측치 - SimpleImputer(sklearn.impute 라이브러리)
* eda - select_dtype, pd.align, pd.cut, np.linspace(start, stop, num=50), pd.unique(), pd.value_counts(), pd.count_values()
* 시각화 - tight_layout(h_pad=4.5), kdeplot()
* 모델링 - lr.predict_proba(결과 예측), rf.predict_proba(test셋)
