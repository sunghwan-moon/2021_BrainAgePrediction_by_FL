## BrainAgePrediction_by_Federated_Learning

이번 프로젝트에서는 연합학습을 활용한 뇌연령예측 모델을 만드는 것을 목표로 하였다.
하지만 아쉽게도 Colab의 개발 환경 특성상 사용할 수 있는 리소스가 제한되어져 있었고
이로 인해 3D Brain MRI를 활용한 예측 모델을 다량의 데이터로 분석하는 것은 불가능했다.



#### 뇌연령 예측 모델은 다음과 같다.

1. 뇌구조학적 데이터를 활용한 Simple MLP 모델
   - Client 수 : 4
   - Client 별 데이터 수 : 100
   - Test 데이터 수 : 93


#### FL 모델 학습 결과
  
1. 뇌구조학적 데이터를 활용한 Simple MLP 모델
   - MAE: 



#### Local과 FL의 성능 비교

Case 1: 환자 수가 적은 병원에서 모델을 돌릴 경우
  - 로컬 Model (N=100)
  - FL Model (N=400)
  - Test N = 93, Epoch = 1000

<<결과>>

(1) 로컬 Model
   - Train MAE : 15.586
   - Test  MAE : 14.554

(2) FL Model
   - Train MAE : 10.272
   - Test  MAE : 9.974
 
 
Case 2: FL의 Client들의 정보의 합과 로컬 병원의 데이터 수가 같을 경우
  - 로컬 Model (N=400)
  - FL Model (N=400)
  - Test N = 93, Epoch = 1000

<<결과>>

(1) 로컬 Model
   - Train MAE : 9.3295
   - Test  MAE : 10.0129

(2) FL Model
   - Train MAE : 9.8939
   - Test  MAE : 9.8630

*7월부터 9월까지 새로 서버와 장비를 할당받아 전반적인 모델을 발전시킬 예정
