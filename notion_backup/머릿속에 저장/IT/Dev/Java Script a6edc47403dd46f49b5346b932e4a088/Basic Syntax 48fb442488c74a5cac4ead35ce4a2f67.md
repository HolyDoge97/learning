# Basic Syntax

---

- **객체지향 프로그래밍. (JS)**
- 코드의 중복을 줄여 휴먼 에러를 방지함.
- 코드의 길이가 줄어들어 가독성이 높아짐
    
    class 햄버거 {
    
    constructor(버거이름) {
    
    this.이름 = 버거이름;
    
    this.패티 = 2;
    
    this.빵 = 2;
    
    }
    
    }
    

햄버거라는 클래스를 생성함. 이 클래스에는 버거 이름을 객체(변수)로 지정받고, 지정받은 이름에다 패티와 빵의 내용을 덧붙혀줌

const 일반버거 = new 햄버거("일반버거");

- **상속 (JS)**

상속은 기존의 클래스를 재활용하여 코드의 간소화를 도와줌.

class 햄버거 {

constructor(버거이름) {

this.이름 = 버거이름;

this.패티 = 2;

this.빵 = 2;

}

}

위와 같은 클래스가 있을때, 상속을 이용하여 유사한 클래스를 만드려면

class 빵식 extend 햄버거 {

constructor(버거이름) {

this.맛 = 짬밥맛;

}

}

이런식으로 생성할 수 있음.

const 군대리아 = new 빵식("군대리아");

군대리아는

name = 군대리아

패티 = 2

빵 =2

맛 = 짬밥맛

이라는 속성을 가지게 됨.

- **var, let, const의 차이 (JS)**
    
    var는 변수 선언 후 동일한 변수로 다시 선언하여 자유롭게 내용을 수정할 수 있음
    
    또한, 선언부 이전에 var 변수를 호출해도 호출처리는 가능함. 다만 호출시점에 담겨있는 데이터를 가져오게되어, undifined가 뜸
    
    var hello = 'hi!';
    
    console.log(hello); --> hi! 출력
    
    var hello = 'OKOK';
    
    console.log(hello); --> OKOK 출력
    
    let은 변수 선언 후 동일한 변수로 선언 불가능하지만, 내용은 수정할 수 있음
    
    var hello = 'hi!';
    
    console.log(hello); --> hi! 출력
    
    var hello = 'OKOK'; --> 이미 사용 중인 변수 명이라며 에러 뱉음
    
    hello = 'LOL';
    
    console.log(hello); --> LOL 출력
    
    const는 변수 선언 후 동일한 변수로 선언 불가능하고 내용도 수정할 수 없음
    
    var hello = 'hi!';
    
    console.log(hello); --> hi! 출력
    
    var hello = 'OKOK'; --> 이미 사용 중인 변수 명이라며 에러 뱉음
    
    hello = 'LOL'; --> 이미 사용 중인 변수 명이라며 에러 뱉음
    
    console.log(hello); --> hi! 출력