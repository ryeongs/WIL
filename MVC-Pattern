### Spring MVC패턴
- 소프트웨어 디자인 패턴 중 하나로 Model(모델), View(뷰), Controller(컨트롤러)와 같이 3가지의 구성요소로 나누어 비즈니스 처리 로직과 사용자 인터페이스를 구분하며 개발하기 위해 사용된다
#### Model
- 데이터를 관리하고 비즈니스 로직을 처리하는 구간이다.
Model은 사용자의 요청이 들어오면 단순히 그에 맞는 로직 처리만 수행한다.

#### View
- 사용자 인터페이스 구간이다. 
#### Controller
- Model과 View의 연결을 위한 구간이다.

#### 처리 순서
1. 사용자의 Request를 Controller가 받는다.
2. Controller는 Business Logic을 처리를 Service와 같이 처리한 후 결과를 Model에 담는다.
3. Model에 저장된 결과를 바탕으로 시각처리를 담당하는 View를 제어하여 사용자에게 전달한다.
