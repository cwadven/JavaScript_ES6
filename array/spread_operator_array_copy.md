## spread operator 배열의 복사

spread operator : 펼침 연산자

```javascript
let pre = ["apple", "orange", 100];
let newData = [...pre];
console.log(pre, newData);
```

### 출력 결과

~~~
["apple", "orange", 100]
["apple", "orange", 100]
~~~

말 그래로 리스트를 쭉 펼치는 것이다!

그리고 그것을 새로운 배열을 만들어서 넣는 것이다.

즉, 완전 복사 한 것이다.