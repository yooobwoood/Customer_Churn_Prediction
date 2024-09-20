✨SKN02-2nd-5Team✨

- 프로젝트 명 : 음악 스트리밍 회사의 고객 이탈 예측 모델 구현 프로젝트 

- 프로젝트 기간 : 2024-07-05 ~ 2024-07-08

# 👀 팀원 및 역할

| 이름     | 역할            |
|----------|-----------------|
| 전유빈   | 총괄 PM         |
| 정영재   | 기획            |
| 전상욱   | 데이터 분석     |
| 강민호   | 모델 구축       |
| 최수원   | 데이터 엔지니어링|

# 👀 Description
음악 스트리밍 회사의 고객의 이탈률을 줄이기 위해 모델을 구축하여 고객이 이탈할지 예측 하고자 함.😀



# 👀 Data Columns
아래의 이미지는 데이터로 사용한 고객 데이터 열 칼럼 임.👍 

![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN02-2nd-5Team/assets/169418269/1c2a41ef-ae08-45fc-9bfe-74b268cfc5c2)



# 👀 모델 평가지표 

- Accuracy vs F1-score
모델 평가지표로 위 두 가지를 고민하였다. 우리 데이터셋을 분석해본 결과, target값이 균형을 이루고 있었다. 따라서 균형한 데이터셋에 더 적합한 accuracy를 평가지표로 사용하기로 결정하였다.


- train-test split
확보한 데이터셋이 train, test 구분이 되어 있지 않았다. 따라서 우리는 주어진 125,000개의 데이터를 70%는 train set으로, 15%는 validation set으로, 15%는 test set으로 나누기로 결정하였다.


- Z-score vs IQR
우리가 확보한 데이터들의 분포를 그려본 결과, 정규분포를 이루지 않는 특성이 상당한 것으로 확인하였다. 따라서 Z-score로 이상치를 처리하는 것은 비합리적인 것으로 판단하였고 IQR을 이용하기로 하였다.


- 그리드 서치
하이퍼 파라미터 튜닝을 위해 그리드 서치 이용하기로 결정하였다.


# 👀 세부 목표 설정 
- 우리의 모델을 사용하면 어떤 고객이 이탈할지 안정적으로 예측할 수 있나❔
- 우리의 모델은 어떻게 작동하나❔
- 고객 중에서 몇 %의 고객을 유지할 것으로 예상하나❔

# 👀사용된 ML모델 및 DL모델 
- 로지스틱 회귀
- 랜덤포레스트
- XGBoost
- 신경망


# 👀Clustering
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN02-2nd-5Team/assets/127372470/ebe03fa1-acea-4be1-91d2-28a6d4227851)



# 모델 성능 평가
| 모델                 | ROC            |
|----------------------|-----------------|
| LogisticRegression   | ![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN02-2nd-5Team/assets/127372470/28bb8820-c9e9-4653-a573-c1ac74ca2b3d) |
| test accuracy | 0.81328 |
| Randomforest   | ![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN02-2nd-5Team/assets/127372470/90827e7a-5f1d-441d-a38b-3d2d97b2cb64)|
| test accuracy | 0.84554 |
| XGBoost   | ![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN02-2nd-5Team/assets/127372470/a6704b4e-bcdc-484c-a02f-91d6b3e0f138)|
| test accuracy | 0.847466 |
| CatBoost   | ![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN02-2nd-5Team/assets/127372470/3c196c98-6573-4d15-98e6-9389ca334b0c)|
| test accuracy | 0.85653 |
| MLP  | ![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN02-2nd-5Team/assets/127372470/3e933c3b-3dce-4647-bcdb-d5c80a18f9b0)|
| test accuracy | 0.83002 |
