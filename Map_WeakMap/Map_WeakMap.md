## Map & WeakMap 추가정보를 담은 객체저장하기

> Set 특징 중복없이 유일한 값을 저장하려고 할 때!

Array -> Set, Weakset
Object -> Map, Weakmap

Map은 key/value 구조

```javascript
let wm = new WeakMap();

let myfun = function(){};
// 이 함수가 얼마나 실행 됐는지? 를 알려고 할 때

// Set 자료구조가 아니라 WeakMap에 있는 set 메서드이다.
// key/value로 만들기
wm.set(myfun, 0);

console.log(wm);

let count = 0;
for (let i=0; i<10; i++>){
    count = wm.get(myfun); // get value
    count++;
    wm.set(myfun, count);
}

console.log(wm);
```