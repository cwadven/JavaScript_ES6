## from 메서드로 진짜 배열 만들기

### 함수에 인자 값을 쓰지 않고, 파라미터 사용 arguments

arguments는 배열이 아니다

```javascript
function addMark(){
    let newData = [];
    for(let i=0; i<arguments.length; i++){
        newData.push(arguments[i] + "!");
    }
    console.log(newData);
}

// 인자를 설정하지 않아도 js는 arguments에서 해당 인자들을 쓸 수 있다.
addMark(1, 2, 3, 4, 5);
```

### 출력 결과

~~~
["1!", "2!", "3!", "4!", "5!"]
~~~

---

### map을 이용한 값 배열 요소를 각각 변환 시키는 것

```javascript
function addMark(){
    let newData = arguments.map(function(value){
        return value + "!";
    })
    console.log(newData);
}

// 인자를 설정하지 않아도 js는 arguments에서 해당 인자들을 쓸 수 있다.
addMark(1, 2, 3, 4, 5);
```

### 출력 결과

~~~
arguments.map is not a function at addMark ...
~~~

arguments는 배열이 아니여서 이런 오류가 뜬다!

map은 자료형이 배열이여야 사용 가능하다!

### 가짜 배열 진짜 배열로 전환

```javascript
function addMark(){
    let newArray = Array.from(arguments);
    let newData = newArray.map(function(value){
        return value + "!";
    })
    console.log(newData);
}

// 인자를 설정하지 않아도 js는 arguments에서 해당 인자들을 쓸 수 있다.
addMark(1, 2, 3, 4, 5);
```

### 출력 결과

~~~
["1!", "2!", "3!", "4!", "5!"]
~~~