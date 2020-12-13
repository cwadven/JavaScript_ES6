## closure

몇번째 리스트입니다.

이벤트 등록

> 이벤트 헨들러
.addEventListener 같은 것

```javascript
var  list = document.querySelectorAll("li");

for (var i=0; i<list.length; i++){
	// 클릭한 이벤트 상황
	list[i].addEventListener("click", function(){
		console.log(i + "번째 리스트 입니다.")
	})
}
```

이럴 경우 li를 누를 경우 무조건 마지막 i의 값이 나온다

"i 번째 리스트 입니다." <br>
"i 번째 리스트 입니다." <br>
"i 번째 리스트 입니다." <br>

이런 이유는 `i`가 closure 변수라고 할 수 있다.

var 변수 여서!? i의 마지막 된 값을 공유 한다.

이 문제를 해결하는 방법으로는 `var`를 `let`으로 만들면 된다.

```javascript
var  list = document.querySelectorAll("li");

for (let i=0; i<list.length; i++){
	// 클릭한 이벤트 상황
	list[i].addEventListener("click", function(){
		console.log(i + "번째 리스트 입니다.")
	})
}
```

이럴 경우 li를 누를 경우 각각의 숫자가 나온다.

"0 번째 리스트 입니다."<br>
"1 번째 리스트 입니다."<br>
"2 번째 리스트 입니다."<br>
....