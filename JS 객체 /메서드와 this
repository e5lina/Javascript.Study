# this

메서드는 객체에 저장된 정보에 접근할 수 있어야 제 역할을 할 수 있습니다. 대부분의 메서드가 객체 프로퍼티의 값을 활용합니다.

**메서드 내부에서 `this` 키워드를 사용하면 객체에 접근할 수 있습니다.**

이때 '점 앞’의 `this`는 객체를 나타냅니다. 정확히는 메서드를 호출할 때 사용된 객체를 나타냅니다.

```jsx
let player = {
  name: "Hoon",
  age: 28,

  userInformation() {
    // 'this'는 '현재 객체'를 나타냅니다.
    alert(this.player);
  }

};

player.userInformation(); // Hoon
```

`user.userInformation()` 이 실행되는 동안에 `this`는 `user`를 나타냅니다.

- 요약하자면
- 객체 프로퍼티에 저장된 함수를 `메서드’ 라고 부릅니다.
- `player.userInformation()`은 객체를 '행동’할 수 있게 해줍니다.
- 메서드는 `this`로 객체를 참조합니다.
