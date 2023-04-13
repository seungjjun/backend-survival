# 학습 키워드
## Java ServerSocket
- ServerSocket : ServerSocket은 클라이언트와 서버가 연결할 수 있도록 엔드포인트를 설정하여 해당 엔드포인트로 연결 요청하는 클라이언트와 네트워크 연결을 도와준다.

- 예를 들어 아래와 같이 port번호 8080을 설정해주면, 8080으로 접속하는 클라이언트의 수신을 대기하고 연결 요청하는 클라이언트와 서버를 연결한다.
```
ServerSocket listener = new ServerSocket(8080);
``` 

## Blocking vs Non-Blocking
- Blocking : blocking은 특정 스레드의 작업이 진행되는 도중에는 다른 스레드를 모두 차단해 작업이 진행중인 스레드가 완료될때까지 정지되는 상태를 말한다. 

- Non-Blocking : Non-Blocking은 Blocking과 다르게 하나의 스레드의 작업이 완료되지 않아도 다른 스레드가 중단되지 않는 것을 말한다.
