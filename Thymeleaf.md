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
#### foreach
