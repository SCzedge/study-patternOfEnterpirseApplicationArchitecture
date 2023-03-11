# 객체 - 관계형 동작 패턴
## 작업단위
- 비즈니스 트랜잭션 중 데이터베이스에 영향을 미치는 변경내용을 추적하고 작업 완료시 데이터베이스에 기록.

### 작동원리
- 작업단위는 객체의 변경내용을 데이터베이스에 기록하기위해 추적하는 객체이다.
- 커밋시점에 해야 할일을 작업단위가 직접 결정한다.
- 데이터베이스 업데이트 메소드를 직접 실행하지 않고 작업단위가 트랜잭션을 열고 동시성검사 후 변경내용을 기록하므로 직접 작업순서를 조정할 필요가 없다.
- 추적을 위한 객체는 객체 호출자를 사용하거나 직접 할 수 있다.
- 호출자 등록은 객체 호출자가 객체를 작업단위에 등록. 등록하지 않으면 커밋시 등록하지 않음.
- 객체 등록은 등록메소드를 객체 매소드에 넣고 작업단위를 각 객체로 전달하거나 유지해야하며 적절할때 등록메소드를 호출하지 않으면 버그가 발생한다.
- 작업단위 컨트롤러는 작업단위가 모든 읽기를 처리하고 복사본을 만들어 수정시 복사본과 비교해 선택적으로 업데이트한다.









