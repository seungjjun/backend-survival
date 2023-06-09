# 학습 키워드

## Value Object
- 식별자가 없는 값만 갖고 있는 객체

- Value Object를 이용해 객체의 목적에 맞는 행위를 위임하여 책임 분리를 할 수 있다.

- 예를 들어 Age라는 VO에 나이를 더하는 메서드를 만들어 나이에 관련된건 Age에게 위임하여 책임을 분리

- VO를 이용하면 도메인 객체를 생성할 때 파라미터로 들어오는것들이 무엇인지(어떤 타입인지) 알 수 있도록 명시해줄 수 있다.

- VO를 잘 활용하면 단일책임원칙을 따를 수 있다.

## Aggregate Mapping
- Aggregate Mapping은 Hibernate 또는 JPA 같은 ORM 프레임워크에서 제공하는 기능이다.

- Value Object를 JPA에서 지원할수 있도록 하는 기술이다.

- Aggregate라고 하는 복잡한 값 객체를 데이터베이스 테이블의 단일 열 또는 열 집합에 매핑할 수 있다.

- 객체 지향 프로그래밍에서 Aggregate는 관련 특성 또는 속성 그룹을 캡슐화하는 객체이다.

- Aggregate는 값 객체 또는 Entity의 구성요소가 될 수 있다.

- Aggregate Mapping을 사용하면 Aggregate를 데이터베이스 테이블의 하나 이상의 열에 매핑할 수 있다.

## JPA 어노테이션
### @Entity
- JPA가 @Entity 어노테이션이 붙은 클래스를 데이터베이스 테이블의 엔티티로 사용하도록 설정하는 어노테이션

- 기본 생성자가 필수이다. (객체 생성을 위함)

### @Table
- @Entity 테이블의 세부사항을 설정하는데 사용하는 어노테이션으로 테이블의 이름, 인덱스 등등 테이블과 관련된 속성을 지정할 수 있다.

### @Id
- @Id 어노테이션이 붙은 필드를 테이블의 기본 키로 설정하는데 사용한다.

- 모든 테이블에는 기본 키가(고유한 식별하는 기본 키) 있어야 하기 때문에 기본 키 설정은 필수적이다. 

### @Embeddable
- @Embeddable 어노테이션이 붙은 클래스가 다른 엔티티 속성에 하위 속성 개념으로 다른 엔티티에 포함될 수 있도록 설정한다.

- @Embeddable이 설정된 객체는 @Embedded 어노테이션이 명시된 필드의 인스턴스를 보유하여 테이블에 @Embeddable 속성들이 매핑이된다. 

### @Embedded
- @Embedded는 @Embeddable의 인스턴스를 보유하고 있는 객체를 나타낼 때 사용한다. 즉 값 객체를 사용하는 필드에 명시한다.

- JPA가 자동으로 @Embedded 어노테이션이 붙은 필드를 @Embeddable 어노테이션이 설정된 객체를 테이블에 매핑한다.
