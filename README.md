# [차종 분류 EfficientNet 모델]

## * 본 프로젝트의 기획의도
 
 ### **"최대한 많은"** 차종을 구분하는 분류 모델 제작
- 최적화된 이미지 처리 방식 찾기
- 클래스의 최대 갯수 찾기 

 

## 1. 데이터: AI-hub data (korean) - 70GB --> 8~9GB

    - 322,664개 
    - 자동차 브랜드, 모델, 연식, 색상, 트림 종류 별 데이터셋 ( 차종 100종, 3099대)
    - 차량 외관 파트 라벨링(15 종류): 프론트범퍼, 리어범퍼, 타이어, A필러, C필러, 사이드미러, 앞도어, 뒷도어, 라디에이터그릴. 헤드램프. 리어램프. 보닛, 트렁크, 루프

## 2. EfficientNET 모델 

    -Reference: https://debuggercafe.com/stanford-cars-classification-using-efficientnet-pytorch/
    -pytorch
    
## 3. Model evaluation
    
    -Accuracy, Loss, Confusion Matrix, Class activation map
    -Tensorboard

## 4. Procedure and Methods  

![데이터 처리 방식 별 차종 분류 절차](https://user-images.githubusercontent.com/51395479/207801862-b03434fd-80a2-48c9-88cd-48a33307f600.png)

### (1) 차량 방향 별 이미지 분류 방식 비교 
- 현대 자동차 Only, 데이터 숫자 50 미만 클래스 drop 

![차량방향별 이미지 분류 방식 ](https://user-images.githubusercontent.com/51395479/207801886-5fb41d91-b1e8-4916-b86d-8d308deab9b3.png)
     
### (2) 브랜드별 분류 방식 비교

- **브랜드 + 모델 + 연식** (트림, 색상 구분X) 

![브랜드 별 이미지 분류 방식](https://user-images.githubusercontent.com/51395479/207801870-8c92da23-9f6e-4f2a-aac9-cac3c51c5ae4.png)

