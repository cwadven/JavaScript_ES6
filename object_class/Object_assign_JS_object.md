## Object assign 메서드

```javascript
const healthObj = {
    showHealth : function() {
        console.log("오늘은 운동시간 : " + this.healthTime);
    }
}

// 프로토를 만들어주는 것 뿐
const myHealth = Object.create(healthObj);

// 일일이 넣어줘야 한다...
myHealth.healthTime = "11:20";
myHealth.name = "crong";

console.log(myHealth);


// 한번에 넣는 방법 방법 2
const myHealth = Object.assign(Object.create(healthObj), {
    name : "crong",
    lastTime : "11:20",
});
```