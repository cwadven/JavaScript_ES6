## module(export & import)의 이해

### 이용하는 js
```javascript
// import 함수 혹은 변수 from 파일명
// {} 로 묶어서 가져와야 한다!
// 이 의미는 ./myloger에 있는 것 중에서 log라는 객체를 log로 이용하려고 하니깐!!
// destructuring 이랑 똑같다!!
import {log} from './mylogger';
// export default 일 경우 {} 이용 안해도 된다!
import aaa from './mylogger';

const root = document.querySelector('#root');
root.innerHTML = '<p>Hello World ! </p>';
log('my first test data');
aaa('my second test data');
```

### 가져오는 js mylogger.js
```javascript
// 가져오기 위해서는 export를 해야한다!
export function log(data){
    console.log(data);
}

export default function aaa(data){
    console.log(data);
}
```