# async / await

***async / await*** 를 통해 복잡한 `Promise Hell` 코드를 간결하게 작성할 수 있게 되었습니다. 함수 앞에 `async` 키워드를 사용하고 `async` 함수 내에서만 `await` 키워드를 사용하면 됩니다. 이렇게 작성된 코드는 `await` 키워드가 작성된 코드가 동작하고 나서야 다음 순서의 코드가 동작하게 됩니다.

```jsx
// 함수 선언식
async function funcDeclarations() {
	await 작성하고자 하는 코드
	...
}

// 함수 표현식
const funcExpression = async function () {
	await 작성하고자 하는 코드
	...
}

// 화살표 함수
const ArrowFunc = async () => {
	await 작성하고자 하는 코드
	...
}
```

- 사용 예시

```jsx
const printString = (string) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve();
      console.log(string);
    }, Math.floor(Math.random() * 100) + 1);
  });
};

const printAll = async () => {
  await printString('A');
  await printString('B');
  await printString('C');
};

printAll();

//출력값 
//A
//B
//C
```
