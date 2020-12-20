## 간단한 객체 생성하기

### 단순 {} 를 이용하여 객체를 생성

```javascript
const name = "crong";
const age = 33;

// Key와 Value 그리고 함수도 들어갈 수 있다!!
// 자바스크립트는 클래스 선언 안해도 객체를 만들 수 있다.
// 객체 선언 방법
const obj = {
    name : name;
    age : age;
}

console.log(obj);
```

### 함수를 이용하여 객체를 생성

```javascript
// 함수를 이용해서 객체 생성

// 오버워치 챔피언 정보
// 속성 name, 궁극기 대사, Health Point
// name은 불변 초기 세팅으로만 들어간다.
// 궁극기 대사 불변
// 데미지를 받았을 때 호출되는 함수
// 힐 받았을 때 호출되는 함수
// 궁극기 대사 출력하는 함수

OverWatch = (name, speach) => {
    const _name = name;
    const _speach = speach;

    let Health_Point = 100;

    const damage = () => {
        Health_Point = Health_Point - 10;
        console.log("앍");
        console.log(Health_Point);
    };

    const heal = () => {
        Health_Point = Health_Point + 10;
        console.log("용사는 죽지 않아요~!");
        console.log(Health_Point)
    };

    const ultimate = () => {
        return _speach;
    }

    return {_name, _speach, Health_Point, damage, heal, ultimate}
}

champion = OverWatch("트레이서", "데자뷰 느껴본적 있어?");
console.log(champion);
champion.damage();
champion.damage();
champion.heal();
console.log(champion.ultimate());
```