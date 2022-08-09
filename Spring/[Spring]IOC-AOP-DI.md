## [Spring] IOC-AOP-DI 란
### IOC(Inversion of Control)
> 프레임워크의 라이프사이클을 관리하고 컨테이너가 빈을 관리해 주기 때문에 '제어의 역전'이라고 한다. 컨트롤의 제어권이 개발자에게 있는게 아니라 프레임워크에 있는 것이다. 
쉽게말해 객체의 생성과 그 객체들의 관리까지 모두 관리한다는 개념인데, 기존에 자바 기반으로 어플리케이션을 개발할 때 자바 객체를 생성하고 서로간의 의존 관계를 연결시키는 작업에 대한 제어권은 보통 개발되는 어플리케이션에 있었는데 IOC 컨테이너는 객체의 생성, 초기화, 서비스 소멸에 관한 모든 권한을 가지면서 객체의 생명주기를 관리한다. 
> 이것을 제어권이 역전되었다해서 IOC라고 부른다.

### AOP(Aspect Oriented Programming)
> 관점지향프로그래밍이라고 부르는데,
우리가 개발을 하다보면 반복되는 작업들이 있다. 이것들의 공통 작업되는 것들을 모아서 필요한 적절한 시기에 적용하는 개념이다.
따로 코드 밖에서 개발을 해두고 프록시개념으로 메서드가 실행되기전, 실행된 직후, 실행시점에 따라 따로 기능을 적용 시키는 것이다.

- 관점지향 프로그래밍. (= 관심사 중심 프로그래핑) 여러 메서드에서 공통적으로 해야하는 일의 코드가 중복된다면, 따로 모아서 재활용하는 것을 말한다. => 공통 코드들을 묶어서 관리한다. (=> 인터페이스를 사용하고 implements로 구현하는 것)
프록시 객체를 생성하는 디자인 패턴.

### DI(Dependency Injection)
> 의존성 주입. 객체 자체가 아니라 Framework에 의해 객체의 의존성이 주입되는 설계 패턴인데 IOC와 연결되는 개념이다.
IOC의 제어권이 프레임워크에게 가게 되는것은 IOC 컨테이너는 DI를 통해 주입시키는데 주입하는 방법은 생성자,메소드의 setter, 멤버변수에 @Inject,@Autowired 를 통해 주입한다.
이러한 방법으로 IOC 컨테이너에 의존성주입을 하는것을 DI라고 부른다.