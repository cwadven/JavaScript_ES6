## for of

JavaScript ES6 반복문 사용 방법

### 1. for(i;i<x;i++) 형태

```javascript
var data = [1, 2, undefined, NaN, null, ""];
// for 문으로 반복
for(var i = 0; i < data.length; i++){
    console.log(i);
}
```

### 2. 객체.forEach(fuction(val, idx, arr){}) 형태

```javascript
// .forEach를 이용하여 반복
// value는 앞에서 부터의 값
// index는 앞에서 부터의 번째
// array는 해당 data의 정보
var data = [1, 2, undefined, NaN, null, ""];
data.forEach(function(value, index, array){
    console.log(value, index, array);
})
```

### 3. for in 형태

```javascript
var data = [1, 2, undefined, NaN, null, ""];
//for in 으로 반복
for(let idx in data){
    console.log(data[idx]);
}

// 단 for in 문제
// 의도하지 않은 상위에 있는 것 까지 가져온다!
Array.prototype.getIndex = function(){};
for(let idx in data){
    console.log(data[idx]);
}
```

### 3. for of 형태

```javascript
var data = [1, 2, undefined, NaN, null, ""];
// for of 로 반복
for(let value of data){
    console.log(value);
}
```

```javascript
// for of는 배열 뿐만 아니라 문자열을 순회도 할 수 있다.
var str = "hello word!!!";
for(let value of str){
    console.log(value);
}
```