![intro](https://user-images.githubusercontent.com/51395479/207835391-7aa4821a-e901-4074-bbd9-244b28c49e0c.png)


# **0. 본 프로젝트의 기획의도**
 
  ### **"최대한 많은"** 차종을 구분하는 분류 모델 제작
 
 매년 수백 여대의 신차가 쏟아지기 때문에 분류해야할 차종의 수도 많고 매년 새롭게 추가해야합니다. 만약 학습이 효율적이지 않다면 모델을 유지, 보수하는데 많은 인력과 비용이 소모되게 됩니다. 따라서, 본 프로젝트에서는 최대한 많은 자동차 종류를 분류할 수 있고 이미지 전처리 단계가 비교적 간단한 차종 인식 분류 모델을 만들어 보고자 합니다. 

 

# **1. 데이터: AI-hub data (korean) - 70GB --> 8~9GB**

    - 322,664개 
    - 자동차 브랜드, 모델, 연식, 색상, 트림 종류 별 데이터셋 ( 차종 100종, 3099대)
    - 차량 외관 파트 라벨링(15 종류): 프론트범퍼, 리어범퍼, 타이어, A필러, C필러, 사이드미러, 앞도어, 뒷도어, 라디에이터그릴. 헤드램프. 리어램프. 보닛, 트렁크, 루프

# **2. EfficientNET 모델** 

    - EfficientNET B0 (input: 224x224)
    - Reference: https://debuggercafe.com/stanford-cars-classification-using-efficientnet-pytorch/
    -pytorch
    
# **3. Model evaluation**
    
    -Accuracy, Loss, Confusion Matrix, Class activation map
    -Tensorboard

# **4. Procedure and Methods**  

<img src="https://user-images.githubusercontent.com/51395479/207801862-b03434fd-80a2-48c9-88cd-48a33307f600.png" width=820 height=300/>

### (1) 차량 방향 별 이미지 분류 방식 비교 
- 현대 자동차 Only, 데이터 숫자 50 미만 클래스 drop 

<img src="https://user-images.githubusercontent.com/51395479/207801886-5fb41d91-b1e8-4916-b86d-8d308deab9b3.png" width=820 height=380/>

     
### (2) 브랜드별 분류 방식 비교 ('차량 전체' 방식 적용)

- **브랜드 + 모델 + 연식** (트림, 색상 구분X) 

<img src="https://user-images.githubusercontent.com/51395479/207801870-8c92da23-9f6e-4f2a-aac9-cac3c51c5ae4.png" width=820 height=400/>


# **4. Results** 

### (1) 차량 방향 별 이미지 분류 방식 비교 

<img src="https://user-images.githubusercontent.com/51395479/207839658-edfb12c2-3bdd-4b66-83dd-99a24536df28.png" width=820 height=400/>


### (2) 브랜드 별 분류 방식 비교 ('차량 전체' 방식 적용)

<img src="https://user-images.githubusercontent.com/51395479/207839647-a283d967-4bb5-4052-8f68-c0b707b14f58.png" width=820 height=400/>


# **5. Class Activation Map** 


<img src="https://user-images.githubusercontent.com/51395479/207841666-0da346a6-b149-4a50-bbca-d811843b66ff.png" width=1200 height=520/>
