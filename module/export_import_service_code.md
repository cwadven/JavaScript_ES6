## module(export & import) 기반 서비스 코드 구현 방법

### 이용하는 js
```javascript
// import 함수 혹은 변수 from 파일명
// {} 로 묶어서 가져와야 한다!
// 이 의미는 ./myloger에 있는 것 중에서 log라는 객체를 log로 이용하려고 하니깐!!
// destructuring 이랑 똑같다!!
import {MyLogger} from './mylogger';
// export default 일 경우 {} 이용 안해도 된다!
import _ from './utility';

_.log('my first test data');
_.log(`current hour is ${getCurrentHour()}`);

const logger = new MyLogger();
_.log(`lectures of Codesquad are ${logger.getLectures()}`);
```

### 가져오는 js mylogger.js (여러개)
```javascript
// 가져오기 위해서는 export를 해야한다!
export default function log(data){
    console.log(data);
}

export const getCurrentHour = () => {
    return (new.Date).getHours();
}

// Class

export class MyLogger{
    constructor(props){
        this.lectures = ['java', 'iOS'];
    }
    getLectures() {
        return this.lectures;
    }
    getTime() {
        return Date.now();
    }
}
```

### 가져오는 js utility.js
```javascript
const _ = {
    log(data){
        if(window.console) console.log(data);
    }
}

// 가져오기 위해서 먼저 객체를 선언하고 export를 한다!
export default _;
```