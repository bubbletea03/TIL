# Express, Pug 등 예습

- 프론트엔드 스터디까지 시간이 많이 남았으니 백엔드도 공부하고 싶어서,
노마드코더의 줌 만들기 인강을 들어보려고 한다.
- https://nomadcoders.co/noom/lectures/3075
- 선수강 해야하는 인강이 있는데, 이게 무료라 이걸 들음.
- 그래서 Express, app.get(), Pug, (req, res) 이런 거에 대해서
미리 알아야 된다길래
공부하려고 한다.


## REST
- REST = Representational State Transfer
- 자원의 상태를 주고받는 모든 것을 의미.
- HTTP Method(post, get, delete, put)를 통한 CRUD(create, read, update, delete)를 적용하는 것
(일단 그냥 개념이구나 하고 넘어가자.)

## End Point


```
http://localhost:3001/api/login
```

- 어떤 리소스에 접근해야 하는지 알려주는 URL이 End Point이다.
- 끝에 있는 /api/login 이 부분이 엔드 포인트.




## app.get

```js
app.get("/", (req, res) => {
  res.send("<h1>Hello world</h1>");
});

app.listen(3000, () => {
  console.log("listening on *:3000");
});
```

- app.get은 GET 리퀘스트를 정의하는 부분
- 첫 번째 피라미터 => End Point

+ app.listen은 포트 정의 및, 서버 구축 성공 시 callback함수 실행


## 서버사이드 렌더링

```js
app.get('/', (req, res) => {
  res.sendFile(__dirname + '/index.html');
});
```

- sendFile로 index.html을 보내도록 한다.
- 그 다음 index.html을 작성한다.
- 그러면 서버사이드 렌더링이다.

에게? 말로만 듣던 서버사이드 렌더링이 겨우 이거라고?



## What is Pug

html을 편하게 작성하게 해준다.
```js
doctype html
html(lang='en')
  head
    title Pug
    script(type='text/javascript').
      foo = true;
      bar = function () {};
      if (foo) {
      bar(1 + 5)
      }
  body
    h1 Pug - node template engine
    #container.col
      p You are amazing
      p
        | Pug is a terse and simple
        | templating language with a
        | strong focus on performance
        | and powerful features.
```
- index.pug 파일에 이렇게 작성 후
- index.html로 변환하는 형식으로 사용하면 된다.
- express에서 아예 pug를 받아들이도록 하는 방법 도 있는 것 같다.




## References

<a href="https://basemenks.tistory.com/254">
    Express란 무엇이고 어떻게 사용하는가? (nodeJS / Rest / Serverside Rendering)
</a>