# 제어문

## 제어문

- **조건문**
    - if문
    
    조건식이 참이면 블록 내의 문장을 처리하고, 거짓이면 블록을 빠져 나감
    
    ```jsx
    if (조건식) {
    // 실행문장;
    }
    ```
    
    - else문
    
    조건식이 참이거나 거짓일때 if문과 함께 사용 ~가 아니라면 else 조건식 실행
    
    ```jsx
    if (조건식) {
    // 실행문장;
    }
    else {
    // 실행문장;
    }
    //else문은 단순히 참과 거짓 두가지의 조건만 존재할때 사용
    //복잡한 조건이 걸려있을땐 else if(조건식)을 통해 자세한 조건식 작성
    ```
    
    - switch문
    
    `if문`과 `삼항 연산자`와 같이 `switch문`은 조건에 따라 다른 동작을 수행시킬 수 있다.
    
    `switch문`은 **어떤 값을 가진 대상을 두고 조건값과 일치하는지를 확인하고 동작을 수행하는 방식**이다.
    
    ```jsx
    <script>
          var session = prompt(
            "관심 세션을 선택해 주세요. 1-마케팅, 2-개발, 3-디자인",
            "1"
          );
          switch (session) {
            case "1":
              document.write("마케팅 세션은 201호에서 진행됩니다!");
              break;
            case "2":
              document.write("개발 세션은 203호에서 진행됩니다!");
              break;
            case "3":
              document.write("디자인 세션은 205호에서 진행됩니다!");
              break;
            default:
              alert("잘못 입력하셨습니다(_ _)");
          }
        </script>
    ```
    
- **반복문**
    - for문
        
        **for문**은 while 문과는 달리 자체적으로 초기식 / 표현식 / 증감식을 모두 포함하고 있는 반복문입니다. 따라서 while 문보다는 좀 더 간결하게 반복문을 표현할 수 있습니다.
        
        (변칙적 사용 찾아보기)
        
    
    ```jsx
    for (let i = 0; i < 10; i++){
        console.log(i); // 0~9까지 출력
    }
    //for (초기식; 조건식; 증감식) {
    
    //조건식의 결과가 참인동안 반복적으로 실행하고자 하는 실행문;
    
    //}
    ```
    
    ```jsx
    <script>
          for (x = 2; x < 10; x++) {
            for (y = 1; y < 10; y++) {
              document.write(x + "X" + y + "=" + x * y + "<br>");
            }
          }
        </script>
    
    // for 문을 이용한 구구단 출력
    ```
    
    - while문
        
        **while문**은 조건문이 참일 때 실행되는 반복문이다. 조건은 문장안이 실행되기 전에 참, 거짓을 판단한다.
        
        ```jsx
        var n = 0;
        var x = 0;
        
        while (n < 3) {
          n++;
          x += n;
        }
        /* 
        다음의 while문은 n이 3보다 작을 때까지 반복한다.
        반복을 살펴보면, n을 x에 계속 더하게 된다. 그러므로 x와 n 변수는 다음의 값을 갖는다.
        첫번째 반복; n=1 과 x=1
        두번째 반복; n=2 과 x=3
        세번째 반복; n=3 과 x=6
        세번째 반복후, n<3 이라는 초건은 더 이상 참이아니가 되므로 반복은 종료된다 
        */
        ```
        
    - do-while문
    
    ```jsx
    //do-while문
    var i = 0;
    do {
    document.write("반복 조건이 true이면 반복합니다. <br>");
    i += 1;
    } while (i < 10);
    ```
    
- **보조 제어**
    - break문
    
    ```jsx
    //break문
    for (i = 0; i < 10; i++){
    document.write("*");
    break; //이 지점에 오면 바로 반복문을 종료합니다.
    }
    ```
    
    - continue문
    
    ```jsx
    //continue문
    for (i = 0; i < 10; i++){
    document.write("*");
    continue; // 위의 "*" 부분만 조건식대로 계속 반복
    document.write("continue문 때문에 이 문자은 건너뜁니다.");
    }
    ```
