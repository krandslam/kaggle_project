스케일링만 한 lgb 값: (정확도) 0.872513522042239 (F1 score) 0.7117869083684442
<br><br>
(묶은 뒤 새로운 컬럼 Married에 저장, 원래 컬럼인 marital-status 삭제)
- 1group: married civ , AF 묶기 -> married <br>
                     (정확도) 0.8728206310558081 (F1 score) 0.7122724556944607
                     
(묶은 뒤 새로운 컬럼 SebAbs에 저장, 원래 컬럼인 marital-status 삭제)                     
-  2group: married civ , AF 묶기 -> married / separated, married spouse absent -> SepAbs / 나머지 두기 <br>
                     (정확도) 0.8731619163397506 (F1 score) 0.712937282967321
<br><br>
정확도와 F1 score 모두 높게 나온 2group 채택 <br>
education 삭제 + 2group 모두 적용하여 Kaggle에 적용하여 나온 점수: 0.87266 <br>
(모두 lgb 모델 기준)
