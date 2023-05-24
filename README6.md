# 함수

## 함수

 **함수**
    - **함수 선언**(**function declaration**)은 지정된 매개변수(parameter)를 갖는 함수를 정의합니다.
        
        ```jsx
        function calcRectArea(width, height) {
          return width * height;
        }
        //function name([param[, param,[..., param]]]) { [statements] }
        //name
        //함수 이름.
        
        //param - 매개변수
        //함수로 전달되는 인수(argument)의 이름. 인수의 최대 개수는 엔진마다 다름.
        
        //statements
        //함수의 몸통(body)을 구성하는 문(statement).
        ```
        
- **지역변수**
    - 함수내에서 사용가능
    - 지역 변수를 선언하려면 예약어 var와 함께 변수 이름을 지정
    
    ```jsx
    var myVar = 100;
    test();
    document.write("myVar is " + myVar);
    
    function test() { 			
    	var myVar = 50;
    }
    //출력값은 100
    ```
    
- **전역변수**
    - 스크립트소스 전체에서 자유롭게 사용가능
    - 함수안에서새롭게전역변수를선언하려면변수이름앞var예약어사용하지않으면됨
    
    ```jsx
    var myVar = 100;
    test();
    document.write("myVar is " + myVar);
    
    function test() { 			
    	myVar = 50;
    }
    //출력값은 50
    ```
    
- ***let / const***
- **예약어**
    
    
- **호이스팅**
- **매개변수**
    
    데이터를 받아오는 역할
    
- **인수**
    
    
- **익명함수**
    
    이름이 없는 함수, 익명 함수를 선언할 때는 이름을 붙이지 않습니다.
    
    ```jsx
    var add = function (a, b){
        return a + b;
    }
    var sum = add(10, 20);
    //sum
    //30
    ```
    
- **즉시실행함수**
    
    ```jsx
    var result = (function (){
        return 10+20;
    }());
    
    console.log(result);
    -----------------
    //매개변수
    var result = (function(a,b){
        return a+b;
    } (10,20));
    
    console.log(result);
    ```
    
- **화살표함수**
