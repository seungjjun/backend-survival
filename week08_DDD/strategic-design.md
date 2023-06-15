# 학습 키워드

## 전략적 설계 (Strategic Design)
- DDD는 크게 전략적 설계와 전술적 설계로 나뉘어 진다. 

- 도구 모음이나 패턴에 따라 전략적 설계 패턴, 전술적 설계 패턴 나뉘어 진다.

- 전략적 설계는 전술적 설계의 선행 조건이다.

전략적 설계는 다음과 같은 패턴을 다룬다.
1. Ubiquitous Language
2. Bounded Context
3. Subdomain

## 보편언어 (Ubiqutious Language)
- Ubiqutious Language는 DDD의 시작이자 끝이다. (DDD의 핵심)

- 모두(도메인 전문가, 비즈니스 분석가, 소프트웨어 설계자, 프로그래머)가 같은 하나의 언어를 사용한다.

- 비즈니스 도메인을 적절하게 다루면서도 코드를 작성할 때도 사용할 수 있는 용어를 만들어 사용해야 한다.

- 설계하기 어렵거나 코딩하기 어려운 어휘는 재검토할 필요가 있다.

## 제한된 컨텍스트 (Bounded Context)
- 커다란 시스템에서는 하나의 언어가 하나의 뜻으로만 사용되지 않는다.
    - 예를 들어, Account라는 어휘는 맥락에 따라 사용자의 계정이란 의미와 은행의 통장이란 의미로 사용할 수 있다.
    - 결국 대화할 때 맥락을 파악하는 비용이 증가한다.

- 맥락을 좁혀 하나의 어휘가 하나의 대상을 지시하는 상황을 만들 수 있다. 

- 하나의 시스템에서 **맥락이 통일되는 경계(Bounded Context)** 로 나눠서 보편 언어를 잘 만들고 유지해야 한다.

### 목적
- 소프트웨어를 조직화 하는 방법

- 소프트웨어를 만들기 위해 모델링 하고, 그때 보편언어를 사용하기 위해 하나의 어휘가 하나의 것만 뜻하기 위해 Bounded Context를 사용한다.

## 하위 도메인 (Subdomain)
- 도메인을 나눌 때, Subdomain이라는 단위를 사용한다.

- 예를 들어, 회사에서 부서 단위로 나누듯이 도메인을 Subdomain으로 나눈다.

- Subdomain은 이미 정해져 있기 때문에 개발하면서 맞춰가야 할 가능성이 크다.

- Subdomain은 문제 공간(problem space)이다. (문제를 다루는 것)

- Subdomain은 시스템쪽이 아닌 좀 더 현실적인 측면에 있다. (문제는 현실에 있기 떄문에)

### 목적
- 현실을 조직화 하는 방법

- 하위 도메인을 나눠 집중을 어느것에 해야 더 큰 비즈니스 가치를 얻을 수 있을지 고민할 수 있음