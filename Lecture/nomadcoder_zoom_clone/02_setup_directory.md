# Server, Frontend 구조 잡기






## Javascript - 환경변수
- __로 시작하는 것들은 JS에서 기본 정의된 변수들임.
- 이걸 환경변수라고 함.
- ex: __dirname, __filename

## Babel 이란
- JS는 물론 TS, JSX등의 유사JS까지 사용자에게 맞는 JS로 변환해주는 컴파일러.
- **크로스 브라우징**이 가능해진다.

+ 강의 따라하면서 @babel/cli, @babel/core, @babel/node, @babel/preset-env 등등 깔았음.

babel.config.json 파일
```json
{
    "presets": ["@babel/preset-env"]
}
```

nodemon.json 파일
```json
{
    "exec": "babel-node src/server.js"
}
```

=> 최종적으로 server.js를 실행하게 됨

- nodemon은 파일에 변경사항 생기면 바로바로 재실행시켜주는 패키지.
- 바뀔 때마다 서버 껐다 키는 번거로움을 덜어줌!

package.json 파일
```json
"scripts": {
    "dev": "nodemon"
  },
```