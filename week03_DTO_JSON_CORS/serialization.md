## 학습 키워드

## 직렬화(Serialization)
- 직렬화는 자바의 객체를 DB에 저장하거나 외부에서 사용할 수 있도록 바이트 스트림으로 변환하는 과정을 말한다. 그리고 이 바이트 스트림을 다시 자바 객체로 변환하는 과정을 역직렬화라고 한다.

- 우리가 자바 언어로 작성된 객체를 웹 페이지 상에서 읽을 수 있는것도 직렬화 과정을 통해서 사람이 읽을 수 있도록 변환이 되기 때문이다.

## 마샬링
- 마샬링은 직렬화와 비슷한 개념이지만 다른 특징으로 다른 언어나 프로그램 간에 데이터를 변환하는 특징이 있다.(RPC 메커니즘 이용)

## JSON (JavaScript Object Notation)
- JSON이란 문자 기반으로 이루어진 key - value 형태로 데이터 교환 형식이다. 
    - 자바 객체(DTO) -> 변환(Jackson 같은것) -> JSON

    - JSON -> 변환(Jackson 같은것) -> 자바 객체(DTO)
- JSON은 사람과 기계 모두 쉽게 읽고 이해할 수 있다는 특징 때문에 언어와 관계 없이 널리 사용되고 있다.

### JSON 구조

```
{
    "company" : "seedwhale",
    "fruits" : [
        {
            "name" : "apple",
            "color" : "red",
        },
    ],
}

```
