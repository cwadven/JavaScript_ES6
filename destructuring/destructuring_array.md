## Destructuring Array

### 배열의 부분만 가져와서 변수에 대입

```javascript
let data = ["crong", "honux", "jk", "jinny"]
let jisu = data[0];
let jung = data[2];

// 문법 python에서 a, _ = (1, 2) 같은 의미이다!
// 대신 javascript에서는 []로 묶는다!
let [jisu,,jung] = data;
```