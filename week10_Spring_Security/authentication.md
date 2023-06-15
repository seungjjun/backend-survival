# 학습 키워드

## Identifier
- Username을 ID로 표현하는걸 주의해야 한다. (국제적으로나 기술적으로나 Username이라는 표현을 널리 쓰고 있다.)

## PostgreSQL (MySQL, MariaDB와 두드러지는 차별점)

## OAuth 2.0
- OAuth 2.0은 사용자가 비밀번호를 제공하지 않아도 데이터에 대한 접근 권한을 다른 애플리케이션이나 웹사이트에 부여할 수 있는 방법을 제공한다. 

## Bearer Token 옵션
- 전달자 토큰이라고도 하는 Bearer Token은 권한을 부여하는 서버에서 클라이언트로 발급하는 액세스 토큰이다. 

- Bearer Token은 서버의 자원에 접근하는 데 필요한 권한을 클라이언트에 제공한다.

- Token은 탈취당할 수도 있기 때문에 https 같은 안전한 방식으로 서버-클라이언트간 교환해야 한다.

## SecurityFilterChain
- SecurityFilterChain을 이용해 컨트롤러로 들어오기 전 단계를 모두 관리할 수 있다. (인증 관련 부분)

- HTTP 요청에 대해 여러 Filter를 먼저 실행할 수 있도록 한다.

## `@Configuration`
- 현재 클래스가 Spring의 설정 파일임을 알려주는 어노테이션이다.

- 이 어노테이션을 단 클래스는 빈 설정을 담당하는 클래스가 된다.

- 이 클래스 안에서 @Bean 어노테이션이 동봉된 메소드를 선언하면, 그 메소드를 통해 스프링 빈을 정의하고 빈의 생명주기는 Spring IoC 컨테이너에서 관리한다.

## `@EnableWebSecurity`
- @EnableWebSecurity 어노테이션을 단 클래스는 Spring Security에 작동에 영향을 미치는 구성 클래스가 된다.

- 해당 클래스에서 security관련 설정을 변경할 수 있다. 예를 들어 custom된 사용자 인증이나 권한을 부여하는 규칙을 변경 등등 여러 보안 구성 방식을 변경할 수 있다.

## Filter vs OncePerRequestFilter
- Filter는 필터링 작업을 수행하거나 요청 및 응답 데이터를 수정하기 위한 기능을 제공하는 인터페이스로 3가지 메서드를 구현해야하지만 OncePerRequestFilter는 Spring 전용 클래스로 doFilterInternal() 메서드 하나만 구현해도 된다.

- OncePerRequestFilter는 필터가 요청당 한 번만 적용되도록 하는 doFilterInternal 메서드를 제공해준다.

- OncePerRequestFilter는 구성된 필터 수와 순서에 관계없이 요청당 한 번만 발생해야 하는 작업을 처리하는 경우에 특히 유용하다.

## FilterChain
- FilterChain은 여러개의 Filter가 하나의 체인처럼 연결되어 형성되는것을 말한다. 

- FilterChain으로 연결된 filter들은 요청을 처리하는 순서가 있다. 
    - 예를 들어, 

## SecurityContext
- SecurityContext는 애플리케이션의 security context에 대한 접근을 제공하는 인터페이스이다. 

- 주로 현재 인증된 사용자의 세부 정보를 저장하는데 사용된다.

- SecurityContextHolder에 보안 관련 정보를 저장한다.

- security를 사용할 때, 스레드간 정보 유출을 방지하기 위해 요청이 완료되면 SecurityContext가 지워지는 것을 확인해야 하는데 SecurityContextPersistenceFilter가 자동으로 지워준다.