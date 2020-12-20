## 특정 문자열이 포함된 배열 만들어 반환하기

### 정답

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
    let listArray = Array.from(list); //li 노드로 구성된 배열
    let eArray = listArray.filter(function(v){
        // v는 각각 node
        return v.innerText.includes("e");
    });
    return eArray;
}
print();
```