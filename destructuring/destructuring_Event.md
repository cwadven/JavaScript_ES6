## Destructuring Event

#### 가져온 배열에 있는 JSON의 특정 위치 function으로 빼오기

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

function getNewsList([,newslist]) {
    console.log(newslist);
}

getNewsList(news);
```

#### EventListener를 이용하여 Destructuring 하기

**HTML**

```html
<body>
    <div>안녕하세요~!</div>
</body>
```

**Javascript**

```javascript
document.querySelector("div").addEventListener("click", function(evt){
    console.log(evt.target);
});

// Destructuring 객체 이용
document.querySelector("div").addEventListener("click", function({target}){
    console.log(target);
});

// Destructuring 객체 화살표 함수
document.querySelector("div").addEventListener("click", ({target}) => {console.log(target)});
```