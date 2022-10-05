#6장 - 클래스 설계

- item36: 상속보다는 컴포지션을 사용하라.
  - 컴포지션은 더 안전하고, 유연하고 명시적이다.
    - (컴포지션이란? 다른객체의 인스턴스를 자신의 인스턴스 변수로 포함해서 메서드를 호출하는 기법이다)
  - 상속을 사용할때?
    - 명확한 is-a 관계일때
    - 슈퍼클래스를 상속받은 모든 서브클래스는 슈퍼클래스로도 동작할 수 있어야한다.
      - 슈퍼클래스의 단위테스트는 서브클래스로도 통과할 수 있어야 한다는 의미(LSP)
  - 오버라이딩 제한
    - 어떤 이유로 상속은 허용하지만, 메서드는 오버라이드하지 못하게 만들고 싶은 경우에는 open 키워드를 사용하자
    - 서브클래스에서 오버라이드할 수 있는 메서드를 제한하고 싶으면 final 키워드를 사용하자.
  - 컴포지션은 다른 클래스의 내부 구현에 의존하지 않기 때문에 더 안전합니다.
  - 컴포지션은 여러 클래스를 대상으로 할 수 있기 때문에 더 유연합니다.
  - 컴포지션은 this 리시버를 사용할 수 없기 때문에 리시버를 명시적으로 활용해야 해야 더 명시적입니다.
---

