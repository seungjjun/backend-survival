## 학습 키워드

## DTO (Data Transfer Object) 란
- DTO란 getter와 setter로만 이루어진(어떠한 로직도 포함하고 있지 않은) 데이터 전송을 목적으로 한 객체이다.

### DTO의 목적
- 주요 목적은 **계층간** 데이터를 전송하기 위함이다. 그리고 필요한 데이터만 전송을 함으로써 데이터를 더 효율적으로 전송해 애플리케이션의 성능 향상을 기대할 수 있다.

### 프로세스 간 통신(IPC, Inter-Process Communication)
- IPC는 각각 개별의 프로세스끼리 서로 통신해서 데이터나 정보를 교환할 수 있도록 하는 기술이다.

- 즉, IPC 기술을 이용해 프로세스는 서로 독립적인 공간에 있어도 데이터를 교환할 수 있다.

- IPC 기술
    - Pipes : 파이프는 단방향 통신으로 한 프로세스에서 다른 프로세스로 일방적으로 데이터를 보낼 수 있는 기술이다.
    - Sockets : 소켓은 네트워크를 통해서 통신을 할 수 있도록 하는 기술으로 대표적으로 TCP/IP, UDP 같은 통신 프로토콜을 지원한다.
    - RPC(원격 프로시저 호출) : RPC는 프로세스가 다른 주소 공간에 있는 프로세스의 메서드를 원격으로 호출할 수 있도록 하는 기술이다.  호출 프로세스는 원격 프로세스에 요청을 보낸 다음 요청된 기능을 실행하고 결과를 호출 프로세스에 반환합니다
    - RMI(Java Remote Method Invocation) : RMI는 다른 컴퓨터의 자바 객체의 메서드를 로컬에 있는 메서드 처럼 호출 할 수 있게 하는 기술이다.

## “무기력한 도메인 모델” 이란 그리고 안티 패턴인 이유
- 무기력한 도메인 모델은 도메인 객체가 DTO처럼 데이터만 갖고 있고 비즈니스 로직같은 동작을 하는 행위를 포함하고 있지 않은 도메인 모델을 의미한다. 
    - 데이터와 행위를 분리하는 점에서 DTO와 같지만 정확히 DTO와는 다른 개념이다. 
### 안티 패턴이라고 불리는 이유
- 데이터와 동작 로직을 분리해야 하기 때문에 유지 보수가 힘들고 이는 결국 절차적 스타일의 디자인이기 때문

- 데이터와 프로세스를 함께 결합하는 객체 지향 설계의 기본 개념에 정면으로 위배된다는 점

- 도메인 모델이 데이터와 동작을 모두 갖고 있어야 한다는 DDD의 원칙에 부합하지 않다.

## 자바빈즈(JavaBeans)
- 자바빈즈 클래스는 일반적으로 따라야할 관례가 있는데 이는 DTO처럼 데이터를 전송하기 위한 관례와 비슷한것 같다. (하지만 같은 개념은 아님)
    - 자바빈즈 클래스 생성 시 지켜야할 관례 : getter, setter, 기본 생성자, 직렬화 역직렬화를 위한 Serializable 인터페이스 상속

## EJB(Enterprise JavaBeans)
- EJB란 기업 환경을 구축하기 위한 기업용 서버의 구성요소 아키텍처로, 트랜잭션, 보안, 비즈니스 애플리케이션의 로직을 갖는 서버측 아키텍처이다. 

## Java의 record
- 자바17에서 도입된 기능으로 record를 이용해 클래스를 선언하면, getter, setter, 생성자, equals(), hashCode(), toString() 메서드를 자동으로 생성해준다.
- 어떠한 동작이나 로직이 없고, 단순히 데이터를 저장하고 전송하는 역할로 사용된다. (DTO 같은 객체를 만들 때 사용하자)

### record의 장점
- getter, setter, 생성자같은 메서드를 작성하지 않아 코드의 양이 줄어든다.
- 한번 생성하면 수정할 수 없는 불변성을 보장한다.

## DAO (Data Access Object)
- DAO는 DB의 데이터에 접근하기 위한 객체이다.


## ORM (Object Relational Mapping)
- ORM이란 객체와 관계형 DB의 데이터를 자동으로 매핑해주는 기술이다.

- 객체지향 프로그래밍에서 도메인 모델과 관계형 DB의 테이블 모델간의 관계를 바탕으로 자동으로 SQL문을 생성하여 객체 모델과 DB 테이블을 일치시켜준다.

### ORM이 가져다 주는 이점
- 개발자가 직접 SQL문을 작성하거나 DB의 스키마를 관리하지 않아도 코드로 관리가 가능하다.

- DB연결이나 트랜잭션 처리, SQL 쿼리 작성 등등 반복적으로 해야하는 작업들을 자동으로 할 수 있다. -> 생산성 증가