# 학습 키워드
## Spring
- Spring은 Java로 애플리케이션을 구축하기 위해 사용되는 프레임워크이다.

- Spring의 주요 기능을 통해 개발자가 더 쉽게 확장 가능하고 유지 보수하기 쉬운 애플리케이션을 구축할 수 있다.

- Spring의 주요 기능
    - DI(Dependency Injection) : Spring의 주요 기능 중 하나인 의존성 주입은 클래스 간 의존관계를 관리하고 있는 Bean 중에서 필요한 것을 컨테이너가 자동으로 주입해 주는 것을 말한다. 즉, 어떤 객체가 사용하는 의존 객체를 직접 만들어서 사용하는 게 아니라, 주입받아서 사용하는 방법을 말한다.
    - Spring MVC : Model-View-Controller(MVC) 아키텍처 패턴을 사용하여 웹 애플리케이션을 구축하기 위한 프레임워크
    
## Spring Boot
- Spring Boot는 개발자가 보다 쉽고 빠르게 애플리케이션을 제작할 수 있도록 기본적으로 세팅이 되어진 환경을 제공해주기 때문에 개발자가 개발환경 세팅에 대한 부담을 줄여주고 개발에 더 집중할 수 있도록 도와주는 프레임워크이다.

- 요약하면 Spring Boot는 Spring 기반 애플리케이션을 보다 쉽고 빠르게 개발할 수 있도록 환경을 제공해준다.

- Spring Boot는 Spring과는 다른 개념이다.

## Spring initializer
- Spring initializer는 Spring Boot 프로젝트를 쉽게 생성할 수 있도록 도와준다.

- 자바 버전, 빌드 시스템(Gradle, Maven) 프로젝트에 필요한 Dependency도 미리 추가할 수 있다.

## Web Server와 Web Application Server(WAS)
- Web Serveer : 웹 서버는 네트워크를 통해 클라이언트에게 주로 정적인 콘텐츠(HTML, 이미지 등등)를 제공한다. 즉, 웹 서버는 클라이언트로 부터의 요청을 처리하여 해당 요청에 맞는 응답을 한다. 

- Web Application Server(WAS) : WAS는 동적인 콘텐츠(실시간 채팅, 알림 등등)을 제공하기 때문에 동적인 웹 애플리케이션을 만들때 필요한 복잡한 로직을 처리하는 기능을 제공한다. 

### Tomcat
- Tomcat은 Java 기반 웹 서버 중 하나로, 동적인 웹을 만들기 위한 웹 서버 또는 서블릿(servlet) 컨테이너이다. 

    - servlet이란 HTTP 요청을 처리하고 동적인 웹 페이지를 생성하는데 사용되는 Java 기반의 웹 애플리케이션 기술이다.

- Tomcat은 자바 서블릿과 자바 서버 페이지(JSP) 컨테이너를 제공하여 HTTP 요청에 대한 응답으로 자바 코드를 실행할 수 있도록 해준다.

- 동적인 처리를 담당하는 서버를 WAS라고 하며 웹서버와 웹 컨테이너의 결합으로 다양한 기능을 컨테이너에 구현한다.

## Model-View-Controller(MVC) 아키텍처 패턴
- MVC 모델은 웹 개발시 일반적으로 사용되는 아키텍처 패턴으로 모델, 뷰, 컨트롤러의 세 가지 구성으로 분리하는 방식이다.

- Model : 애플리케이션의 데이터와 비즈니스로직을 나타내는 부분이다.

- View : 애플리케이션의 사용자가 보는 부분(인터페이스)을 나타낸다. 즉 데이터가 사용자에게 어떻게 표시되어지는지에 대한 방식과 상호 작용(버튼 같은)하는 방법을 나타낸다.

- Controller : 사용자의 요청을 수신하여 Model과 상호작용하고, 적절한 데이터를 View단을 통해 표현한다. 즉, 사용자의 요청을 수신하여 전달하는 역할을 담당한다.

- 애플리케이션을 MVC 패턴같이 세 가지 구성요소로 분리함으로써 유지 관리나 확장성, 테스트하기 쉬운 코드를 작성할 수 있다.

- 또 하나의 장점으로 어느 한 부분이 변경되어도 다른 부분에 영향을 미치지 않아 리팩터링이나 관리하기가 쉽다.

## 관심사의 분리(Seperation of Concern)
- 관심사의 분리는 MVC 패턴처럼 프로그램을 구성할 때, 계층을 분리하여 각 계층의 관심사에 맞는 코드만 모아 다른 계층에 영향을 주지 않도록 하는 설계 원칙이다.

- 관심사의 분리를 함으로써 어느 한 부분의 코드를 변경해도 다른 부분에는 영향을 미치지 않기때문에 개발자는 확장 가능한 애플리케이션을 만들 수 있고, 유지 보수가 용이해진다는 장점이 있다.

## Spring MVC
- Spring MVC는 MVC 아키텍처 패턴을 사용하여 웹 애플리케이션을 구축하기 위한 프레임워크이다.

- Model, View, Controller를 통해 클라이언트의 다양한 HTTP 요청을 처리하고 응답하기 위해 도와준다.

- 주요 기능으로 Request Mapping, Interceptors 등이 있다.
    - Request Mapping : 클라이언트로부터 들어오는 요청에 대해 적절한 컨트롤러에 매핑할 수 있도록 하는 기능이다.
    - Interceptors : 요청과 응답을 interceptor해 인증같은 추가적인 작업을 할 수 있도록 하는 기능이다.

## Java Annotation
- Annotation은 추가적인 정보를 제공하기 위해 추가할 수 있는 메타데이터의 일종이다.

- 어노테이션은 "@" 뒤에 어노테이션 이름으로 표시한다.

- 예를들어 특정 클래스를 컨트롤러로 표시하기 위해 @Controller 어노테이션을 추가하여 해당 클래스가 컨트롤러로 사용되도록 자동으로 설정을 해준다.

- 어노테이션은 개발자가 직접 정의할 수도 있고, 라이브러리나 프레임워크에서도 제공해준다.

## Spring Annotation
- Spring Annotation은 Spring 프레임워크에서 제공하는 어노테이션을 의미한다.

### @RestController
- @RestController는 @Controller와 @ResponseBody를 조합한 어노테이션으로 RESTful한 웹 애플리케이션을 만들기 위해 사용되는 어노테이션이다.


### @Controller
- @Controller 어노테이션이 명시된 클래스를 Spring MVC에서 Controller로 표시하는데 사용한다.

### @ResponseBody
- @ResponseBody는 클라이언트의 요청에 대한 응답값이 JSON 같이 일반 텍스트와 같은 형식으로 변환되어 HTTP body에 담아 응답하는 어노테이션이다.

### @GetMapping
- @GetMapping은 HTTP GET 요청을 특정 컨트롤러 메서드에 매핑하는 데 사용되는 어노테이션이다. 

- @GetMapping에 path를 설정할 수 있는데 해당 path로 들어오는 get요청을 자동으로 @GetMapping 어노테이션이 명시된 메서드에 매핑이 된다.

### @RequestMapping
- @RequestMapping은 @GetMapping과 같이 특정 컨트롤러 메서드에 매핑하는 데 사용되는 어노테이션이다.

- @RequestMapping은 메서드에 명시하는것이 아니라 클래스에 명시함으로써 해당 클래스의 모든 메서드의 요청 경로를 한번에 설정해줄 수 있다.

```
@RestController
@RequestMapping("/hello")
public class WelcomeController {

    @GetMapping
    private String hello() {
        return "Hello";
    }

    @GetMapping("/world")
    private String world() {
        return "Hello, World!";
    }
}
```

- 위 예시 코드를 보면 "/hello"에 대한 get 요청으로 hello() 메서드로 매핑이 되어 응답으로 "Hello"가 응답이 되고, "/hello/world"에 대한 get 요청으로 world() 메서드가 매핑이 되어 "Hello, World!"가 응답이 된다.
