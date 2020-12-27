## WeakMap 클래스 인스턴스 변수 보호하기

WeakMap 활용

```javascript
// 함수를 이용해서 클래스???
function Area(height, width) {
    this.height = height;
    this.width = width;
}

Area.prototype.getArea = function(){
    return this.height * this.width;
}

let myarea = new Area(10, 20);

console.log(myarea.getArea());
console.log(myarea.height);

// WeakMap을 이용하여 height에 접근하지 못하도록?
// private하게 만들고 싶을 경우
const wm = new WeakMap();

function Area(height, width) {
    wm.set(this, {height, width});
}

Area.prototype.getArea = function(){
    const {height, width} = wm.get(this);
    return height * width;
}

let myarea = new Area(10, 20);

console.log(myarea.getArea());
// 안됨!!
console.log(myarea.height);
```