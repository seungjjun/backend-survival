# 학습 키워드

## N + 1 problem
- N + 1 문제는 특정 엔티티를 조회할때 연관된 엔티티까지 같이 조회하기 위해 N개의 추가 쿼리가 발생하는 문제를 말한다.

- 연관된 엔티티란 @OneToMany나 @ManyToOne 어노테이션으로 엔티티간의 관계를 1:N 또는 N:1으로 설정해준것을 의미한다.

## DDD의 Aggregate
- Aggregate는 도메인 중심 디자인의 패턴이다.

- DDD 집계는 단일 단위로 취급할 수 있는 도메인 개체의 클러스터
    - 예를 들어 주문과 해당 라인 항목은 별도의 개체이지만, 주문(및 해당 라인 항목)을 단일 aggregate로 취급하는 것이 유용하다.

- aggregate는 구성 요소 객체 중 하나가 집계 aggregate가 된다. 

- aggregate 외부의 모든 참조는 aggregate 루트로만 이동해야 하기 때문에 루트는 aggregate 전체의 무결성을 보장할 수 있다.

- aggregate는 도메인 모델 내에서 서로 관련된 객체들을 그룹화하고 캡술화하는데 사용되는 개념인가?

## CascadeType.ALL
- Cascade은 영속성 전이를 의미하며 영속성 전이란 특정한 엔티티에 대해 작업을 수행하면 연관된 엔티티도 동일하게 작업이 수행되는 것을 의미한다.

- CascadeType에는 6가지 종류가 존재
    - ALL : 모든 Cascade를 한번에 적용
    - PERSIST : 엔티티를 영속화할 때, 연관된 엔티티도 함께 영속화
    - MERGE : 엔티티 상태를 병합할 때, 연관된 엔티티도 모두 병합
    - REMOVE : 엔티티를 제거할 때, 연관된 엔티티도 모두 제거
    - REFRESH : 엔티티를 Refresh할 때, 연관된 엔티티도 모두 새로고침
    - DETACH : 엔티티를 detach() 하면, 연관 엔티티도 detach()상태가 되어 변경 사항 반영 되지 않음

## orphanRemoval
- 고아 객체 제거라고 불리는 orphanRemoval는 CascadeType.REMOVE와 비슷하게 부모 엔티티가 삭제되면 자식 엔티티도 같이 삭제가 된다.

- 부모 엔티티에서 제거된 자식 엔티티는 고아가 되므로 데이터베이스에서 고아 객체는 자동으로 제거하는 기능

- CascadeType.REMOVE와의 차이점이라면 CascadeType.REMOVE은 부모 엔티티에서 자식 엔티티를 삭제해도 자식 엔티티가 그대로 남아있지만, orphanRemoval = true로 설정하면 자식 엔티티는 고아 객체가 되어 제거가 된다.

## Event Sourcing
- Event Sourcing은 애플리케이션에서 상태를 변화시키는 이벤트를 순서에 맞게 저장하여 상태를 만들어내는 개발 패턴 중 하나이다.

- 데이터의 상태를 변경시키는 모든 데이터를 저장해서 이후에 다시 replay하여 애플리케이션의 상태를 재구성할 수 있고, 로그로써도 활용이 가능하다.

### @OneToMany
- @OneToMany 어노테이션은 엔티티간의 관계에서 일대다 (1:N) 관계를 정의할 때 사용 된다.

- 예를들어 Team에는 여러 Member가 존재하는것 처럼 두 엔티티간의 관계를 코드로 설정할 때, Team 엔티티에 Member 엔티티를 자식으로 여러개 갖고 있도록 설정할 수 있다. 

### @JoinColumn
- @JoinColumn은 다대일 관계에서 '다'쪽에서 @JoinColumn 어노테이션으로 속성들을 지정해줄 수 있다.

- name 속성을 이용해 조인 하는 열의 이름을 지정할 수 있다.

- 예를들어 Team과 Member의 엔티티 연관 관계에서 Member 엔티티속 선언된 Team 필드에 @JoinColum(name = "team_id") 이런식으로 명시해주면 Member 테이블에는 Team 엔티티를 team_id로 표시가 된다.
    - 즉, Member 테이블에 Team 필드를 어떤 이름으로 표시할 것인지 정해주는 것이다.
