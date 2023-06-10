# 학습 키워드

## Hexagonal Architecture

- 전통적인 3계층 관점
1. Presentation (UI Layer)
2. Domain (Application Layer + Domain Layer)
3. Data

- 알리스테어 콕번의 논의
1. User-side
2. Application
3. Database-side

- 여기서 Application을 제외한 외부는 여러 개가 존재할 수 있고, 더 추가하기 위해 육각형(Hexagonal)이란 표현을 사용한다.

- 이러한 구분이 필요한 이유?
    - UI와 비즈니스 로직이 섞이는 문제를 해결하기 위해서

- UI와 비즈니스 로직이 섞이는 문제의 해결법은 Layered Architecture이지만, User-side와 Database-side를 완전히 다른 것 처럼 취급하는 경향이 있다.
    - 하지만 단순히 Appication의 외부로 취급하면, 위 둘은 동일한 구조를 갖게된다.
    - Application 입장에서 그놈이 그놈이다.

- 위와 같이 하면 appication이 다른 외부 요소와 분리되어 테스트하기 쉽고, 재사용하기도 좋아진다.

- Hexagonal Architecture를 활용하면 큰 무언가를 얻는게 아닌 UI와 비즈니스 로직이 섞이는 문제를 해결하고, 테스트하기 쉽고 재사용성 좋은 구조를 만들기 위함이다.

- UI Layer에 비즈니스 로직이 없고 Application Layer를 테스트하기 위해 Mocking을 하고 있다면 이미 Hexagonal Architecture를 사용하고 있다고 말할 수 있다.

## POJO
- POJO(Plain Old Java Object)를 의미한다.

- 특정 Java 프레임워크 또는 인터페이스를 확장하거나 구현하지 않는 Java 객체를 나타내는 데 사용하는 용어이다.

- 예를 들어, 필드와 해당 getter/setter 메서드만 존재하는 단순한 객체를 POJO라고 한다.

- 애플리케이션의 비즈니스 논리에 초점을 맞춤으로써 Java 코드의 단순성과 명확성을 장려한다.
