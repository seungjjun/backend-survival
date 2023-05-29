# 학습 키워드

## 리파지터리 (Repository)
- Repository는 Aggregate를 관리하는 Collection처럼 작동한다.
    1. 오직 Aggregate만 Repository를 갖는다.
        - Order aggregate는 Order Repository만 갖는다.

    2. Repository는 영속화 방법 및 기술을 감춘다.
        - Repository는 일반적으로 영속화 방법 및 기술을 감춰 인터페이스로만 구현한다.

- Spring Data JPA는 위 두가지를 만족시키기 위한 기능을 갖고 있다.

- Repository를 전역으로 접근하기 위해 Spring의 DI를 통해서 간단하게 접근 가능하게 할 수 있다.

## Application Layer와 UI Layer
### Domain Layer
- 비즈니스 도메인에 집중한 코드(핵심 비즈니스 로직)를 모아둔 곳

- 문제 도메인의 핵심 개념과 객체를 나타내는 도메인 엔티티를 정의하고 관리한다.

- 아키텍처의 다른 계층과 독립적이다. 

### Application Layer
- Repository와 Aggregate를 사용하는 코드를 모아둔 곳
    - Use Case가 직접적으로 드러나는 곳이다.

- UI Layer과 Domain Layer 간의 다리 역할을 한다.

- 트랜잭션을 관리하고 도메인 계층과의 상호 작용에서 데이터 일관성과 무결성을 보장한다.

### UI Layer
- 구체적인 기술로 사용자와 소통하는 코드가 모인 곳 (Web 등)

- 사용자에게 정보를 표시하고 사용자 상호 작용을 처리하는 역할을 한다.

- UI Layer는 사용자 입력을 캡처하여 추가 처리를 위해 Application Layer 으로 전달한다.

## Layered Architecture를 쓰는 이유
- 도메인 모델을 다른 곳에 뿔뿔히 흩어져 놓는것이 아니라 Domain Layer에 집중 시켜 domain layer만 보면 도메인 모델이 어떻게 쓰이는지 한번에 파악이 가능하다.

- Layered Architecture의 도움 없이는 Domain을 Domain Layer에 격리 시키는 것이 불가능하다.