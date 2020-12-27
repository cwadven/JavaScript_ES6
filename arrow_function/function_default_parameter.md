## Arrow function default parmeter

```javascript
function sum(value, size = {value:1}){
    return value * size.value;
}

// 매개변수 size를 넣지 않아도 자동으로 기존에 설정한 값을 대신 한다는 의미이다.
console.log(sum(3));
```