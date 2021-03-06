## Index
- 인덱스란
> 추가적인 쓰기 작업과 저장 공간을 활용하여 데이터베이스 테이블의 검색 속도를 향상시키기 위한 자료구조이다.
> > 데이터를 조회하는 SELECT 외에도 UPDATE, DELETE의 성능이 같이 향상된다. 만약 Index 를 사용하지 않고 컬럼을 조회하면 전체를 비교하여 탐색해서 처리 속도가 떨어지는 Full Scan을 수행하기 때문이다. 
- 장점 
1. 테이블을 조회하는 속도와 그에 따른 성능을 향상시킬 수 있다. 
2. 전반적인 시스템의 부하를 줄일 수 있다.
- 단점
1. 인덱스를 관리하기 위해 DB의 약 10%에 해당하는 저장공간이 필요하다.
2. 인덱스를 관리하기 위해 추가 작업이 필요하다.
3. 인덱스를 잘못 사용할 경우 오히려 성능이 저하되는 역효과가 발생할 수 있다.
### 관리
> DBMS는 index를 항상 최신의 정렬된 상태로 유지해야 원하는 값을 빠르게 탐색할 수 있다. 그렇기 때문에 인덱스가 적용된 컬럼에 INSERT, UPDATE, DELETE가 수행된다면 각각 다음과 같은 연산을 추가적으로 해주어야 하며 그에 따른 오버헤드가 발생한다.

- INSERT: 새로운 데이터에 대한 인덱스를 추가함
- DELETE: 삭제하는 데이터의 인덱스를 사용하지 않는다는 작업을 진행함
- UPDATE: 기존의 인덱스를 사용하지 않음 처리하고, 갱신된 데이터에 대해 인덱스를 추가함

### 사용하면 좋은 경우
- 규모가 작지 않은 테이블
- INSERT, UPDATE, DELETE가 자주 발생하지 않는 컬럼
- JOIN이나 WHERE 또는 ORDER BY에 자주 사용되는 컬럼
- 데이터의 중복도가 낮은 컬럼
> 인덱스를 사용하는 것 만큼이나 생성된 인덱스를 관리해주는 것도 중요하다. 그렇기 때문에 사용하지 않는 인덱스는 바로 제거를 해주어야 한다. 
