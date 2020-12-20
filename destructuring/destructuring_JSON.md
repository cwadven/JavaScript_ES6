## Destructuring JSON파싱

### JSON을 이용해서 간단하게 변수 설정

#### 가져온 배열에 있는 JSON의 특정 위치 빼오기

```javascript
let news = [
    {
        "title" : "sbs",
        "imgurl" : "http://sbs이미지/",
        "newslist" : [
            "sbs뉴스1",
            "sbs뉴스2",
            "sbs뉴스3"
        ]
    },
    {
        "title" : "mbc",
        "imgurl" : "http://mbc이미지/",
        "newslist" : [
            "mbc뉴스1",
            "mbc뉴스2",
            "mbc뉴스3"
        ]
    }
]

let [,mbc] = news;
console.log(mbc);
```

#### JSON 객체의 값을 변수에 할당 하기

```javascript
// 위의 코드 추가
let {title, imgurl} = mbc;
```

#### 특정위치의 배열 값과 그 것을 변수에 한번에 가져오기

```javascript
// 위의 코드
let [,{title, imgurl}] = news;
```