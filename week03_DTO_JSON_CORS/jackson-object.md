# 학습 키워드

## Jackson ObjectMapper
- Jackson ObjectMapper을 이용해서 직렬화, 역직렬화를 할 수 있다. 
    - DTO -> JSON(직렬화), JSON -> DTO(역직렬화)

- DTO 객체를 JSON으로 직렬화를 해주려면 DTO 클래스는 기본 생성자와 getter가 존재해야 자동으로 변환이 된다.
    - getter 메서드의 형식은 반드시 getXXX 형태로 생성이 되어야 한다.
        - get으로 시작하지 않으면 Spring의 기본 MessageConverter인(ObjectMapper를 이용해 자바 객체를 JSON으로 변경해주는 역할) MappingJackson2HttpMessageConverter가 get으로 시작하는 메서드를 찾는데 없으면 인식하지 못한다.

## ObjectMapper
- ObjectMapper는 직렬화, 역직렬화 하기 위해 Jackson 라이브러리에서 제공해주는 클래스이다.

- writeValue() 메서드에 파라미터로 Object를 넘겨주면 자동으로 String으로 변환(직렬화)이 된다.

- 위와 비슷하게 readValue() 메서드가 있는데 클라리언트로 부터 요청 받은 메시지를 객체(DTO 형태)로 변환(역직렬화)이 된다.

- Spring을 이용하면 (기본 Converter인 MappingJackson2HttpMessageConverter를 이용) ObjectMapper 클래스를 이용해 직렬화, 역직렬화 해주는 메서드(writeValue, readValue)필요없이 자동으로 직렬화, 역직렬화를 해준다.

## @JsonProperty
- @JsonProperty 어노테이션은 자바 객체(DTO)를 직렬화할때 이름을 명시해주는 역할을 한다.  
    - DTO클래스의 필드에서 선언해준 이름과 직렬화된 JSON에서 이름을 다르게 사용하고 싶을 때 사용하면 된다.

- 아래 예시처럼 필드에는 이름을 content로 했지만 @JsonProperty("body")를 명시해줬기 때문에 JSON으로 직렬화 했을 떄는 content가 아닌 body로 명시된다.

```
public class Post {
    @JsonProperty("body")
    private String content;
}
```
