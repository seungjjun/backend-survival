# 학습 키워드
## Java HTTP Server
- Java HTTP Server: Java의 HTTP 서버는 HTTP 서버를 쉽게 생성하고 HTTP 요청을 처리할 수 있도록 자바에서 제공하는 클래스이다. HTTP Server를 통해 우리가 흔히 아는 웹 애플리케이션이나 REST API를 만들 수 있다.

## Java NIO
- Java NIO : NIO(New Input/Output)는 Non-Blocking 방식을 지원하는 특징을 갖고 있다. 즉, Java의 프로그램이 NIO를 통해(비동기 처리) 좀 더 효율적으로 입출력 작업을 수행할 수 있도록 도와준다.
- NIO의 주요 특징 중 하나로 channel을 사용한다는 것이다.
    - Channel : 채널이란 읽고 쓸 수 있는 양방향 데이터 스트림을 의미한다.


## Java Lambda expression(람다식)
- 람다식은 자바 8에서 도입된 주요 기능 중 하나로 함수형 프로그래밍에서 기존 코드보다 더 간결하게 표현할 수 있도록 도와주는 방법이다.

- 람다식의 간단한 예로 아래와 같이 numbers 리스트에서 2의 배수의 숫자들만 찾아서 더하는 식을 간단하게  표현할 수 있다.
```
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);

int sum = numbers.stream()
    .filter(n -> n % 2 == 0)
    .mapToInt(Integer::intValue)
    .sum();
```


### Java Functional interface(함수형 인터페이스)
- Java에서 함수형 인터페이스란 단 하나의 추상 메서드만 있는 인터페이스를 말한다. 추상 메서드 외에도 기본 (default) 메서드, 정적 (static) 메서드도 포함될 수 있다. 
- 함수형 인터페이스는 보다 더 간결하고 유연한 코드를 작성할 수 있도록 도와준다.

- 함수형 인터페이스의 장점
    - 간결한 코드 : 함수형 인터페이스를 사용하면 람다 표현식을 사용할 수 있어 보다 간결하고 가독성이 좋은 코드를 작성할 수 있다. 즉, 유지 관리하기가 더 쉽다.
    - 유연한 코드 : 함수형 인터페이스는 데이터 필터링, 컬렉션 정렬 등 다양한 상황에서 사용할 수 있어, 상항에 맞게 코드를 작성할 수 있다. 
