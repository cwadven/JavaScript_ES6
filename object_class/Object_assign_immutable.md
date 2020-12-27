## ES6 Class

```javascript

const previousObj={
    name : "crong",
    lastTime : "11:20",
};

// 이전 객체를 이용하여 새로운 객체 만들기
// 객체를 이용하여 새로운 객체 반환
// assign은 맨앞에 있는 객체에 뒤에 있는 매개변수 값들을 전부 다 넣는다!
const myHealth = Object.assign({}, previousObj, {
    lastTime : "12:30",
});
```
