## Binary-classification  

## Descripion  
💡 직원 데이터로부터 해당 직원의 퇴사 여부를 결정하는 Binary Classification task  
✅ Dataset: 3,722(train) / 931(test)  

## Pre-processing
- 각 colunm별 결측치 확인
- 범주형(명목형: Nominal) 변수 One-hot Encoding ➡️ cat2num 함수로 구현
- 상관관계 확인 ➡️ 기준과 바교했을 때 상관계수가 가장 낮은 feature 제거 
        ##### ❔❓ PCA(차원축소를 적용해보면 어떨까?)
- training data / validation data 분리
        ##### 값이 변하는 scale의 차이가 크면 학습 시 어려움이 있을 수 있음 ➡️ normalization 적용

## Training
- LightGBM, CatBoost, Random Forest ➡️ **Stacking** , final estimator: LGBMClassifier


## Results
Stacking Training Accuracy: 0.8629492777964394  
Stacking Validation Accuracy: 0.8617449664429531
