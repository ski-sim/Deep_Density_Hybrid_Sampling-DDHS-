# Deep_Density_Hybrid_Sampling-DDHS-
Learning From Imbalanced Data With Deep Density Hybrid Sampling (IEEE 2022) [article link](https://ieeexplore.ieee.org/document/9723474) </br>
### Overview
- Autoencoder 기반의 Embedding Network 를 활용하여 Hybrid Sampling
- Imbalanced Dataset 에 대한 Sampling 후 Linear SVM/Regression 성능 평가 시 SOTA 달성
- Euclidean Distance 를 활용하는 SMOTE 기반의 Over-sampling 방법론의 최대 단점인 High-Dimensional Problem 해결
- 세 가지 Loss Term (CE, Center, Reconstruction) 을 활용하여 Sampling 성능 향상
- Density-based Filtering 으로 Minority Class 의 High-Quality

### High-Dimensional Problem 해결
![image](https://github.com/ski-sim/Deep_Density_Hybrid_Sampling-DDHS-/assets/121158156/059decc0-c7d6-4bd5-9b7a-fdf3bc49689b)
auto-encoder를 이용해 저차원으로 매핑 후 샘플링
-> Reconstruction loss 발생

### 세 가지 Loss Term (CE, Center, Reconstruction)
![image](https://github.com/ski-sim/Deep_Density_Hybrid_Sampling-DDHS-/assets/121158156/d242cae6-e293-424f-b385-81f71d81bf33)

CE (Cross Entropy loss) : 잘못 분류된 데이터 포인트에 더 많은 패널티 부여</br>
Center : class center에 멀리 떨어진 데이터 포인트에 더 많은 패널티 부여
