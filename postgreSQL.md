### postgreSQL 에러
> 프로젝트에서 posetgreSQL로 만들어 놓은 테이블과 컬럼명을 select 했는데   
> Column 'DATA' does not exist  
> 라는 문구와 에러가 떴다.  
> 이미 있는 테이블, 컬럼명인데 없다는 에러만 떴다.  
> 찾아본 결과 나와 같은 사람들이 있었다.  
>   
> posetgreSQL은 소문자가 기본이라고 한다.     
>   
> 대문자를 "" 으로 묶으면 소문자로 자동 변환되기 때문에 출력이 된다.   
> 그래서 대문자 컬럼명을 
> SELECT "DATA" FROM TEST; 이런 식으로 "" 로 묶어주니 정상 출력된다.  
> 
