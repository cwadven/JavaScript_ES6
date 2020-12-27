## rest_parameters

```javascript
// 예상할 수 없는 매개변수의 개수를 모를 경우 사용
function checkNum() {
    // arguments를 array로 바꾸기
    const argArray = Array.prototype.slice.call(arguments);
    console.log(argArray);
    const result = argArray.every((v) => typeof v === "number")
    console.log(result);
}

const result = checkNum(10,2,3,4,5,"55");
const result = checkNum(10,2,"55");


// 스프레드를 이용해서 arguments 이용 안하고 바로!
function checkNum(...argArray) {
    // arguments를 array로 바꾸기
    const result = argArray.every((v) => typeof v === "number")
    console.log(result);
}

const result = checkNum(10,2,3,4,5,"55");
const result = checkNum(10,2,"55");
```