# 학습 키워드

## Multipart FormData
- Multipart FormData는 HTTP POST 요청 시 파일 및 텍스트 필드와 같은 여러 유형의 데이터를 보내는 방법이다.

- 이미지, 문서 또는 파일을 첨부할 때 처럼 파일 업로드가 포함된 양식을 제출해야 할 때 일반적으로 사용된다.

- HTTP 요청 시 Content-Type header가 multipart/form-data로 설정되어 요청이 간다.

## `@ModelAttribute`
- @ModelAttribute 어노테이션은 HTTP 요청시 URL의 쿼리 변수나 body에 담겨오는 데이터를 바인딩 하기 위해 사용하는 어노테이션이다.

- GET 요청의 경우 
    - "/user?userId=1111" 이와 같은 URL에 GET 요청을 할 때, @ModelAttribute 어노테이션을 이용해 userId의 값(1111)을 @ModelAttribute에서 선언해준 변수에 바인딩 시켜줄 수 있다. 아래 예시에서 userId 변수에 "1111"값을 set할 수 있다.
        ```
        @RequestMapping("/user")
        public String getUser(@ModelAttribute("userId") String userId) {
            return userId;
        }
        ```
- POST 요청의 경우
    - POST 요청 시 @ModelAttribute의 value에서 선언해준 값을 body에 담겨오는 데이터와 일치하는 것을 찾아 바인딩 한다.

## @RequestMapping consumes
- consumes속성은 컨트롤러 메서드가 처리할 수 있는 미디어 타입을 지정하는 데 사용된다.

- 만일 요청이 consumes속성으로 지정해준 타입이 아닌 경우 에러를 반환한다.
