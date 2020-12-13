## string

어떤 string이 어떠한 문자로 시작하는지 확인하는 메소드

```javascript
let str = "hello word ! ^^ ~~";
let matchstr = "hello";
console.log(str.startsWith(matchstr));
console.log(str.endsWith(matchstr));
console.log(str.includes(matchstr));
```

**str.startsWith(matchstr)**<br>
시작하는 문자가 matchstr과 같으면 true를 반환.<br>
시작하는 문자가 matchstr과 다르면 false를 반환.<br>

**str.endsWith(matchstr)**<br>
끝나는 문자가 matchstr과 같으면 false를 반환.<br>
끝나는 문자가 matchstr과 다르면 false를 반환.<br>

**str.includes(matchstr)**<br>
str 글자 안에 matchstr이 들어있을 경우 true 반환.<br>
str 글자 안에 matchstr이 들어있지 않을 경우 false 반환.<br>