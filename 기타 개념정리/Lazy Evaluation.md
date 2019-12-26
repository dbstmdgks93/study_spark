# Lazy Evaluation

출처: https://dororongju.tistory.com/137 

Lazy 방식은 당장에 해결해야할 문제들이 차례로 주어지더라도 마지막 문제를 제공받을 때 까지 게으르게 기다리다가 마지막 문제를 알게되면, 그때 연산을 시작함으로써 결과를 얻기 위해 필요하지 않은 연산은 수행하지 않게 됩니다.



아래의 코드는 **1~10까지의 정수를 갖는 List**에서 6보다 작고, 짝수인 요소를 찾아 10을 곱한 리스트 중 **첫 번째 요소**를 출력하는 코드입니다.

```java
final List<Integer> list = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
 
System.out.println(
    list.stream()
        .filter(i -> i<6)
        .filter(i -> i%2==0)
        .map(i -> i*10)
        .findFirst()
        .get()
);
```

당연히 결과는 다음과 같습니다.

```java
20
```



위의 코드가 만약 **Eager Evaluation** 방식으로 동작한다면,

1. 모든 요소들에 대해 6보다 작은지 체크해야하고,

2. 1번에서 구한 모든 요소들에 대해 짝수인지 체크해야하고,

3. 2번에서 구한 모든 요소들에 10을 곱해주고,

4. 3번의 요소들 중 첫 번째 요소를 반환해야 합니다.

실제로 어떻게 동작하는지 살펴보기 위해 코드를 수정해서 실행시켜 봅시다.

```java
final List<Integer> list = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
 
System.out.println(
    list.stream()
        .filter(i -> {
            System.out.println("i < 6");
            return i<6;
        })
        .filter(i -> {
            System.out.println("i%2 == 0");
            return i%2==0;
        })
        .map(i -> {
            System.out.println("i = i*10");
            return i*10;
        })
        .findFirst()
        .get()
);
```

```java
i < 6
i%2 == 0
i < 6
i%2 == 0
i = i*10
20
```

순차적으로 연산을 진행하다가 원하는 값인 첫 번째 요소의 값을 구하면 나머지 연산을 피하는 것을 볼 수 있습니다.



