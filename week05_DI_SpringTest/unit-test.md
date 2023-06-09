# 학습 키워드

## V 모델
- V모델은 소프트웨어 개발의 생명주기를 설명하는 모델 중 하나로 뒤로 돌아갈 수 없는 폭포수 모델의 확장된 형태이다.

- 폭포수 모델은 뒤로 돌아갈 수 없다는 단점이 있지만 각 단게를 나눠 다루는것은 유용하다.

- 각 단계에 대한 테스트를 작성하여, 처음부터 어떻게 테스트를 할지 생각한다.

1. 요구사항 분석 → 사용자 중심 ⇒ 인수 테스트
2. 시스템 설계 → 시스템 사양 결정 ⇒ 시스템 테스트
3. 아키텍처 설계 → 고수준 설계 ⇒ 통합 테스트
4. 모듈 설계 → 저수준 설계 ⇒ 단위 테스트
5. 구현 → 코딩

## Test Matrix
- 품질을 2가지 관점으로 바라볼 수 있다. (외적 품질, 내적 품질)

- 일반적으로 말하는 품질은 외적 품질을 의미한다. 

- 눈에 보이지 않는 내적 품질은 당장 큰 성과가 업기 때문에 놓치는 경우가 많다.

## 내적 품질(테스트 코드 작성등)을 높이면 좋은 이유
- 내적 품질이 우수하면 외적 품질을 끌어올리거나 대응하기 좋다.

- 내적 품질이 좋으면 문제가 생겼을때 바로 원인을 파악하고 쉽게 수정할 수 있다.

- 즉, 애플리케이션의 유지보수나 확장성에 있어 좋다.

## JUnit
- JUnit은 Java 애플리케이션용 자동화된 테스트를 지원하는 프레임워크이다.
- 단위 테스트만 지원하는것이 아닌 통합 테스트, E2E테스트를 작성하는데도 사용이 된다.

## 단위 테스트
- 단위 테스트는 애플리케이션 시스템의 개별 구성 요소 또는 단위를 확인하는 데 중점을 둔 테스트이다.

- 예를 들어 함수, 메서드, 클래스 또는 모듈이 단위 테스트의 대상이 될 수 있다. 
- 단위 테스트의 목적은 각 코드 단위가 예상대로 작동하고 독립적으로 올바르게 작동하는지 확인하는 것입니다.

### 단위 테스트의 장점
- 각 단위를 독립적으로 테스트함으로써 개발자는 개발 초기에 문제를 파악하고 수정할 수 있다는 장점이 있다.

## E2E 테스트
- E2E(End-to-End) 테스트는 실제로 사용하는 사용자 시나리오를 작성하여 애플리케이션을 평가하는 테스트이다. 

- E2E 테스트는 애플리케이션을 사용하는 사용자 관점에서 작성된다.

- 예를 들어 작성된 시나리오를 바탕으로 데이터 입력, 사용자 인터페이스와의 상호 작용, 결과 확인을 예상하고 테스트한다.

- E2E 테스트는 일반적으로 프로덕션 환경과 유사한 환경에서 자동화하여 실행한다.