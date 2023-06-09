# 객체

## 객체

- **객체*(Object)***
    
    객체란 이름(*name*)과 값(*value*)으로 구성된 프로퍼티(*property*)의 정렬되지 않은 집합이다.
    
    프로퍼티의 값으로 함수가 올 수도 있는데, 이러한 프로퍼티를 메소드(*method*)라고 한다.
    
    객체란 세상에 존재하는 모든 것을 의미한다.
    
    ```jsx
    var toyRobot = {
        productId: "123-12",
        name: "Robot",
        price: "25,000",
        madeIn: "Korea",
        quantity: 10,
        showStock: function() {
            document.querySelector("#display").innerHTML = "이 제품의 가격은 " + this.price + "원 이며 원산지는 "
             + this.madeIn + "이고, 이름은" + this.name + "입니다."
        }
    };
    //실행해야 할때는 함수선언
    ```
    
    **객체 선언 한번 더 찾아보고 공부하기**
    
- **객체의 종류**
    - 내장 객체
        
        자바스크립트 프로그래밍을 할 때 자주 사용하는 요소는 미리 객체로 정의되어 있음
        
    - 문서 객체 모델
        
        객체를 사용해 웹 문서를 관리하는 방식
        웹 문서 안에 포함된 이미지, 링크, 텍스트 필드 등도 모두 각 별도의 객체로 미리 존재함
        
    - 브라우저 객체 모델
        
        **BOM(브라우저 객체 모델)이란** 브라우저 창에 포함된 모든 객체 요소들을 의미한다. 브라우저에는 URL 주소에 대한 정보를 제공하는 'location' 객체, 현재 실행 둥인 브라우저에 대한 정보(브라우저명, 코드명 등)를 제공하는 'navigator' 객체, 브라우저의 방문 기록에 대한 정보를 제공하는 'history' 객체 등이 있다.
        
    - 사용자 정의 객체
        
        자바스크립트에는 수많은 내장 객체가 존재하지만 필요하다면 사용자가 직접 객체를 만들 필요가 있다. 이렇게 **사용자가 직접 만든 객체**를 '사용자 정의 객체'라고 한다.
        
- **속성*(Property)***
    
    객체에서 값을 담고 있는 정보
    
    - 객체의 속성 값을 가져올 때는 객체 이름 뒤에 마침표(.)를 찍고 그 뒤에 속성명을 적음
    - 내장 객체에도 만들어져 있음
- **생성자 함수**
    
    객체를 만들어 내는 함수
    
    - function 예약어 사용
    
    ```jsx
    function Book(author, pages, price, title){
        this.author = author;
        this.pages = pages;
        this.price = price;
        this.title = title;
    }
    jsBook = new Book("고정훈", "355", "24900", "아이스 아메리카노")
    // 생성자 함수의 객체 추가
    // jsBook.author
    // '고정훈'
    // 뼈대만 만들어주면 new 함수로 선언해서 객체를 계속해서 만들 수 있다.
    ```
    
- **사용자 정의 객체**
    
    ```jsx
    var book = {
        title : "자바스크립트",
        author : "홍길동",
        pages : 500,
        price : 15000,
        info : function(){
            alert(this.title + "책의 분량은" + this.pages + "쪽입니다.");
        }
    };
    // 사용자함수 객체 만들기
    ```
    
- **리터럴(*Literal)***
    
    중괄호 `{...}`를 이용해 객체를 선언하는 것을 ***객체 리터럴(object literal)*** 이라고 부릅니다. 객체를 선언할 땐 주로 이 방법을 사용한다. 자료를 표기하는 방식으로도 부른다. 프로그래밍 언어 전체에서 사용하는 언어
    
    ```jsx
    let user = new Object(); // '객체 생성자' 문법
    let user = {};  // '객체 리터럴' 문법
    ```
    
- ***for..in* 반복문**
    
    `for..in` 반복문을 사용하면 객체의 모든 키를 순회할 수 있습니다. 
    
- **객체 변수**
    
    객체 속성 접근 방법
    
    - 객체명.속성명 / 객체명[’속성명’]
        
          car.name    /  car[’name’]
        
- ***Proto-Type* / *Instant***
    - **프로토타입**
        
        자바스크립트의 모든 객체는 프로토타입(*prototype*)이라는 객체를 가지고 있습니다. 모든 객체는 그들의 프로토타입으로부터 프로퍼티와 메소드를 상속받습니다. 이처럼 자바스크립트의 모든 객체는 최소한 하나 이상의 다른 객체로부터 상속을 받으며, 이때 상속되는 정보를 제공하는 객체를 프로토타입(*prototype*)이라고 합니다.
        
    - **인스턴스**
        
        상속(*inheritance*)이란 새로운 클래스에서 기존 클래스의 모든 프로퍼티와 메소드를 사용할 수 있는 것을 의미합니다. 상속을 통해 새로운 프로그램의 요구에 맞게 기존 클래스를 수정하여 재사용할 수 있습니다. 또한, 클래스 간의 종속 관계를 형성함으로써 객체의 관계를 조직화할 수 있는 장점이 있습니다. 따라서 이러한 상속은 추상화, 캡슐화와 더불어 객체 지향 프로그래밍을 구성하는 중요한 특징 중 하나가 됩니다. 자바스크립트에서는 현재 존재하고 있는 객체를 프로토타입으로 사용하여, 해당 객체를 복제하여 재사용하는 것을 상속이라고 합니다.
        
    
    ```jsx
    function Sword(color, metal) {
      this.color = color;
      this.metal = metal;
      this.is = function() {
        console.log(`This is ${this.color} ${this.metal} sword!`);
      };
    }
    const redSteel = new Sword('red', 'steel');
    
    console.log(redSteel); //Sword {color: 'red', metal: 'steel', is: ƒ}
    
    redSteel.is(); //This is red steel sword!
    ```
    
    객체지향언어에서 흔히 사용되는 클래스(*Class*)가 자바스크립트에서는 프로토타입(*prototype*)이며 생성자 함수가 사용된다. 다시 말해 클래스나 프로토타입을 사용하여 만들어 낸 것이 결과물이 인스턴스라고 할 수 있다. 이렇게 생성된 인스턴스는 원래의 객체인 클래스나 프로토타입이 가지고 있는 프로퍼티(*property*)와 메소드(*method*)를 모두 상속(*inheritance*)받는다!
    
- **날짜/시간 정보를 가져오는 함수**
    - 외워야 할 것만 외우기(나머지는 알아서 정리)
    
    ![Untitled](%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%20ea24e2be18e8452bbe978afcda28533a/Untitled.png)
    
- **날짜/시간 정보를 설정하는 함수**
    - 외워야 할 것만 외우기(나머지는 알아서 정리)
    
    ![Untitled](%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%20ea24e2be18e8452bbe978afcda28533a/Untitled%201.png)
    
- **Math 함수**
    
    
    | Math.min(x,y,z....) | 가장 작은 값 반환 |  |
    | --- | --- | --- |
    | Math.max(x,y,z....) | 가장 큰 값 반환 |  |
    | Math.random() | 0보다 크거나 같고 1보다 작은 무작위 숫자 반환 |  |
    | Math.round(x) | 소수점 첫 번째 자리에서 반올림 후 반환 |  |
    | Math.floor(x) | 인수와 같거나 작은 수 중에서 가장 큰 정수 반환 |  |
    | Math.ceil(x) | 인수와 같거나 큰 수 중에서 가장 작은 정수 반환 |  |
    | Math.abs(x) | x의 절댓값 반환 |  |
    
    | Math.sqrt(x) | x의 제곱근 반환 |
    | --- | --- |
    | Math.cbrt(x) | x의 세제곱근 반환 |
    | Math.exp(x) | e의 x제곱근 값을 반환 |
    | Math.log(x) | x의 자연로그 값을 반환.(ln x) |
    | Math.log2(x) | x의 2를 밑으로 가지는 로그 값을 반환 |
    | Math.pow(x,y) | x의 y제곱을 반환 |
    | Math.sign(x) | x의 부호 값을 반환 |
