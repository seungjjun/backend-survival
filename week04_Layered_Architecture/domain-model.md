# 학습 키워드

## Domain Model이란
- 행동과 데이터를 모두 통합하는 도메인의 객체 모델이다.

- 애플리케이션 도메인의 개념, 관계 및 규칙을 나타낸다. 
    - 도메인은 소프트웨어를 개발하는 대상 영역으로 생각 = 문제 영역을 개념적으로 모델링한 것

### DDD란
- Domain-Driven Design의 약자로 도메인 주도 개발을 의미한다. 

- DDD는 문제를 도메인 중심으로 사고하여 핵심 도메인과 그 로직에 집중하여 복잡한 시스템을 단순화 하는 것을 목표로 한다.

- DDD를 하기 위해서는 비즈니스 도메인에 대한 이해가 높아야 하고, 문제상황을 정확히 파악해야 한다.

## JPA Entity와 DDD Entity의 차이점
- JPA Entity의 주요 목적은 관계형 데이터베이스에서 스키마를 일치시키고 데이터를 유지하는데 있다.

- 반면 DDD Entity의 주요 목적은 Entity안에 상태와 행위를 모두 포함시켜 도메인관련 비즈니스 로직을 캡슐화하여, Entity가 도메인 로직에 집중 되도록하는데 있다.

## Repository
- 도메인 모델을 관리하는 영역으로 도메인 모델이 비즈니스 로직에 집중할 수 있도록 한다.

- 도메인 Entity의 생명주기, 검색등을 관리한다.

## VO(Value Object)
- 고유한 ID가 없지만 해당 속성 또는 특성에 의해 정의되는 객체이다. 
    - 예를 들면 날짜, 주소 또는 화폐가 있다.

### VO 특징
- 불변성 : VO는 일반적으로 불변성의 특징을 랒고 있다. 
- 동등성 : VO는 비교할때 메모리 주소가 아닌 속성을 기준으로 비교 되기 때문에 모든 속성이 같을 경우 동등하다고 본다. 고유한 id를 갖고 있는 Entity와는 다르다.
- 재사용성 : VO는 속성으로 정의하기 때문에 다른 도메인 모델에서도 재사용 할 수 있다. 

## 정적 팩토리 메서드
- 정적 팩토리 메서드는 해당 클래스의 인스턴스를 만들기 위해 정적 메서드를 만드는 방법으로 객체 지향 프로그래밍의 디자인 패턴 중 하나이다.

### 정적 팩토리 메서드의 장점
- 메서드가 호출될때마다 새로운 객체를 생성하지 않는다.

- 생성자와 다르게 메서드의 이름을 통해 메서드의 목적을 설명할 수 있어 가독성이 향상한다.