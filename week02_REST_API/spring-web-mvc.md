# 학습 키워드
## @RequestMapping
- @RequestMapping은 컨트롤러 클래스의 모든 메서드에 api를 일괄적으로 매핑하는데 사용하는 어노테이션으로 모든 메서드에 공통적으로 매핑하는 URI를 @RequestMapping에 설정해 코드의 중복을 줄일 수 있다.

- [1주차 강의 노트 참고](/week01_HTTP/spring-web-mvc.md)

### @GetMapping
- HTTP GET 요청을 메서드에 매핑함으로 @GetMapping에 설정한 api로 요청이 왔을 때 해당 메서드를 호출하도록 설정하는 어노테이션이다.

- 데이터를 Read할 때 사용하는 어노테이션이다. 

### @PostMapping
- HTTP POST 요청을 특정 메서드에 매핑하는데 사용하는 어노테이션이다.

- 데이터를 Create할 때 사용하는 어노테이션이다.

### @PatchMapping
- HTTP PATCH 요청을 특정 메서드에 매핑하는데 사용하는 어노테이션이다.

- 데이터를 Update할 때 사용하는 어노테이션이다.

### @DeleteMapping
- HTTP DELETE 요청을 특정 메서드에 매핑하는데 사용하는 어노테이션이다.

- 데이터를 Delete할 때 사용하는 어노테이션이다.

### @PathVariable
- PathVariable은 URI 변수를 매개변수에 파라미터로 받아서 사용할 수 있도록 해주는 어노테이션이다.

- 아래 예시 코드에서 URI에서 설정한 변수 {postId}를 @PathVariable에서 설정해준 Long postId 변수에 바인딩해서 사용할 수 있게 해준다.

```
@GetMapping("posts/{postId}")
public String posts(@PathVariable("postId") Long postId) {
       //
}
```

## @RequestBody
- @RequestBody어노테이션도 @PathVariable과 비슷하게 요청 본문에 들어오는 내용을 @RequestBody에 설정해준 변수에 바인딩해주는 어노테이션이다.

## @ExceptionHandler
- @ExceptionHandler는 예외 처리를 도와주는 어노테이션으로 메서드가 처리해야할 예외 처리를 @ExceptionHandler와 함께 설정헤주면 해당 예외가 발생할떄 @ExceptionHandler를 설정해준 메서드가 호출되서 예외를 처리해준다.

- 아래 예시 코드 처럼 @ExceptionHandler에 UserNotFoundException 클래스를 설정했을 때, GET요청으로 user를 못찾았을 때 해당 메서드가 호출 되도록 설정해줄 수 있다.

```
@ExceptionHandler(UserNotFoundException.class)
```

## @ResponseStatus
- @ExceptionHandler를 설정할 때 @ResponseStatus를 설정해서 해당 에러가 어떤 응답 상태를 반환하는지 HTTP 상태 코드를 명시해주도록 도와주는 어노테이션이다.

- @ResponseStatus 어노테이션을 사용함으로써 예외 발생 상황 같은 특정 상황에 대해 HTTP 응답을 보다 더 의미있게 상태 코드를 반환할 수 있다.
