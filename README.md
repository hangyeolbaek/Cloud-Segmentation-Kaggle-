# Cloud-Segmentation-Kaggle-
Cloud Segmentation Project on Kaggle Competition, In the Course on Python Programming using Google Colab: Computer Vision, Hanbat National University.


[데이터 전처리, 네트워크 설계, 학습 방법을 결정하기 위한 분석 자료]
Learning rate
부정확한 레이블 확인
이상치(outlier) 확인


[사용한 방법]
batch 10, epoch 4, train data rate 0.1 (avoid overfitting)
deeplabv3 model
데이터 증대 (+ A.ElasticTransform(p=0.3)) (to increase the diversity of your training data and improve the model's generalization ability.)
Filter 44 to 64 (By using more filters, the network can learn more complex representations.)



[코드 명 (모델/알고리즘/패키지 이름)]
(deeplabV3/Resnet-101/Semantic-Segmentation-Suite)



[어려웠던 점]
https://github.com/GeorgeSeif/Semantic-Segmentation-Suite/tree/master/docs 파일들을 사용하고 싶었다. 다양한 모델파일들이 있어 학습 성능 향상을 기대하였다. 하지만 위 repository의 파일들은 tensorflow version 1.15.0 기반으로 작성된 코드들이었고 Colab에서는 tensorflow version 1.x으로 다운그레이드 할 수 없었다. 
DeeplabV3+ model을 사용하고 싶었으나 계속되는 오류를 해결하지 못하였다.
캐글은 GPU 사용시간을 각자에게 일주일에 30시간 제한을 주었다. 처음엔 충분할 줄 알았으나 막상 학습을 돌려보니 더 필요하였다.
Colab에서는 tensorflow version 2.x만 지원하였고 tensorflow version 1.x 기반으로 작성된 github repository의 코드와 호환이 맞지 않았다. 

[배운 점]
Machine learning training에는 캐글이나 코랩보다 리눅스 환경의 데스크탑이 훨씬 편하다고 느꼈다.
데스크탑에서는 Tensorflow, pytorch 버전에 따라 cuda 및 cuDNN 버전도 변경해야 해서 가상환경 설정이 중요하다.
