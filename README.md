# DNA_data
## “데이콘 유전체 정보 품종 분류 AI 경진대회”
- 데이콘 유전체 정보 품종 분류 AI 경진대회
- 기간: ‘23년 01월 ~ ‘23년 02월(1개월)
- 성과: 상위 25%
- Tools: Python
<br>


### 👤역할
데이터 분석, 모델 개발
<br>

### 🧐 Main Issues
모델 개발과 파라미터 설정을 통해 98% 이상의 accuracy를 달성하기가 어려웠음. 모델 파라미터 설정이 아닌 데이터 분석을 통한 인사이트 도출이 필요하였음.
다뤄보지 못한 딥러닝 모델이나 XGBoost 등 부스팅 모델을 사용하면 효과가 향상될 것으로 기대됨.

### 🛠️ Resolved
데이터 class의 불균형을 발견해 smote 기법을 활용해 데이터 불균형을 해결해 모델의 정확도를 높이고자 하였음. 
  하지만 데이터 기존의 불균형 샘플들을 보간하여도 모델의 정확도가 향상되지 않음.
snp_info 데이터를 활용, 데이터를 유전체 그룹 별로 묶어서 학습시켜야 한다는 인사이트를 도출.
  그룹별로 묶어서 성능을 확인해보고 최종적으로 선택하였음.
xgboost, catboost, knn모델이 기존에 정확도가 높은 모델이였어서 3가지 모델에 대해 gridsearch를 수행,베스트 parameter와 best snp group을 활용해 모델 학습 후 예측
그중 knn모델이 accuracy 99프로로 향상됨을 확인.

<br>

### 🎯 Result
그리드 서치, snp grouping을 활용해 유의미한 feature를 선정해 학습시켜 모델의 향상을 확인하였음.
초기 97%의 정확도를 가진 모델은 로지스틱 회귀 모델이였음.
<br>
### ⭐ Learnd Lessons
단순 모델링 과 파라미터 튜닝이 중요한 것이 아닌 데이터셋 자체에서 인사이트를 도출하고 활용하는것이 데이터 분석가로서 중요한 역량이라는 것을 알게됨.

<br>
<br>

<div class="image-container">
  <img src="https://user-images.githubusercontent.com/93497667/232216526-99e27c85-daac-4a25-b49a-73c3848aaf25.jpg" alt="image"  width="400"/>
  <img src="https://user-images.githubusercontent.com/93497667/232216651-c00ad08b-0d94-43ef-998b-8851b734d169.jpg" alt="image"  width="400"/>
</div>


- [커널밀도분석(KDE)](https://www.notion.so/TMP-e977f66c09ee453b9e2c05d3869ff5e9?pvs=4)
