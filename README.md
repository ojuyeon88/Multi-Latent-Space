# Multi-Latent-Space

## Introduction
기존의 Autoencoder는 encoder-decoder의 구조를 통해 입력 데이터를 더 작은 차원의 latent space(이하 잠재 공간)을 압축-복원하는 작업을 거쳤다. 

해당 아이디어(다중 잠재공간; Multi Latent Space)는 여러 개의 잠재 공간을 도입하여 각 잠재 공간이 입력 데이터의 특정 특징에 수렴하도록 하여, 고차원 데이터의 복잡한 특징을 계층적으로 학습하게 돕는다. 고차원 데이터의 특징을 계층적으로 학습함으로써 보다 향상된 복원률과 효율성을 달성하자는 아이디어에서 개발되었다. 

이를 통해 향상된 이미지 복원률, 빠른 학습 및 복원 속도, 특징 표현의 세분화 및 효율적 데이터 압축을 기대한다.

## Proposed Method 
![image](https://github.com/user-attachments/assets/dfc5c238-2755-428b-8fda-7af55310ec86)
- 다중 Latent space를 통한 복원 이미지 품질 향상
- i개의 개별 잠재 공간을 통합하여 전체 잠재 표현 Z를 구성

## Results
![image](https://github.com/user-attachments/assets/9218d004-c46d-45d1-856d-42597fcc1503)
![image](https://github.com/user-attachments/assets/8f9a44b1-fcda-4d5a-86a2-204bfd77c319)
- 기존 Autoencoder 모델과 제안된 모델의 Output 비교 후 정량적, 정성적 평가 진행
- 기존 Autoencoder의 경우 4와 9의 군집이 명확히 분류되지 않는 한계점을 지님
- 제안된 모델의 경우 각각의 군집을 기존 모델보다 올바르게 분류

## Conclusion
- 데이터를 다중 Latent Space로 매핑하여 세부적 특징을 독립적으로 학습
- 평균 제곱 오차(MSE)를 최소화를 통한 잠재 공간 개수 최적화, Overfitting 없이 안정적으로 높은 복원 성능
- 숫자 4와 9처럼 유사한 데이터에서 기존 모델 대비 명확한 구분 및 복원 성능 입증
- 모델의 처리 속도 향상 및 초고차원 데이터 복원을 위한 새로운 설계 방안과 최적화 기법 요구됨
