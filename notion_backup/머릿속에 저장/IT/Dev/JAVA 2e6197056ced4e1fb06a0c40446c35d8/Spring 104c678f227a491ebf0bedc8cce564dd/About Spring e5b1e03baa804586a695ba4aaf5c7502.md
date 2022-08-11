# About Spring

---

**1. Spring은 Java 기반의 프레임워크다.**

**2. Java 기반이므로 객체지향 프로그래밍을 지원한다.**

**3. 더하여 Spring은 더 고도화된 객체지향(극대화된 다형성) 어플리케이션을 개발할 수 있도록 도와준다.**

- 스프링 프레임워크 : Spring 기술의 핵심
- 스프링 부트 : 스프링의 기술을 편하게 이용할도록 도와줌
- 스프링 데이터 : DB의 CRUD를 편하게 사용할 수 있게 해줌
- 스프링 REST Docs : API문서를 쉽게 만들 수 있도록 해줌
- 스프링 핵심기술 : Spring DI Container, AOP, Event
- AOP란? : 관점 지향 프로그래밍, 어떠한 로직들을 핵심적인 관점으로 나누어서 생각하고, 그 관점을 토대로 공통적인 기능을 묶는 것을 의미
- 스프링 웹 기술 : Spring MVC, Spring WebFlux
- 데이터 접근기술 :Transaction, JDBC, ORM/XML 지원
- 기존에는 Enterprise Java Beans, EJB라는 기술을 사용했음.

자바 bean 클래스를 사용하여 큰 규모의 앱개발을 단순화 하기 위해 발표된 스펙이라고 함.

- > 분산기술은 좋으나, 어렵고 복잡하며 느림
- 이를 개선하기 위해 스프링이 탄생했는데, 스프링은 대규모 자바 개발을 간편화 해주는 오픈소스 경량 프레임워크
- > 평범한 자바 클래스로 EJB 기능을 유지시면서도 코드의 단순화가 가능해졌고, 여러 객체들간의 의존성 해결 및 라이프사이클 관리를 해줌.

**<의존성 주입. (Dependency Injection)>**

- 클래스간의 Hello hi = new Hello(); 와 같이 특정클래스가 다른 클래스를 사용하는 것은 해당 클래스가 Hello 클래스에 의존성을 가진다는 것으로 말할 수 있음.
- > 스프링은 이러한 문제를 해결하기 위해 사용자가 new Hello();처럼 직접 객체를 생성하여 클래스를 호출하는게 아니라, 스프링의 컨테이너로 부터 객체를 전달받음. 이를 **의존성 주입**이라고 칭함.

**<제어의 역전. (Inversion of control)>**

- 기존엔 객체의 생성과 삭제 등을 개발자가 직접 제어해야하는 구조에서, 스프링 컨테이너가 이를 대신 처리해 주는 것을 말함. 원래는 개발자가 해야할 역할을 프레임워크가 처리한다고 하여 **제어의 역전**이라 칭함.

<**Spring - Mybatis 연결>**

1. Maven 의존성 처리

2. root-context.xml 작성 (웹(view)과 관련되지 않은 DAO, Repository, DB등의 설정을 해주는 파일), 파일의 namespace 설정

3. DB 설정이 필요한 파일에 @ContextConfiguration으로 root-context의 경로를 지정해줌

4. mybatis-config.xml은 기본적인 MYBATIS의 설정이 저장되어있는 파일. SQL 쿼리문을 담은 mapper의 경로를 지정해줄 수 있음.

5. 매퍼의 지정은 mybatis-config와 root-context에서 둘다 설정 가능함. 다만 같은 매퍼를 각각의 파일에서 지정하면 충돌이 일어남

- sql연결 요구 *.java> ContextConfiguration으로 root-context 연결 > root-context가 mybatis-config 경로 확인 후 연결 > mybatis-config가 해당하는 mapper 확인

루트 어플리케이션 컨텍스트 파일 = root-context.xml

각종 설정을 위한 *-context.xml 파일들은 bean 형식으로 이루어져 있음