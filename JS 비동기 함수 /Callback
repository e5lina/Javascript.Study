# Callback

**Callback 함수**는 **다른 코드의 인수로서 넘겨주는 실행 가능한 코드**를 말한다. 콜백을 넘겨받는 코드는 이 콜백을 필요에 따라 즉시 실행할 수도 있고, 아니면 나중에 실행할 수도 있다. 쉽게 말해 **함수를 등록하기만 하고 어떤 이벤트가 발생했거나 특정 시점에 도달했을 때 시스템에서 호출하는 함수!**

- ***Callback*** 함수의 기본 형태

```jsx
function func(callback) {
	callback();
}
function callback() {
	console.log("callback이다");
}

func(callback);
```

- 필요한 이유
    - **Callback** 함수는 가독성이나 코드 재사용 면에서도 사용 된다.
    - 비동기 방식으로 작성된 함수를 동기 처리하기 위해 사용한다.
- ***Callback Hell***
    - 콜백 지옥(callback hell)이란 **콜백 함수를 익명 함수로 전달하는 과정에서 또 다시 콜백 안에 함수 호출이 반복되어 코드의 들여쓰기 순준이 감당하기 힘들 정도로 깊어지는 현상**을 말한다
    
    ```jsx
    step1(function (value1) {
        step2(function (value2) {
            step3(function (value3) {
                step4(function (value4) {
                    step5(function (value5) {
                        step6(function (value6) {
                            // Do something with value6
                        });
                    });
                });
            });
        });
    });
    //step1에서 어떤 처리 이후 그 결과를 받아와, 인자로 전달된 익명 함수의 매개변수로 넘겨준다. 이후 step2에서 또 어떤 처리를 하고, 다음 익명 함수가 실행된다. 이를 반복하다보면 코드가 피라미드 모양으로 기술되게 된다.
    ```
    
- **Callback Hell을 벗어나기 위해 async, await를 사용한다.**
