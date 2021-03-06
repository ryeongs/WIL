##[JPA] JPA란
- Java Persistence API 는 자바 진영의 ORM(Object-Relational Mapping) 기술 표준이다. 애플리케이션과 JDBC 사이에서 동작한다.
  - ORM은 이름 그대로 객체와 관계형 데이터베이스를 매핑한다는 뜻이다.
  - ORM 프레임워크는 객체와 테이블을 매핑해서 패러다임의 불일치 문제를 개발자 대신 해결해준다.
  - ORM 프레임워크는 단순히 SQL을 개발자 대신에 생성해서 데이터베이스에 전달해주는 것뿐만 아니라 앞서 이야기한 패러다임의 불일치 문제들도 해결해 준다. 따라서 객체 측면에서는 정교한 객체 모델링을 할 수 있고 관계형 데이터베이스는 데이터베이스에 맞도록 모델링하면 된다. 그리고 둘을 어떻게 매핑해야 하는지 매핑 방법만 ORM 프레임워크에 알려주면 된다. 덕분에 개발자는 데이터 중심인 관계형 데이터베이스를 사용해도 객체지향 애플리케이션 개발에 집중할 수 있다.
- 데이터베이스 기술이라기보다 애플리케이션의 데이터를 객체지향 관점으로 바라보고 다룰 수 있게 해주는 객체지향 기술이다.
- 객체지향의 근본 원리를 충실히 따르면 생산성과 품질, 유지보수성 모두를 만족시킬 수 있는 효과적인 개발이 가능하다는 것은 이미 스프링 프레임워크가 잘 보여주었다. JPA는 전 세꼐 스프링 개발자들이 가장 많이 사용하는 데이터 처리 기술이다.

### JPA를 사용해야하는 이유
1. 생산성
 -  JPA를 사용하면 다음 코드처럼 자바 컬렉션에 객체를 저장하듯이 JPA에게 저장할 객체를 전달하면 된다. INSET SQL을 작성하고 JDBC API를 사용하는 지루하고 반복적인 일은 JPA가 대신 처리한다.
 > jpa.persist(member); // 저장
 > Member member = jpa.find(memberId); // 조회   
 - 따라서 반복적인 코드와 CRUD용 SQL을 개발자가 직접 작성하지 않아도 된다. 
2. 유지보수
 - SQL에 의존적인 개발에서도 이야기했듯이 SQL을 직접 다루면 엔티티에 필드를 하나만 추가해도 관련된 등록, 수정, 조회 SQL과 결과를 매핑하기 위한 JDBC API 코드를 모두 변경해야 했다.   반면에 JPA응 사용하면 이런 과정을 JPA가 대신 처리해주므로 필드를 추가하거나 삭제해도 수정해야할 코드가 줄어든다.
