# 학습 키워드

## IOException
-  입출력 작업(파일 읽기/쓰기, 네트워크 통신, 데이터베이스 액세스 등) 중 발생할 수 있는 예외를 나타내느 클래스이다.

## `FileOutputStream`
- FileOutputStream은 바이트 단위로 데이터를 파일에 쓰기 위해 사용하는 클래스이다.

## Mockito  `verify`
- verify메서드는 테스트 시, 테스트하려는 mock객체의 메서드가 호출되었는지 검증하는 메서드이다.

- 아래 verify 테스트는 repository라는 mock객체가 있을때 repository의 save() 메서드가 호출 되었는지 검증하는 테스트이다.

```
verify(repository).save(any());
```

## @SpyBean 과 @MockBean 차이
### @MockBean
- @MockBean은 mock객체를 생성한 뒤 이 bean을 컨테이너에 등록하여 테스트 시에 실제 bean대신 가짜 빈을 사용하도록 한다.

- 실제 bean이 아닌 가짜 bean을 사용하여 가짜 동작(메서드)을 수행하도록 하여 테스트 할 수 있다.

- 특히, 외부 의존성이 높은 객체를 @MockBean을 사용하면 해당 객체가 의존하고 있는 bean을 가짜로 대체하기 때문에 의존성이 높은 객체를 테스트할 때 유용하다.

### @SpyBean
- @SpyBean은 실제 bean의 일부분을 mock객체로 대체하여, 진짜 객체의 메서드를 유지하면서 특정 메서드만 가짜로 구현하도록 할 수 있다.

- 테스트 시, given()을 이용해 @SpyBean으로 설정한 객체의 메서드를 가짜로 구현할 수 있다. 이때 given()으로 호출하지 않은 메서드들은 실제 메서드를 호출한다.

### @MockBean과 @SpyBean의 차이
- @MockBean과 @SpyBean은 모두 테스트 시, mock객체를 만들고 사용한다는 점은 같지만 주요 차이점은 @MockBean은 실제 bean을 대체하는 가짜 bean을 만들어 원하는 동작을 수행하도록 가짜 메서드를 만들고, @SpyBean은 실제 bean을 사용하여 실제 기능을 유지한 채 특정 메서드만 가짜로 구현하는 기능이다.
