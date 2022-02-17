## Thymeleaff 타임리프 란
> 템플릿 엔진이며 서버사이드 자바 템플릿 엔진의 한 종류이다. 
> > 템플릿 엔진은 지정된 템플릿 양식과 데이터가 합쳐져 HTML문서를 출력하는 소프트웨어이다. 웹사이트 화면을 어떤 형태로 만들지 도와주는 양식
  
    
### Text 출력
> <div th:text="${text}"></div> 혹은
> <div>[[${text}]]</div> 

### 조건문
####  if , else
> <div th:if="${data != null and data != ''}" th:text="${data}"></div>   
> <div th:unless="${data != null and data != ''}" th:text="데이터 없음"></div>   
> > else == unless 고 unless 를 쓸 경우 if 에서 쓴 조건을 똑같이 명시해줘야 else 역할을 한다. 
#### switch case
> <th:block th:switch="${data.name}"> 
>  <div th:case="A"> A</div>  
>  <div th:case="B"> B</div>  
></th:block>  
  
#### each  반복문
> <th:block th:each="data:${datas}">  
>	  <h1 th:text="${data}"></h1> 
> </th:block> 
- 변수명 앞에 status 변수를 추가해 row에 대한 추가정보를 얻을 수 있다.
> <th:block th:each="data,status:${datas}">
>	  <h1 th:text="|${status.count} ${data}|"></h1>
> </th:block>    
> > status 속성
> > - index : 0부터 시작
count : 1부터 시작
size : 총 개수
current : 현재 index의 변수
event/odd : 짝수/홀수 여부
first/last : 처음/마지막 여부
