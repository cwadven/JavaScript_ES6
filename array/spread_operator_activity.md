## spread operator 활용

spread operator : 펼침 연산자

### 중간에 다른 배열의 값을 집어 넣기.

```javascript
let pre = [100, 200, "hello", null];
let newData = [0, 1, 2, 3, ...pre, 4]
console.log(newData)
```

### 출력 결과

~~~
[0, 1, 2, 3,100, 200, "hello", null, 4]
~~~

말 그래로 배열를 쭉 펼치는 것이다!

그리고 그것을 새로운 배열을 만들어서 넣는 것이다.

즉, 객체가 같지 않으며 새로운 것을 만들어 완전 복사 한 것이다.

---

### 개별 파라미터로 값 전달 쉽다.

```javascript
function sum(a,b,c){
    return a+b+c;
}

let pre = [100, 200, 300];

// 두번째 값은 배열로 받음
// 펼쳐지면서 sum에 들어간다.
console.log(sum.apply(null, pre));

//spread operator를 사용할 경우
console.log(sum(...pre));
```

### 출력 결과

~~~
600
600
~~~