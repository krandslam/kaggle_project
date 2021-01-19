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
방법1 결과: (정확도) 0.8725817814279043 (F1 score) 0.711695036072961 <br>
방법2_평균 결과: (정확도) 0.8539845222832776 (F1 score) 0.6721465923376397 <br>
방법2_중앙 결과: (정확도) 0.8587957144004946 (F1 score) 0.6803504509092442  <br>
방법3_평균 결과: (정확도) 0.8545303994140545 (F1 score) 0.6728275072398571  <br>
방법3_중앙 결과: (정확도) 0.8588641368075521 (F1 score) 0.680951719865188  <br>
결론: 방법1이 가장 좋다 캐글에서도 <br>

- marital-status <br>
1group_결과: (정확도) 0.8728206310558081 (F1 score) 0.7122724556944607 <br>
2group_결과: (정확도) 0.8731619163397506 (F1 score) 0.712937282967321 <br>
결론: 2group 채택

- education & education-num <br>
education 삭제: (정확도) 0.8730937151760108 (F1 score) 0.713032906886005 <br>
education-num 그룹화: (정확도) 0.871762750310614 (F1 score) 0.7097831638905535 <br>
결론: education 컬럼 삭제 채택, education-num은 그룹화 X <br>
education 삭제 + 2group 모두 적용하여 Kaggle에 적용하여 나온 점수: 0.87266

- age <br>
방법1 결과: (정확도 )0.872957149827139 (F1 score) 0.7124075578884208<br>
방법2 결과: (정확도) 0.8700566732224555 (F1 score) 0.7039559571560925<br>
방법3 결과: (정확도) 0.8706025736420028 (F1 score) 0.7046080388700718<br>
방법4 결과: (정확도) 0.8720017163823691 (F1 score) 0.7112684039390137<br>
방법5 결과: (정확도) 0.8729570333832877 (F1 score) 0.7113094769692528<br>
결론: 방법1 채택

- workclass <br>
방법1 결과: (정확도) 0.872513522042239 (F1 score) 0.7117869083684442<br>
방법2 결과: (정확도) 0.8727523716701425 (F1 score) 0.7127117491470303<br> 
결론: 방법2 채택

- fnlwgt <br>
방법1 결과: (정확도) 0.8713875332883859 (F1 score) 0.7089981375352713<br>
결론: 채택 안함

- race <br>
방법1_race 삭제: (정확도) 0.8727523949589129 (F1 score) 0.7123987069045048 <br>
방법2_백인만 : (정확도) 0.8726500408135699 (F1 score) 0.7120529216154321<br>
결론: 방법1 채택

- occupation <br>
직군별 분류 단순화: (정확도) 0.8719333754860076  (F1 score) 0.7086311680545627<br>
소득별 분류 단순화: (정확도) 0.8701247462979588 (F1 score) 0.7047927395485947<br>
결론 : 그대로 두거나 다른 기준으로 변형<br>

- relationship <br>
husband, wife 합치기: (정확도) 0.8728889486633993 (F1 score) 0.7124114796416939<br>
결론: 방법 사용<br>

- native country <br>
오픈소스: (정확도) 0.8725817232059787 (F1 score) 0.712096630613746<br>
캐글점수 : 0.87215(소폭상승)<br>
결론: 오픈소스 사용<br>

- hours per week <br>
범위별 그룹 만들기: (정확도) 0.8718995252584179 (F1 score) 0.7095955541927542<br>
결론: 분류 범위 다르게 설정하거나, 그대로 사용<br>
