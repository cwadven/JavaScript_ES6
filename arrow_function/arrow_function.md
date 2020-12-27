## Arrow function

```javascript
setTimeout(function() {
    console.log("settimeout");
}, 1000);


// 화살표 함수
setTimeout(() => {
    console.log("settimeout");
}, 1000);


// 예 1)
// 기본
let newArr = [1,2,3,4,5].map(function(value, index, object){
    return value * 2;
});

console.log(newArr);

// 화살표 함수
let newArr = [1,2,3,4,5].map((v) => {
    return v * 2;
});

console.log(newArr);

// 화살표 함수 (return, 중괄호 생략 가능)
let newArr = [1,2,3,4,5].map((v) => v * 2);

console.log(newArr);

// 화살표 함수 (가독성을 위해서 ()사용 )
let newArr = [1,2,3,4,5].map((v) => (v * 2) );

console.log(newArr);
```