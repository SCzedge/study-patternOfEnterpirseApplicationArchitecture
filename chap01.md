# chap01

## 계층화
- 계층화는 소프트웨어 시스템을 분할하는 데 사용하는 가장 일반적인 기법
- 상위 계층은 하위 계층이 정의하는 서비스를 사용하나 하위계층은 상위계층을 인식할 수 없음
- 모든 계층형이 불투명한 구조는아니나 대부분 불투명함.

### 장점
1. 단일 계층을 하나의 일관된 계층으로 이해할 수 있음
    - 이더넷작동 방법을 몰라도 TCP기반 FTP서비스 구축가능
2. 대안 구현으로 계층을 대체 할 수있음.
    - FTP는 다른 프로토콜 기반에서 변경없이 작동할 수 있음.
3. 계층간 의존성 최소화
4. 표준화 용이
5. 다른 여러 상위서비스에서 사용가능.

### 단점
1. 전체가 효과적으로 캡슐화 되지않음.
2. 계층을 추가하면 성능이 저하됨



## 엔터프라이즈 애플리케이션에서 계층의 발전
웹과 함께 3계층 방식이 보편화됨.
## 세가지 주요 계층
- 상황에 맞는 적절한 분리방법의 선택이 필요함.
- 도메인과 데이터원본은 프레젠테이션에 의존하지 않아야함

1. 프레젠테이션
    - 사용자와 소프트웨어 간 상호작용 처리
    - 서비스제공, 정보표시(html등), 사용자요청, http요청, 명령줄 호출, 일괄 작업API처리
2. 도메인
    - 시스템 핵심 논리
    - 입력, 저장데이터 기반 계산
    - 유효성검사
    - 데이터 원본 결정
3. 데이터 원본
    - 데이터베이스, 메시징시스템, 트랜잭션관리자
    - 다른패키지와의 통신
    - 지속성 데이터를 저장
    
## 계층이 실행될 위치 선택
1. 서버에서 모두 실행
가장 간단하며 업그레이드 및 수정이 용이
2. 클라이언트에서 모두 실행
응답성 및 비연결작업에서 유리

## 계층별 선택 위치
1. 데이터 원본
    - 거의 모든경우 서버에서실행
2. 프레젠테이션
    - 사용자 인터페이스 유형에 따라 달라짐.
    - 순수한 html만 클라이언트로 전달할 수록 문제가 간단해짐
3. 도메인
    - 서버에서 실행하는것이 유지관리에 유리
    - 클라이언트 실행시 응답성 및 비연결작업에 유리






























