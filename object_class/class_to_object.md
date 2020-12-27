## ES6 Class

```javascript
// ES6 전
function Health(name) {
    this.name = name;
}

Health.prototype.showHealth = function() {
    console.log(this.name + "님 안녕하세요");
}

const h = new Health("crong");
h.showHealth();

// ES6!! 결국 function의 프로토타입과 똑같다!!!
class Health {
    // __init__ 같은 것
    constructor(name, lastTime){
        this.name = name;
        this.lastTime = lastTime;
    }

    showHealth(){
        console.log("안녕하세요" + this.name);
    }
}

// 결론 함수의 프로토타입에 저장되는 거랑 마찬가지!!
const myHealth = new Health("crong");
myHealth.showHealth();
```