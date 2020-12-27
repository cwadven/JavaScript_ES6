## WeakSet으로 효과적으로 객체타입저장하기

> 참조를 가지고 있는 객체만 저장이 가능하다.

```javascript
let arr = [1,2,3,4,5];
let arr2 = [5,6,7,8];

// 각 배열 obj 객체로 쉽게 만들기
// 넣을 때 자동으로 arr이라는 키 이름과 arr의 값이 들어간다.
// obj = {arr:[1,2,3,4,5], arr2:[5,6,7,8]}
let obj = {arr, arr2};

let ws = new WeakSet();

// 가능
ws.add(arr);
ws.add(arr2);
ws.add(obj);
ws.add(function(){});

// 불가능
// ws.add(111);
// ws.add("111");
// ws.add(null);

arr1 = null;
arr2 = null;

//arr1과 arr2의 값은 보이지만, 실질적으로는 없다..?
console.log(ws);

console.log(ws.has(arr), ws.has(arr2));
```