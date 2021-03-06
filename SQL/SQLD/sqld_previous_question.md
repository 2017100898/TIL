# SQLD 기출문제
* UNION은 데이터의 중복행을 제거한다.
* 로우의 길이가 너무 길어서 데이터 블록 하나에 데이터가 모두 저장되지 않고 두 개 이상의 블록에 걸쳐 하나의 로우가 저장되어있는 형태 : `로우 체이닝`
* 수정된 데이터 해당 데이터 블록에 저장하지 못 하고 다른 블록의 빈공간 찾아 저장 하는 방식 : `로우 마이그레이션`
* 속성에 대한 데이터 타입, 크기, 제약사항 지정 : `도메인`
* '_' 들어가 있는 문자열 찾는 SQL : `'%@_%' escape '@' `
* 차집합 구하는 집합 연산자 : `except`
* 데이터 무결성을 보장하는 방법 : `어플리케이션 로직으로, trigger, 제약 조건`, `lock 은 아님`
* 등수가 1,2,2,3 으로 나오는 함수 : 	`DENSE_RANK`
* 등수가 1,2,3,4 으로 나오는 함수 : `ROW_NUMBER`
* 1,2,2,4 로 나오는 함수: `RANK`
* ROUND(3.45, 1) : `3.5`
* 테이블에 데이터 입력 : `INSERT`
* 테이블 데이터 수정 : `UPDATE`
* 테이블 데이터 삭제 : `DELETE`
	* 세 개 + SELECT 모두 DML 
* DML 수행 후 원복을 위한 명령어 : `ROLLBACK`
* 반정규화의 이유: `I/O량 많아서 성능 저하될 때, 조인으로 인한 성능저하 예상될 때, 칼럼 계산 해서 읽을 때 성능저하 예상` 
* DB에 저장되는 데이터와 그들간의 관계 표현하는 스키마: `외부 스키마`
* ERD에 표시되는 것: `관계명, 관계차수, 관계선택사항`
* 테이블 반정규화 병합 : `1:1, 1:M, 슈퍼/서브`
* 엔터티 안에 인스턴스가 개별적으로 관계 가지는 것: `패어링`
* 지정된 주식별자의 값은 변경될 수 없다.
* S 병원은 여러 명의 환자가 존재하고 각 환자에 대한 이릅, 주소 등을 관리해야 한다. 가장 적절한 엔터티는 `환자`
* 속성의 특징: `엔터티를 설명하고 인스턴스의 구성요소가 된다`
* 데이터 모델링 특징 : `추상화, 명확화, 단순화`
* 속성의 종류: `기본속성, 설계속성, 파생속성`
	* 설계속성: 모델링 과정에서 발생되는 속성, 유일한 값 부여, 상품 코드, 지점 코드 등
* 모델링 순서: `정규화 정확하게 - DB 용량 산정 - 트랜잭션 유형 파악 - 반정규화 - 이력모델, PK/FK 조정, 슈퍼/서브타입 조정 - 성능관점에서 모델 검증`
* 파티션별 윈도우에서 가장 먼저 나온 값 구하는 WINDOW FUNC : `FIRST_VALUE`
* 트랜잭션: `COMMIT이 완료되면 영구적으로 저장 보장해야 한다`
* 데이터 모델링이 최종적으로 완료된 상태라 정의할 수 있는, 물리적 스키마 설계 전 단계 : `논리적 모델링`
* SQL 실행 순서 : `FROM - WHERE - GROUP BY - HAVING - SELECT - ORDER BY`
* 옵티마이저 종류 : `성능기반, 비용기반`
* Nested Loops Join : `OLTP 많이 사용, 랜덤 액세스,...`
