# 1st level. New York City Taxi Trip Duration
- competition: [New York City Taxi Trip Duration](https://www.kaggle.com/c/nyc-taxi-trip-duration)
- notebook: [EDA + Baseline Model](https://www.kaggle.com/aiswaryaramachandran/eda-baseline-model-0-40-rmse)

## Study Log
중요한 코드/새로운 코드/추가 자료를 정리해주세요.


#### 1. Understand the problem
```python
```

#### 2. Exploratory Data Analysis
* 지도 시각화 - folium 라이브러리
```python
```

#### 3. Feature Engineering
* 날짜 관련 변수가 있을 때는 datetime으로 형변환해주고, 유의미한 변수 단위로 잘라서 변수를 추가해주는 작업이 필요
```python
# object에서 datetime으로 형변환 
pd.to_datetime(data, format='%Y-%m-%d %H:%M:%S')
data.dt.date # 날짜
data.apply(lambda x: x.day) # 일
data.apply(lambda x: x.hour) # 시간
data.apply(lambda x: calendar.day_name[x.weekday()]) # 요일
```
* 배열 세로 결합(vstack)
```python
np.vstack((data1, data2)) # data1과 data2의 열 개수는 반드시 일치해야 한다
```

* 위/경도가 주어지고 이동거리를 측정하는 경우의 함수 -> 유클리디안 측정법과는 달리 곡면거리 측정 가능
```python
def calculateDistance(row):
    R = 6373.0
    pickup_lat = radians(row["pickup_latitude"])
    pickup_lon = radians(row["pickup_longitude"])
    dropoff_lat = radians(row["dropoff_latitude"])
    dropoff_lon = radians(row["dropoff_longitude"])
    diff_lon = dropoff_lon - pickup_lon
    diff_lat = dropoff_lat - pickup_lat
    a = sin(diff_lat / 2)**2 + cos(pickup_lat) * cos(dropoff_lat) * sin(diff_lon / 2)**2
    c = 2 * atan2(sqrt(a), sqrt(1 - a))
    distance = R * c
    return distance
```

#### 4. Model Selection
```python
```

#### 5. Model Optimization
```python
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
