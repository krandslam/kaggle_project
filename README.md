# kaggle_project

- 각각의 전처리 결과는 스케일링 한것과 스케일링 안한것(노스케일링)으로 구분했고  
light GBM, Xgboost, Randomforest 모델로 테스트함

- 결과1: lightGBM 스케일 / 결과2 : lightGBM 노스케일  
결과3: Xgboost 스케일 / 결과4 : Xgboost 노스케일  
결과5: Randomforest 스케일 / 결과6 : Randomforest 노스케일  


- 결측치1: " ?"로 되어있는 범주형 결측치 모두 삭제  
결과1: 
결과2: (정확도) 0.7166345576250718 <br>
      (F1 score) 0.7166345576250718
결과3: 
결과4: (정확도) 0.6598626997843584 <br>
      (F1 score) 0.6598626997843584
결과5: 
결과6: (정확도) 0.67864532211554 <br>
      (F1 score) 0.6598626997843584

- 결측치2: 결측치 자체로 두고 처리  
결과1: 
결과2: (정확도) 0.7111835566506057 <br>
      (F1 score) 0.7111835566506057
결과3: 
결과4: (정확도) 0.6547251234120461 <br>
      (F1 score) 0.6547251234120461
결과5: 
결과6: (정확도) 0.6664351428115887 <br>
      (F1 score) 0.6664351428115887

- 결측치3: 결측치를 최빈값으로 대체  
결과1: 결과2: 결과3: 결과4: 결과5: 결과6:
