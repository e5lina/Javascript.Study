# Promise

프로미스는 자바스크립트 비동기 처리에 사용되는 객체입니다. 여기서 자바스크립트의 비동기 처리란 ‘특정 코드의 실행이 완료될 때까지 기다리지 않고 다음 코드를 먼저 수행하는 자바스크립트의 특성’을 의미합니다.

- **프로미스의 3가지 상태(states)**
- **State**
    
    기본 상태는 `pending`(대기)입니다. 비동기 처리를 수행할 콜백 함수(`executor`)가 성공적으로 작동했다면 `fulfilled`(이행)로 변경이 되고, 에러가 발생했다면 `rejected`(거부)가 됩니다.
    
- 프로미스를 사용할 때 알아야 하는 가장 기본적인 개념이 바로 프로미스의 상태(states)입니다. 여기서 말하는 상태란 프로미스의 처리 과정을 의미합니다. `new Promise()`로 프로미스를 생성하고 종료될 때까지 3가지 상태를 갖습니다.
- ***Pending***(대기) : 비동기 처리 로직이 아직 완료되지 않은 상태
    - `new Promise()` 메서드를 호출하면 대기(Pending) 상태가 됩니다.
    
    ```jsx
    new Promise();
    ```
    
    - `new Promise()` 메서드를 호출할 때 콜백 함수를 선언할 수 있고, 콜백 함수의 인자는 `resolve`, `reject`입니다.
    
    ```jsx
    new Promise(function(resolve, reject) {
      // ...
    });
    ```
    
- ***Fulfilled***(이행) : 비동기 처리가 완료되어 프로미스가 결과 값을 반환해준 상태
    - 여기서 콜백 함수의 인자 `resolve`를 아래와 같이 실행하면 이행(Fulfilled) 상태가 됩니다.
    - 그리고 이행 상태가 되면 아래와 같이 `then()`을 이용하여 처리하면 결과 값을 받을 수 있습니다.
    - ***Fulfilled***(이행) 상태를 다르게 표현하면 ‘완료’라고 말할 수 있습니다
    
    ```jsx
    new Promise(function(resolve, reject) {
      resolve();
    });
    
    function getData() {
      return new Promise(function(resolve, reject) {
        var data = 100;
        resolve(data);
      });
    }
    
    // resolve()의 결과 값 data를 resolvedData로 받음
    getData().then(function(resolvedData) {
      console.log(resolvedData); // 100
    });
    ```
    
- ***Rejected***(실패) : 비동기 처리가 실패하거나 오류가 발생한 상태
    - `new Promise()`로 프로미스 객체를 생성하면 콜백 함수 인자로 `resolve`와 `reject`를 사용할 수 있다고 했습니다. 여기서 `reject`를 아래와 같이 호출하면 실패(Rejected) 상태가 됩니다.
    - 그리고, 실패 상태가 되면 실패한 이유(실패 처리의 결과 값)를 `catch()`로 받을 수 있습니다.
        
        ```jsx
        new Promise(function(resolve, reject) {
          reject();
        });
        
        function getData() {
          return new Promise(function(resolve, reject) {
            reject(new Error("Request is failed"));
          });
        }
        
        // reject()의 결과 값 Error를 err에 받음
        getData().then().catch(function(err) {
          console.log(err); // Error: Request is failed
        });
        ```
        
- **Then**
    - `executor`에 작성했던 코드들이 정상적으로 처리가 되었다면 `resolve` 함수를 호출하고 `.then` 메서드로 접근할 수 있습니다. 또한 `.then` 안에서 리턴한 값이 `Promise`면 `Promise`의 내부 프로퍼티 `result`를 다음 `.then` 의 콜백 함수의 인자로 받아오고, `Promise`가 아니라면 리턴한 값을 `.then` 의 콜백 함수의 인자로 받아올 수 있습니다.
        
        ```jsx
        let promise = new Promise((resolve, reject) => {
        	resolve("성공");
        });
        
        promise.then(value => {
        	console.log(value);
        	// "성공"
        })
        ```
        
- **Catch**
    - 작성했던 코드들이 에러가 발생했을 경우에는 `reject` 함수를 호출하고 `.catch` 메서드로 접근할 수 있습니다.
    
    ```jsx
    let promise = new Promise(function(resolve, reject) {
    	reject(new Error("에러"))
    });
    
    promise.catch(error => {
    	console.log(error);
    	// Error: 에러
    })
    ```
    
- Finally
    - 작성했던 코드들의 정상 처리 여부와 상관없이 `.finally` 메서드로 접근할 수 있습니다.
    
    ```jsx
    let promise = new Promise(function(resolve, reject) {
    	resolve("성공");
    });
    
    promise
    .then(value => {
    	console.log(value);
    	// "성공"
    })
    .catch(error => {
    	console.log(error);
    })
    .finally(() => {
    	console.log("성공이든 실패든 작동!");
    	// "성공이든 실패든 작동!"
    })
    ```
    
- Promise.all
    - Promise.all() 은 여러개의 비동기 작업을 동시에 처리하고 싶을때 사용합니다. 인자로는 배열을 받고, 해당 배열에 있는 모든 Promise 에서 작성했던 코드들이 정상적으로 처리되었을때 결과를 배열에 저장해 새로운 Promise를 반환한다.
    
    ```jsx
    const result = [];
    First()
      .then(value => {
        result.push(value);
        return Second();
      })
      .then(value => {
        result.push(value);
        return Third();
      })
      .then(value => {
        result.push(value);
       console.log(result);  
    	 // ['첫번째', '두번째', '세번째']
      })
    // 이랬던 기존 프로미스를 사용한 비동기 함수 코드를
    
    // promise.all을 사용하여 코드를 깔끔하게 정리할 수 있다.
    Promise.all([First(), Second(), Third()])
      .then((value) => console.log(value))
      // ['첫번째', '두번째', '세번째']
      .catch((err) => console.log(err));
    ```
