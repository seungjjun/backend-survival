# 학습 키워드

## 전술적 설계 (Tactical Design)
- DDD Lite, Model Driven Design이라고도 불린다.

- 매우 작은 규모의 설계 및 코드를 작성할때 유용한것이 전술적 설계이다.

- 보편 언어를 통해 도메인 모델을 발견때, 이를 설계와 코드에 반영하는것이 **모델 주도 설계(Model Driven Design)** 이다.

## 엔티티 (Entity) vs 일반적으로 이야기하는 개체 (Entity)
### DDD의 Entity
- OOP의 Entity는 속성이 아니라 얼마나 연속적인지, 어떻게 식별할 수 있는지(고유한 식별자)에 따라 정의된다.

- 예를들어, 홍길동이라는 사람이 키가 큰다고 해도 (속성이 변해도) 홍길동은 홍길동인것 처럼 속성이 변한다고 해도 Entity가 변하는 건 아니다.
    - 속성의 변경에 관계없이 존재하는 동안 일정하게 유지되는 아이덴티티로 특징지어진다.

- 식별자(identifier = ID)가 존재하고, 동일성(identity)을 확인한다면 Entity라고 할 수 있다.

- 더 거칠게 이야기하면 고유한 ID를 가진 도메인 객체를 나타내는데 사용되는 개념이다.

## 값 객체 (Value Object, VO)
- 연속성과 식별성이 중요하지 않은 객체
    - 즉, A라는 객채와 B라는 객체의 속성이 같으면 다르다고 볼 필요가 없는 객체
    - 예를 들어, 내가 갖고 있는 100원 동전 객체와 땅에 떨어진 100원 동전 객체를 다른 객체로 볼 필요없이 똑같은 100원의 가치를 갖고 있는 동전 객체로 바라보면 된다.

- Entity와 VO는 바로 어떤것이 Entity이고 어떤것은 VO로 나눠지지 않고 **어떤 비즈니스 도메인**인지에 따라 달라진다.

- VO는 속성을 통해서 동등성(Equality)을 판단한다.
    - 그래서 VO는 항상 Java의 equals메서드를 구현해야 한다.

- 예측 가능성을 높이고 혼란을 막기 위해서 가능한 **불변 객체**로 만들어야 한다.

## 동일성(Identity)과 동등성(Equality)
- Entity는 **동일성(identity)** 을 비교하여 판단, VO는 **동등성(Equality)** 을 비교하여 판단

### Identity 
- Identity는 객체를 다른 객체와 구별하고 별도의 개체로 식별할 수 있게 해준다.

- 예를 들어, 동일한 속성(이름, 나이)을 가진 "Person"이라는 객체를 두개 생성할 경우 이 두 객체는 동일한 값을 가질 수 있지만 서로 다른 Identity를 가진 다른 객체로 구별이 된다.

### Equality
- Equality는 두 객체 간의 비교를 의미하여, 값이나 속성 측면에서 비교하여 동일한지를 판단한다.

- 예를 들어, "Person" 클래스의 두 객체가 있을 때, 서로 다른 ID를 가지고 있더라도 속성(이름, 나이)이 동일한 값을 가지면 동일한 것으로 판단한다.