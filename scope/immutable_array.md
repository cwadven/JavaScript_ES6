## immutable array

불변한 array를 이용하여 새로운 array 만들기

```javascript
const list = ["apple", "orange", "watermelon"];
list2 = [].concat(list, "banana");
console.log(list2);
```

> list -> ["apple", "orange", "watermelon"]
> list2 -> ["apple", "orange", "watermelon", "banana"]

list2 는 let 이다.