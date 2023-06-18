# 학습 키워드

## JWT
- JWT (JSON Web Tokens)는 인증에 필요한 정보를 암호화시킨 토큰을 뜻한다.

- JSON 포맷을 이용해 사용자에 대한 속성을 저장하는 Claim 기반의 웹 토큰

### JWT의 구조
  - xxx[header].yyy[payload].zzz[signature]
  - header
    - 토큰의 타입과 해시 암호화 알고리즘으로 구성된다.
    - alg는 헤더를 암호화 하는 것이 아닌, Signature를 해싱하기 위한 알고리즘을 지정하는 것이다.
        ```
        {
          "alg": "HS256",
          "typ": "JWT"
        }
        ```
    - alg : 알고리즘 방식을 지정하며, 서명(Signature) 및 토큰 검증에 사용한다.
    - typ : 토큰의 타입을 지정한다.
  - payload
    - 토큰에 사용자가 담고자 하는 정보를 담는 곳이다.
    - Payload에는 토큰에서 사용할 정보의 조각들인 Claim 이 담겨있고, 이는 JSON(Key/Value) 형태의 한 쌍으로 이루어져 있다.
  - signature
    - 토큰을 인코딩하거나 유효성 검증을 할 때 사용하는 고유한 암호화 코드이다.

## Claims-based identity
- 클레임 기반 ID는 응용 프로그램이 조직 내부, 다른 조직 및 인터넷에서 사용자에 대해 필요한 ID 정보를 획득하는 일반적인 방법이다.

- 또한, 인증 및 권한 부여와 같은 추가 보안 기능이 포함되어 있다.

- 일반적인 예로 JWT(JSON Web Token)가 있다.

## 대칭키 암호화 / 공개키 암호화
- 암호화란?
    - 평문을 암호문으로 변환하는 과정
- 복호화란?
    - 암호문을 평문으로 변환하는 과정

### 대칭키 암호화 방식
- 암·복호화에 동일한 키를 사용하는 방식으로 키를 비공개 한다.
- 어떤 정보가 대칭키를 통해 암호화 되었다면, 똑같은 키를 갖고 있는 사용자가 아니면 해당 정보를 확인 할 수 없다.

### 공개키 암호화
- 어떤 정보를 특정한 사용자에게 보낼 때 해당 사용자의 공개키를 통해 정보를 암호화 하여 전송한다.

## `@Secured`
- @Secured 어노테이션을 이용해 인증된 사용자의 역할에 따라 특정 메서드를 호출할 수 있는지 여부를 결정할 수 있다.

- 예를 들어, 아래 예시 코드의 admin() 메서드는 역할이 ROLE_ADMIN인 사용자만 접근할 수 있다.
```
@GetMapping("/admin")
@Secured("ROLE_ADMIN")
public String admin() {
    return "Hello, world!";
}
```
- @Secured 어노테이션이 작동하려면 @EnableGlobalMethodSecurity(securedEnabled = true)를 configuration에서 작성해야 한다.
