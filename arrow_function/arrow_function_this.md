## Arrow function this context 내용

```javascript
const myObj = {
    runTimeout() {
        setTimeout(function() {
            // 이것을 사용하려고 하면 bind를 해야한다
            // 인자로 쓰는 function을 이용하여 그 안에 this를 사용하면 window를 가르킨다!!!
            // 그래서 myObj를 가르키기 위해서는 bind를 해야 된다!
            this.printData();
        }.bind(this), 200);
    },

    printData(){
        console.log("hi codesqud!");
    }
}

myObj.runTimeout();

//arrow 함수일 경우 bind를 해줄 필요가 없다
const myObj = {
    runTimeout() {
        setTimeout(() => {
            // 이것을 사용하려고 하면 bind를 해야한다
            this.printData();
        }, 200);
    },

    printData(){
        console.log("hi codesqud!");
    }
}
```

> **예2)**

```javascript
const el = document.querySelector("P");

const myObj = {
    register() {
        el.addEventListener("click", function(evt){
            this.printData(evt.target);
        }.bind(this));
    },

    printData(el) {
        console.log('clicked!!', el.innerText);
    }
}


// arrow 사용할 경우
const myObj = {
    register() {
        el.addEventListener("click", (evt) => {
            this.printData(evt.target);
        });
    },

    printData(el) {
        console.log('clicked!!', el.innerText);
    }
}
```