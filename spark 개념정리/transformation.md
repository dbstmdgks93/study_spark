## transformation (변환)

변환이란 RDD를 가공하고 그 결과 새로운 RDD를 얻는 처리다. 변환처리 후의 RDD가 가지는 요소는 변환처리 전의 RDD에 있던 요소를 가공하거나 필터링해 생성된다.



### transformation 처리 전의 RDD가 가지는 요소를, 같은 RDD의 다른 요소들과 관계없이 처리할 수 있는 종류

#### filter

요소를 필터링한다.

![filter 개요](images/filter%20%EA%B0%9C%EC%9A%94.PNG)

#### map

각 요소에 동일한 처리를 적용한다.

![map 개요](images/map%20%EA%B0%9C%EC%9A%94.PNG)



#### flatmap

각 요소에 동일한 처리를 적용하고 여러 개의 요소를 생성한다.

![flatmap 개요](images/flatmap%20%EA%B0%9C%EC%9A%94.PNG)



#### zip

파티션 수가 같고, 파티션에 있는 요소의 수도 같은 두 개의 RDD를 조합해 한 쪽의 요소 값을 key로, 다른 한 쪽의 요소 값을 value로 가지는 pair를 만든다.

![zip 개요](images/zip%20%EA%B0%9C%EC%9A%94.PNG)



### 변환 전의 RDD가 가지는 요소를 같은 RDD의 다른 요소와 함께 처리하는 변환

- reduceByKey

같은 키를 가지는 요소를 집약처리한다.

![reduceByKey 개요](images/reduceByKey%20%EA%B0%9C%EC%9A%94.PNG)

- join

두 개의 RDD에서 같은 키를 가지는 요소끼리 조인한다.

![join 개요](images/join%20%EA%B0%9C%EC%9A%94.PNG)

##### 출처

아파치 스파크 입문 : 따라 하며 쉽게 익히는 스파크 SQL, 스트림처리, 머신러닝

