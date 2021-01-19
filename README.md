# kaggle_project

## 결측치 처리

- 각각의 전처리 결과는 스케일링 한것과 스케일링 안한것(노스케일링)으로 구분했고  
light GBM, Xgboost, Randomforest 모델로 테스트함

- 결과1: lightGBM 스케일 / 결과2 : lightGBM 노스케일  
결과3: Xgboost 스케일 / 결과4 : Xgboost 노스케일  
결과5: Randomforest 스케일 / 결과6 : Randomforest 노스케일  


- 결측치1: " ?"로 되어있는 범주형 결측치 모두 삭제  
결과1: (정확도) 0.8697604649329989
      (F1 score) 0.7174423280503007 <br>
결과2: (정확도) 0.8693925338052211
      (F1 score) 0.7166345576250718 <br>
결과3: (정확도) 0.8541569947809056
      (F1 score) 0.6598626997843584 <br>
결과4: (정확도) 0.8541569947809056 
      (F1 score) 0.6598626997843584 <br>
결과5: (정확도) 0.8507710832214143
      (F1 score) 0.6777270448443145 <br>
결과6: (정확도) 0.8510655527037543
      (F1 score) 0.6782019919138523 <br>

- 결측치2: 결측치 자체로 두고 처리  
결과1: (정확도) 0.872513522042239
      (F1 score) 0.7117869083684442 <br>
결과2: (정확도) 0.8722404379220361
      (F1 score) 0.7111835566506057 <br>
결과3: (정확도) 0.857055728862821
      (F1 score) 0.6547251234120461 <br>
결과4: (정확도) 0.857055728862821
      (F1 score) 0.6547251234120461 <br>
결과5: (정확도) 0.8514250282085231
      (F1 score) 0.6675322550482756 <br>
결과6: (정확도) 0.8514591346125855
      (F1 score) 0.6674148729426281 <br>

- 결측치3: 결측치를 최빈값으로 대체  
결과1: (정확도) 0.8721041520384076
      (F1 score) 0.71074375604975 <br>
결과2: (정확도) 0.8725134754646982
      (F1 score) 0.711476594182421 <br>
결과3: (정확도) 0.8572263423938293
      (F1 score) 0.6551490745956257 <br>
결과4: (정확도) 0.8572263423938293
      (F1 score) 0.6551490745956257 <br>
결과5: (정확도) 0.8529263737172255
      (F1 score) 0.6709974649826776 <br>
결과6: (정확도) 0.8529263970059956
      (F1 score) 0.6709962997052819 <br>
   
## 컬럼 전처리
lgb 모델 + 스케일링한 결과  
각 컬럼 전처리 방법은 해당 폴더의 README 파일에 존재
- capital gain & loss <br>
- capital gain & loss <br>
방법1 결과: (정확도) 0.8727524415364533 (F1 score) 0.7117820081101073 (캐글) 0.87253 <br>
방법2 결과: (정확도) 0.8539845222832776 (F1 score) 0.6721465923376397 (캐글) 0.72382 <br>
결론: 방법1이 가장 좋다 캐글에서도 <br>
