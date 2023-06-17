# 학습 키워드

## CSRF(Cross Site Request Forgery)
- Cross Site Request Forgery(사이트 간 요청 위조)는 웹 보안 취약점의 일종이며, 사용자가 자신의 의지와는 무관하게 공격자가 의도한 행위(데이터 수정, 삭제, 등록 등)을 특정 웹사이트에 요청하게 하는 공격이다.

### CSRF의 동작 원리
1. 공격자는 게시판에 관리자가 관심을 가질 수 있는 제목으로 CSRF 스크립트가 포함된 게시물을 등록한다.
2. 관리자는 확인이 필요한 게시물로 파악하여, CSRF 스크립트가 포함된 게시물을 확인한다.
3. 게시물을 읽은 관리자는 CSRF 스크립트가 포함된 것을 알지 못한 채 게시물을 확인한다. 하지만, 관리자의 권 한으로 공격자가 원하는 CSRF 스크립트 요청이 발생한다.
4. 공격자가 원하는 CSRF 스크립트 결과가 발생하여, 관리자 및 사용자의 피해가 발생한다.

## 자바 Date vs LocalDateTime
- Java8부터 LocalDate와 LocalDateTime이 도입되었다.

- Date 객체는 변경가능하다는 문제가 있었는데 LocalDateTime 객체는 불변성이라는 특징이 있다.

- Date는 epoch 이후 밀리초 단위로 나타내는 반면 LocalDateTime은 나노초 단위로 나타낸다.

- 일반적으로 여러방면에서 LocalDateTime을 사용하는것이 좋다.

## Epoch Time
- Epoch Time은 시간을 총 초 단위로 추적하는 방법이다. 시작 시간은 1970년 1월 1일 ("Unix epoch" - 00:00:00 Coordinated Universal Time(UTC) 이후 경과된 초 수) Unix epoch에서 시작한다.

- 타임스탬프는 Unix epoch 이후 경과된 초 수를 측정한 것이다.

- Unix 계열 운영 체제 및 파일 형식에서 널리 사용되고 표준 일관된 방식으로 날짜와 시간을 처리해야 하는 컴퓨팅 및 프로그래밍에 유용하다.

## Spring Security PasswordEncoder
- PasswordEncoder는 비밀번호 encoding을 하기 위해 Spring Security에서 제공하는 인터페이스다.

- 애플리케이션의 db에 저장된 user의 password를 보호하는 데 사용되는 보안 수단으로 사용된다.

- DB가 노출되더라도 암호를 인코딩하면 user의 암호를 볼 수 없다.

## Argon2
- Argon2는 비밀번호를 해싱하는 알고리즘 중 하나이다.

- Spring Security는 'Argon2PasswordEncoder'를 기본적으로 제공하지 않아 Bouncy Castle 라이브러리를 이용해 Argon2 알고리즘을 사용할 수 있다.
