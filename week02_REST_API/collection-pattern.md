# 학습 키워드
## Collecation Pattern
- 여러 리소스들을 한번에 나타내기 위해 복수명사를 사용하여 URI를 표현하는 패턴

- 단일 자원을 표현할떄는 계층 구조를 이용해 표현
    - 예를 들어 100개의 게시물 중 2번째의 게시물을 표현할 때는 "/posts/2"으로 URI를 구성한다.

## 새로 알게된 사실
- 계층 구조를 표현할떄 너무 복잡한 구조는 오히려 복잡해져 비효율적이다.
    - 이전 프로젝트를 진행할떄 댓글 삭제 같은 간단한 작업을 할 때 /posts/{postId}/comments/{commentId} 이 형태로 어떤 게시글의 댓글을 삭제하려는지 전부 명시하는 방법으로 URI 구성을 했었는데 간단한 작업에 대한 요청은 /comments/{commentId} 같은 형태가 더 좋다고 한다. (굳이 어떤 게시글의 댓글을 명시하는것보다 그냥 심플하게 삭제하려는 댓글의 아이디만 명시하는게 더 좋아보인다)
