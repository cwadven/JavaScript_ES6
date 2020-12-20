## Destructuring Object

### 오브젝트를 이용해서 간단하게 변수 설정

```javascript
let obj = {
    name : "crong",
    address : "Korea",
    age : 10
}

let {name, age} = obj;
// 각각의 변수를 obj에 키값과 동일한 이름을 가진 value를 넣는다.
// let name = obj.name
// let age = obj.age

let {name:name2, age:age2} = obj;
// 만약 내가 동일한 이름을 이용하지 않고 다른 이름을 사용하려고 할 경우
```