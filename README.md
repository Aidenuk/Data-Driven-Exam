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
-> 에러를 줄이기 위해서 최소제곱법을 이용한다 ( 즉, 점들은 + 또는 - 에 위치해서 제곱을 시켜줌으로써 뭉개지지 않게 하는 것이 목표, 오차를 적게만드는 것 ) 
[ 모든 것을 다 더하면 가능 ] 
오차값 = 측정값 - 예측값 ( e = yi - yi hat) 





