# Probono-AI 모델링 및 테스트용<br></br>

## 파일 목록
* population_data : 22/09/01~23/08/31까지의 서울시 데이터 모음
* preprocessed_data : 전처리 된 지역별 데이터 모음(화곡 1동, 역촌동, 진관동, 길동)
  * Yeokchon_pop_data.csv : 역촌동 인구 데이터
  * Jingwan_pop_data.csv : 진관동 인구 데이터
  * Hwagok1_pop_data.csv : 화곡1동 인구 데이터
  * Gil_pop_data.csv : 길동 인구 데이터
    
* modeling_process : 지역별 데이터 모델링 과정
  * yeokchon_modeling_process.ipynb
  * jingwan_modeling_process.ipynb
  * hwagok1_modeling_process.ipynb
  * gil_modeling_process.ipynb
    
* trained_models : 지역별 fitting 된 lstm 모델
  * yeokchon_model.h5
  * jingwan_model.h5
  * hwagok1_model.h5
  * gil_model.h5
    
* data preprocessing.ipynb : 데이터 전처리

<br></br>

## 경로 지정
`cd /content/drive/MyDrive/comma_ai_dev/Probono-AI-Model` 수정
<br></br>

## lstm 모델 호출
```python
from keras.models import load_model  

model = load_model('population_predict.h5')
#input_shape -> (n_input = 24, n_features = 1)
```
<br></br>

## csv file 호출
```python
import pandas as pd

df = pd.read_csv('pildong_data.csv',index_col=0, parse_dates=True)
```
