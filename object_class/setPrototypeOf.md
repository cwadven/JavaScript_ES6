## Object setPropertypeOf

```javascript
const healthObj = {
    showHealth : function() {
        console.log("오늘은 운동시간 : " + this.healthTime);
    },
    setHealth : function(newTime){
        this.healthTime = newTime;
    }
}


const myHealth = {
    name: "crong",
    lastTime: "11:20",
}

// myHealth라는 곳에 healthObj의 프로토타입을 넣기 (메서드 넣기)
Object.setPropertypeOf(myHealth, healthObj)
```