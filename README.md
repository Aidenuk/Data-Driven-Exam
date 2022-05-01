# Data-Driven-Exam
due 17th of May


Data Normalisation (데이터 정규화) / Data standardization (데이터 표준화)

why we need them?

-> 머신 러닝 알고리즘으 기본적으로 데이터를 가지고 무언가를 해내는 친구들이다. 많은 양의 데이터를 가지고 머신기계를 학습시키는 것이 머신러닝, 우리말로느 기계학습이라고 한다.
보통 예측하고자 하는 것과 연관이 있을만한 여러 개의 특성을 가지고 머신러닝 알고리즘을 훈련시킨다.

그렇다면 사람의 학력과 지능 사이 연관이 있을 것과 같은 특성들을 도출한다. 그 사람의 학력, 학교, 공부 기간 등등 하지만 여러가지의 과들이 있듯이 특성의 단위도 다르고 값의 범위도 차이가 있다.

그리고 단위가 같더라도 값으 범위가 크게 차이나느 상황에서도 제대로 비교하느 것이 힘들다. (지방대 의대 vs 서울대 예체능) 

따라서 특성들의 단위를 무시할 수 있도록, 또한 특성들의 값의 범위를 비슷하게 만들어 줄 필요가 있다. 그것이 바로 정규화 또는 표준화가 해주는 일이다. 
정규화와 표준화가 해주는 것을 특성 스케일링(feature scailing) 또는 데이터 스케일링(data scailing) 이라고 한다. 

[정규화 공식]

<img width="316" alt="Screenshot 2022-05-01 at 21 15 54" src="https://user-images.githubusercontent.com/84698855/166163011-19a73966-17a8-4bfa-a012-453093ce265f.png">



이 공식을 사용하면 한 특성 내에 가장 큰 값은 1로, 가장 작은 값은 0 을 변환된다. 이 공식을 이용해서 각 특성들의 값을 변환해주면 모두 [0,1]의 범위를 갖는다. 


[표준화 공식]

<img width="229" alt="Screenshot 2022-05-01 at 21 22 17" src="https://user-images.githubusercontent.com/84698855/166163217-9ef1ec89-9671-4fae-ab3b-5a4ef18b2bc6.png">


여기서 뮤는 한 특성의 평균값이고 분모값은 표준편차이다. 표준화는 어떤 특성의 값들이 정규분포, 즉 종모양의 분포를 따른다고 가정하고 값들을 0의 평균, 1의 표준편차를 갖도록 변환해주는 것이다.
