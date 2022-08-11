# Java Inheritance

자바 상속 관련 지식

---

1. extends는 일반 클래스와 abstract 클래스 상속에 사용되고, implement는 interface 상속에 사용된다.
2. class가 class를 상속받을 땐 extends를 사용하고, interface가 interface를 상속 받을 땐 extends를 사용한다.
3. class가 interface를 사용할 땐 implements를 써야하고
4. interface가 class를 사용할 땐 implements를 쓸수 없다.
5. extends는 클래스 한 개만 상속 받을 수 있다.
6. extends 자신 클래스는 부모 클래스의 기능을 사용한다.
7. implements는 여러개 사용 가능하다.
8. implements는 설계 목적으로 구현 가능하다.
9. implements한 클래스는 implements의 내용을 다 사용해야 한다.

**자바 extends/implements/abstract 차이**

- extends : 부모 클래스의 메소드나 변수를 그대로 사용할 수 있음.
- implements : 부모는 선언만 되어있음. 변수나 메소드 같은 내용은 자식에서 오버라이딩 해줘야함
- abstract : extends하여 사용하되, 몇몇은 추상 메소드화 되어있어 오버라이딩 필요

<aside>
💡 extends는 클래스를 확장하는 거고 implements는 인터페이스를 구현하는 것이다.

인터페이스와 보통 클래스의 차이는 인터페이스는 정의한 메소드를 구현하지 않아도 된다.

인터페이스를 상속받는 클래스에서 인터페이스에 정의된 메소드를 구현하면 된다.

</aside>