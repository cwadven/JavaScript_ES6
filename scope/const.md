## const

변하지마!!(변경 금지)! 이지만, const를 사용하더라도 배열과 오브젝트의 값을 변경하느 것은 가능하자!

값을 재할당 하는 것만 안된다!!!!!!!!

재할당

```javascript
const a = 10;
a = 100;
```

### 변경하지마 예

```javascript
function home() {
	const homename = [1,2,3,4];
	homename = ["1","2"];
	console.log(homename);
}
```

### 변경가능 예

```javascript
function home() {
	const homename = ["apple", "orange", "watermelon"];
    home.push("banana");
	console.log(homename);
}
```

위와 같이 변경이 되지 않도록 하려고 할 때 만든다.