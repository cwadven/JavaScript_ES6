## Set으로 유니크한 배열 만들기

> Set 특징 중복없이 유일한 값을 저장하려고 할 때!

```javascript
let mySet = new Set();

// 요소 추가
mySet.add("crong");
mySet.add("hary");
mySet.add("crong");

console.log(if(mySet.has("crong")));

mySet.forEach(function(v){
    console.log(v);
})

// 요소 제거
mySet.delete("crong");

mySet.forEach(function(v){
    console.log(v);
})
```