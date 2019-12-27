## Action

transformation이 RDD로부터 다른 RDD를 얻는 '데이터 가공'에 해당하는 조작이라면, 액션은 RDD내용을 바탕으로 데이터를 가공하지 않고 원하는 결과를 얻는 조작이다. 액션에는 다음과 같은 것이 있다.

### saveAsTextFile

RDD의 내용을 파일로 출력한다.

![saveAsTextFile 개요](images/saveAsTextFile%20%EA%B0%9C%EC%9A%94.PNG)

### Count

RDD의 요소의 수를 센다.

![count 개요](images/count%20%EA%B0%9C%EC%9A%94.PNG)



### 참고

일부 액션만 소개했다. 다른 변환과 액션들은 스파크의 공식문서를 참고해야 한다.



##### 출처

아파치 스파크 입문 : 따라 하며 쉽게 익히는 스파크 SQL, 스트림처리, 머신러닝



