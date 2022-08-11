# Java Version. Feature

자바 버전별 차이점.

Java8 ~ Java18

---

## Java1.8

1. Lamda
    1. 익명클래스의 사용을 Lamda 표현식을 사용하여 간결하고 직관적으로 구현할 수 있음
2. stream
    1. 리스트를 비교하거나 확인할때 사용되는 Collection의 반복적인 코드와 멀티코어 활용의 어려움을 해결
3. interface default method
    1. interface에서 default로 정의된 인터페이스를 다른 클래스 내부에서 메소드로 구현하게 할 수 있음
4. Optional
5. new date and time

---

## Java9

1. Java JigSaw 
    1. Maven, Gradle과 비슷한 모듈시스템. 
2. 컬렉션에서 사용할 수 있는 list, set, map 등의 기능 추가
    
    ![Untitled](Java%20Version%20Feature%202a2afc7e9bc249f1961e4c9857c7b79f/Untitled.png)
    
3. 스트림에 takeWhile, dropWhile, iterate등의 기능 추가
4. optional에 ifPresentOrElse 기능 추가
5. Interface에 private제한자 메서드 생성 기능 추가
6. Java 파일을 컴파일 하지 않고도 실행 가능

---

## Java10

1. var 키워드 추가. 
    1. var의 스코프는 해당 메서드 내부를 바라봄
    
    ![Untitled](Java%20Version%20Feature%202a2afc7e9bc249f1961e4c9857c7b79f/Untitled%201.png)
    

---

## Java11_LTS

1. 람다 표현식에 var 키워드 사용 가능
2. String/file에 새로운 키워드 추가

---

## Java12

1. 유니코드 11 지원

---

## Java13

1. 유니코드 12.1 지원
2. 스위치 표현식에서 값을 return가능

![Untitled](Java%20Version%20Feature%202a2afc7e9bc249f1961e4c9857c7b79f/Untitled%202.png)

---

## Java14

1. 스위치 표현의 표준화
    
    ![Untitled](Java%20Version%20Feature%202a2afc7e9bc249f1961e4c9857c7b79f/Untitled%203.png)
    
2. instanceof 패턴 매칭

![Untitled](Java%20Version%20Feature%202a2afc7e9bc249f1961e4c9857c7b79f/Untitled%204.png)

---

## Java15

1. 텍스트 블록 사용 가능 (””” ~~~ “””)
2. 봉인 클래스 사용 가능
    1. 상속 가능한 클래스를 지정할 수 있음.
    2. 상속의 대상은 상위 클래스에 존재하거나 인터페이스 내에 있어야함

![Untitled](Java%20Version%20Feature%202a2afc7e9bc249f1961e4c9857c7b79f/Untitled%205.png)

---

## Java16

1. 유닉스 도메인소캣에 연결 가능
2. 외부 링커 API 기능 제공

---

## Java17_LTS

1. Pattern Matching for Switch
    1. 객체를 전달하여 기능을 전환하고 유형확인이 가능해짐
        
        ![Untitled](Java%20Version%20Feature%202a2afc7e9bc249f1961e4c9857c7b79f/Untitled%206.png)
        
2. Deprecating the Security Manager 제거 예정

---

## Java18

1. UTF-8을 Java Standard API의 기본 Charset으로 지정
2. 간단한 웹서버를 위한 cli툴 제공
3. Reimplement Core Reflection with Method Handle

---