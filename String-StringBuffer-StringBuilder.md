

## String, StringBuffer, StringBuilder 
### String 
- 문자열을 대표하는 것으로 문자열을 조작하는 경우 유용하게 사용 가능
- new 연산자를 통해 생성되면 인스턴스 메모리 공간이 절대 변하지 않으므로 '+',concat과 같은 연산시 메모리의 내용이 변하는것이 아니라 새로운 String 인스턴스가 생성된다.
  - 이렇게 새로운 문자열이 만들어지면 기본의 문자열은 가비지 콜렉터에 의해 제거되야 한다.
- 문자열 연산이 많아지는 경우 성능이 떨어진다.
  - 불변하기 때문에 조회가 빠르고 멀티스레드 환경에서 동기화를 신경 쓸 필요 없다.
### StringBuffer 와 StringBuilder
- String과 다르게 클래스는 한 번만 만들고 메모리의 값을 변경시켜서 동기화를 신경 쓸 필요 없다. (기존의 버퍼 크기를 늘리며 유연하게 동작)
  - 그러므로 문자열 연산이 자주 있을 때 사용하면 좋다.
- StringBuffer 와 StringBuilder 차이점 
  - StringBuffer는 각 메서드별로 Synchronized Keyword가 존재하여, 멀티스레드 환경에서도 동기화를 지원
     반면, StringBuilder는 동기화를 보정하지 않음.

###결론
1. String은 짧은 문자열을 더할 경우 사용
2. StringBuffer는 스레드에 안전한 프로그램이 필요할 떄나, 개발 중인 시스템의 부분이 스레드에 안전한지 모를 경우 사용하면 좋다.
3. StringBuilder는 스레드에 안전한지 여부가 전혀 관계 없는 프로그램을 개발할 때 사용하면 좋다.
4. 단순 성능만 놓고 본다면 연산이 많은 경우, StringBuilder > StringBuffer >> String 이다.

출처 : https://12bme.tistory.com/42
