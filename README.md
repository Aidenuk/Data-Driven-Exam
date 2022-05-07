# Data-Driven-Exam
due 17th of May





Regression (회기분석)

* 회기란 말은 어딘가로 돌아간다는 의미
* 도대체 어디로 돌아가길래 이런 이름이 붙었을까 ?

회기분석의 목적 

* 주어진 (독립)변수로 (종속)변수를 예측학 위해 -> 독립변수란(Independent) : 영향을 주는 변수(원인) / 종속변수란(Dependent) : 영향을 받는 변수(결과) 

* 단순회귀(Simple regression) : 독립변수 1개 & 종속변수 1개
* 다중회귀(Multiple regression) : 독립변수 2개 이상 & 종속변수 1개


<img width="1245" alt="스크린샷 2022-05-03 15 22 46" src="https://user-images.githubusercontent.com/84698855/166473368-bf5f28c3-b3be-416a-ad75-0ee8cfd10230.png">

위에 데이터를 토대로 새로운 데이터를 추론할 수 있다. (different value of independent)

-> 새로운 데이터를 예측하기 위해 필요한 것 : 추세선 (이 추세선을 예측하느 것이 회귀분석의 최종 목적 !)


추세선 
->  y = a + bx ( y is dependent x is independent ) we need a and b value. [ a 는 절편 b 는 기울기 ] 
a 와 b 의 값을 구하는것이 회귀분석 

<img width="792" alt="Screenshot 2022-05-03 at 15 35 48" src="https://user-images.githubusercontent.com/84698855/166474328-bed5aca1-7cc4-4b78-8863-33b19421257e.png">




y hat = a + bx is 추세선 / y = a + bx is 점들( i 들은 점들의 개별의 값)


<img width="797" alt="Screenshot 2022-05-03 at 15 39 27" src="https://user-images.githubusercontent.com/84698855/166475005-2e1c96cf-378d-4f6b-a4f5-aeb9476053fe.png">





가장 완벽한 추세선 즉 좋은 추세선은 에러의 차이가 적은것 
-> 에러를 줄이기 위해서 최소제곱법을 이용한다 ( 즉, 점들은 + 또는 - 에 위치해서 제곱을 시켜줌으로써 뭉개지지 않게 하는 것이 목표, 오차를 적게만드는 것 ) 모든 점들을 제곱후 점의 개수만큼 나누기
[ 모든 것을 다 더하면 가능 ] 
cost(a,b) 의 값이 추세선과 가까울 수록 0의 수렴 반대로 0에서 커질수록 오차 범위 큼

오차값 = 측정값 - 예측값 ( e = yi - yi hat) 





Classification (분류) 

말 그대로 분류를 뜻하는 classfication 은 지도학습의 일종으로 기존에 존재하는 데이터의 category관계를 파악하고, 새롭게 관측된 데이터의 category를 스스로 판별하는 과정이다. 

예를들어 문자를 판별하여, 스팸 보관함으로 분류하는것과 같은 단일분류와, 수능 점수가 몇 등급에 해당하는지 판별하는 종류의 다중분류가 있다. 다중분류는 비지도학습의 clustering 과 비슷하지만, 
가장 큰 차이점은 category의 도메인이 정의되있는가 그렇지 않은가 이다. 

지도학습의 classification 은 이미 정해진 카테고리(레이블) 안에서 학습하여 새로운 데이터르 분류하지만, 비지도학습의 clustering은 정해지지 않은 카데고리(레이블)르 원하는 만크 생성하여, 분류하는 것이 가장 큰 차이점이다. 


Classification 알고리즘 종류 

(1) K -nearest neighbor 
KNN 은 데이터를 분류하고 새로운 데이터 포인트의 카테고리를 결정할 때 K 개의 가장 가까운 포인트를 선점하고 그중 가장 많이 선택된 포인트를 카테고리로 이 새로운 데이터를 분류하는 방법이다. 
KNN 에서 고려해야 할 사항은 알고리즘의 핵심 부분의 대상 포인트와의 거리 대한 측정이고, 이를 계산하는 방법으로 무조건 유클리드 거리 측정 방식을 사용하는 것을 자제해야한다. 

모든 데이터 열을 이처럼 같은 방식으로 처리하면 생각하지 못한 변수에 의해 오류가 생길 수 있으므로 거리의 제곱을 합산학 전 각 카테고리에 대한 평규 거리를 빼고 계산하는 방식과 같은 다양한 거리 계산 알고리즘의 대한 논의가 필요하다. ex) 실수 데이터의 경우 유클리드 거리 측정방식을 사용하고 범주형 혹은 이진 데이터와 같은 유형의 데이터는 해밍거리 측정 방식을 사용한다. 


<img width="674" alt="스크린샷 2022-05-05 16 15 06" src="https://user-images.githubusercontent.com/84698855/166955673-8be6c5dc-aba7-4a84-8bfc-67490dab95e2.png">

(2) Naive Bayes 

나이브 베이즈는 확률을 사용한다. 
ex) 만약, 심슨에 대한 feature에 age와 sex 2개가 존재하는 상황에서, 심슨으 나이, 성별에 따라 살아남을 확률은 알마인지 계산 


<img width="656" alt="스크린샷 2022-05-05 16 17 42" src="https://user-images.githubusercontent.com/84698855/166956142-f4dc5af7-e89b-4f45-a3b6-4f896d750112.png">





Gaussian Mixture Model (GMM) with clurstering 

<img width="702" alt="Screenshot 2022-05-07 at 10 23 42" src="https://user-images.githubusercontent.com/84698855/167248078-f496e96b-debf-4f2e-bea8-d27cf2c34dc8.png">

가우시안 분포가 여러 개 혼합된 clustering 알고리즘이다. 현실에 존재하는 복잡한 형태의 확률 분포를 그림과 같이 K개의 gaussian distribution을 혼합하여 표현하자는 것이 GMM의 기본 아이디어이다. (이때 K는 데이터를 분석하고자 하는 사람이 직접 설정해야한다.) 

주어진 데이터 x에 대해 GMM은 x가 발생할 확률을 아래 식 과 같이 여러  Gaussian probability density function 의 합으로 표현한다. 

<img width="663" alt="Screenshot 2022-05-07 at 10 27 42" src="https://user-images.githubusercontent.com/84698855/167248212-c273fb17-9f06-46a5-9f05-b1c8f90163a1.png">


위에 식에서 mixing coefficient 라고 하는 Pie k 는 K번째 gaussian distribution이 선택될 확률을 나타낸다. 따라서 pie k는 아래의 두 조건을 만족해야 한다. 

<img width="450" alt="Screenshot 2022-05-07 at 10 30 33" src="https://user-images.githubusercontent.com/84698855/167248328-a79de133-d4ce-44aa-8393-2ce1d03ad025.png">




