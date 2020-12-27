## Tagged Template literals

> **함수를 이용한 template literal 사용**

```javascript
const data = [
    {
        name: 'coffee-bean',
        order : true,
        items : ['americano', 'milk', 'green-tea']
    },
    {
        name: 'starbucks',
        order : false,
    }
]

function fn(tags, name, items){
    console.log(tags); // ${변수} 이게 split하는 기준
    if (typeof items === "undefined"){ // name이랑 items는 내가 설정한 ${변수}를 순서대로 가르킨다.
        items = "주문 가능한 상품이 없습니다";
    }
    return (tags[0] + name + tags[1], + items + [tags][2]);
}

// 앞에 fn을 붙이면 해당 함수를 통해서 가져오는데,
const template = fn`<div>welcome ${data[1].name}!!</div><h2>주문가능항목</h2><div>${data[1].items}</div`

console.log(template);
```