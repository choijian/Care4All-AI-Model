# Probono-AI 모델링 및 테스트용<br></br>

## 파일 목록
* population_data : modeling에 사용한 데이터 모음
* Aug_pop_prediction.csv : lstm을 이용해 예측한 시간대별 8월 인구수
* data preprocessing.ipynb : 데이터 전처리
* forecasting_monthly_data.ipynb : 데이터 예측
* lstm_modelin.ipynb : 데이터 모델링
* pildong_data.csv : 22/08/01~23/07/31까지의 data를 합친 csv 파일
* population_predict.h5 : 학습된 lstm 모델
<br></br>

## 경로 지정
`cd /content/drive/MyDrive/comma_ai_dev/Probono-AI-Model` 수정
<br></br>

## lstm 모델 호출
```python
from keras.models import load_model  

model = load_model('population_predict.h5')
#input_shape -> (n_input = 168, n_features = 1)
```
<br></br>

## csv file 호출
```python
import pandas as pd

df = pd.read_csv('pildong_data.csv',index_col=0, parse_dates=True)
```
