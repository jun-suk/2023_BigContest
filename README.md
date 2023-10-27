# 2023_BigContest
정형데이터분야 어드밴스드리그  
![bigcon23](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/43638b26-f2b1-447d-911d-b09c9246f169)  
[발표자료](https://github.com/jun-suk/PJT_2023_BigContest/blob/main/%5B%E1%84%87%E1%85%A1%E1%86%AF%E1%84%91%E1%85%AD%E1%84%8C%E1%85%A1%E1%84%85%E1%85%AD%5D%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%92%E1%85%A7%E1%86%BC%E1%84%83%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%90%E1%85%A5%E1%84%87%E1%85%AE%E1%86%AB%E1%84%8B%E1%85%A3_%E1%84%8B%E1%85%A5%E1%84%83%E1%85%B3%E1%84%87%E1%85%A2%E1%86%AB%E1%84%89%E1%85%B3%E1%84%83%E1%85%B3%E1%84%85%E1%85%B5%E1%84%80%E1%85%B3_%E1%84%90%E1%85%B5%E1%86%B7_%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%A5%E1%84%83%E1%85%B3%E1%84%85%E1%85%B5%E1%86%B7.pdf)  

[결과보고서](https://github.com/jun-suk/PJT_2023_BigContest/blob/main/%5B%E1%84%80%E1%85%A7%E1%86%AF%E1%84%80%E1%85%AA%E1%84%87%E1%85%A9%E1%84%80%E1%85%A9%E1%84%89%E1%85%A5%5D%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%92%E1%85%A7%E1%86%BC%E1%84%83%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%90%E1%85%A5%E1%84%87%E1%85%AE%E1%86%AB%E1%84%8B%E1%85%A3_%E1%84%8B%E1%85%A5%E1%84%83%E1%85%B3%E1%84%87%E1%85%A2%E1%86%AB%E1%84%89%E1%85%B3%E1%84%83%E1%85%B3%E1%84%85%E1%85%B5%E1%84%80%E1%85%B3_%E1%84%90%E1%85%B5%E1%86%B7_%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%A5%E1%84%83%E1%85%B3%E1%84%85%E1%85%B5%E1%86%B7.pdf)  

[코드](https://github.com/jun-suk/PJT_2023_BigContest/blob/main/%5B%E1%84%8F%E1%85%A9%E1%84%83%E1%85%B3%5D%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%92%E1%85%A7%E1%86%BC%E1%84%83%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%90%E1%85%A5%E1%84%87%E1%85%AE%E1%86%AB%E1%84%8B%E1%85%A3_%E1%84%90%E1%85%B5%E1%86%B7_%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%A5%E1%84%83%E1%85%B3%E1%84%85%E1%85%B5%E1%86%B7.ipynb)
<br>

### 0. 파일 설명

- Area.py : openCV를 활용하여 좌석별 시야 이미지로부터 보이는 무대면적을 수치화하는 파일

<br>

### 1. 대회 주제

- 예술의전당 콘서트홀 좌석 그룹핑
- 공연별/좌석별 적정 가격을 도출할 수 있는 가격모델 제시

<br>

### 2. 대회 기간

- 참가접수: 2023년 7월 31일 ~ 9월 15일
- 제출마감일: 2023년 9월 27일

<br>

### 3. 가설 도출

- 논문 및 공연예술관련 대학 교본으로 리서치로 가설 도출
    - 공연예술상품은 **고객의 최대지불용의금액을 기반으로 거래가격이 설정**됨.
    - 객석의 차등가격의 근거로 **무대사시권, 무대인접권, 음향 청음권**을 사용한다.
    - 비관객 설문조사에서의 최대지불용의금액은 실제 예술의전당 좌석가격보다 높으나 비싸다고 생각하고 알아보지 않고 있다.
    - 예술의 전당 개관 35주년 인터뷰에서 장형준 사장님은 관객과 함께하는 예술의전당을 강조하였다.
    
- 문제정의
    - 기존 좌석등급은 공급자 위주로 결정되고 있다. 가격에서 중요한 역할을 하는 관객의 지불용의 금액은 서비스에 영향을 받지 않고 있다.

- 가설
    - 좌석 등급과 등급 간 가격차이에 대한 근거가 관객이 이해할 수 있을정도로 명확하다면 만족도와 지불용의금액이 증가할 것이다.

<br>

### 4. 프로젝트 목적

- 좌석 선호도를 등급 배분 및 좌석등급간 가격차의 근거로 활용하여 관객 의사를 직간접적으로 반영
    - 가정 : 고객의 좌석예매 순서는 해당 공연에 대한 좌석 선호도를 내표하고 있다.
- 실제 예술의전당에서 활용할 수 있도록 기존 공연기획 프로세스에 바로 포함될 수 있고, 쉽게 이해가능한 모델 설계

<br>

### 5. 프로젝트 내용

- 중요 파생변수
    - **(무대인접권)** 예술의전당 홈페이지에서 제공하는 엑셀 좌석배치도를 통해 각 좌석의 x, y, z 좌표를 생성
        
        ![엑셀 배치도](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/713677b8-415e-4ca8-9d3b-bc23d1c56753)
        
    - **(무대사시권)** openCV를 통해 ‘Area.py’파일을 만들어 예술의전당 홈페이지에서 제공하는 좌석별 시야 이미지에서 보이는 무대바닥면적을 수치화해서 활용
        
        ![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/d7e0969f-32b9-40c1-8cfd-67ab70b5dd80)
        
        - 클릭을 통해 빨간점을 찍고, 연한 초록색 면적이 계산되어 feature로 활용할 수 있도록 코딩


    - **(고객 선호도)** 공연별 예매순서를 느린 순으로 랭크(cumcount)하여 고객선호도를 수치화
        - 예매되지 않은 좌석 ==  0
        - 제일 늦게 예매된 좌석 == 1
        - 제일 빠르게 예매된 좌석 == {해당 공연의 총 예매좌석수}

<br>

- 공연 클러스터링
    - '예매가 빨리 된 좌석일수록 고객 선호도가 높은 좌석'이라는 가설을 세움.
    - 공연별 예매 순서를 기준으로 좌석 선호도의 분포가 비슷한 공연끼리 클러스터링함.

        ![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/e2c37b73-7bad-4bbd-8a68-d2c1f64712a5)

<br>


- 공연 클러스터별 주요 변수 파악
    - 1)에서 만든 공연 클러스터별 좌석 가치 판단요소(좌석 시야, 가로거리, 가로 방향(무대기준 좌,우), 세로거리, 세로 방향(무대기준 앞, 뒤), 층고)이 좌석 선호도에 미치는 영향의 크기와 양, 음의 상관관계를 파악하고, 이를 수치화함.
        - 클러스터 3(마지막 시각화)의 SHAP Value
            
            ![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/630d1064-cc95-4813-bcb4-f906a65251f2)
            
        
- 좌석등급 분배
    - 선호도 순으로 좌석의 등급을 지정하되, 등급별 좌석의 갯수는 기존 예술의전당에서 적용중인 등급별 허용좌석수를 참고함.
    - 등급별 선호도 평균의 차를 통해 등급간 가격 차이 산정
        
        ![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/0b3e1184-d5d1-4099-9939-9165e524c28c)
        
        ![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/ef77a68b-f129-4250-870f-3a31bdbf41c0)
        
        ![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/0ceb632d-c77d-47f5-9e47-3456738d40a5)
        

- 데이터 외 예술의전당 공연에 적용(simulation)
    - 선우예권 피아노 리사이틀(10/18, 수) 공연정보를 통해 모델 시현
        - XGB를 통해 기본정보를 활용하여 어떤 클러스터에 해당할지 분류
            
            ![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/579d0b6b-e042-459f-a0da-9f4b8d7260b1)
            
- 최종 예매창 예시

![Untitled](https://github.com/jun-suk/PJT_2023_BigContest/assets/73885257/acc43e25-1cba-4226-af7f-ec15ecb41818)

### 6. 기대효과

- 높은 실현가능성
    - 기존 공연기획 프로세스를 해치치 않으며 서비스 가능
- 산정 근거 제공
    - 좌석 선호도, 변수 영향력 등이 수치화되어있기에 관객이 이해가능한 형태로 제공 가능
- 기존 방식과 시너지
    - 대회에서 제공된 데이터 외 정보(목표객단가, 고정비, 연주자 등급 등)이 포함되면 성능이 높아질 것으로 예상
- 관객이 먼저
    - 관객의 예매순서로 가중치가 정해지기때문에 예매 데이터가 쌓일수록 피드백이 지속적으로 업데이트되면서 최적의 가격 및 분포가 도출될 수 있음.
