## 특정 문자열이 포함된 배열 만들어 반환하기

### 문제

<img src="https://github.com/cwadven/JavaScript_ES6/blob/master/activity/img/question.PNG" alt="drawing" width="600"/>

### 자답 :

#### HTML

```html
<body>
    <ul>
        <li>apple</li>
        <li>orange</li>
        <li>banana</li>
        <li>strawberry</li>
    </ul>
</body>
```

#### JavaScript

```javascript
function print() {
    let list = document.querySelectorAll("li");
    // Node를 배열로 만들겠다.
    let newArray = Array.from(list);
    // 만든 배열에서 filter라는 메소드를 이용해, 특정 조건을 만족하는 값을 가져온다.
    // 매개변수 안에는 함수가 들어가기는 하는데, return 조건이 참인 경우를 출력한다.
    // 해당 함수의 매개변수 의미는 배열 안에 있는 각요소를 해당 매개변수로 쓴다는 것이다.
    newArray = newArray.filter(word => word.innerText.includes("e"));
    console.log(newArray);
}
print();
```