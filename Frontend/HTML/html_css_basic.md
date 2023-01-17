# 드림코딩 유튭 보면서 html/css 지식 필기

## HTML 구조
- 주로 header, main contents, sidebar, footer 이런 큰 박스들로 나눠진다.
- 큰 박스 안에 작은 박스들로 나눠진다.

https://youtu.be/i0FN-OwJ7QI

## Block, Inline
- Block은 한 줄에 하나
- Inline은 공간이 허용하면 바로 옆에도 배치 가능

+ Block: `div`, `p` 등
+ Inline: `span`, `b`, `input` 등
  

## 선택자 (Selector) 몰랐던 거
 
- `a[href="naver.com"]` => 속성(Attribute)이 href="naver.com"인 a를 고른다.
- `^="naver"` naver로 시작하는
- `$=".com"` .com으로 끝나는

- `:`는 가상 선택자(Pseudo Selector)로, 요소의 상태에 따라 선택. ex) `:first-child`는 첫자식인 것을 선택

## padding 같이 방향별로 있는 거
- padding: top right bottom left; 순으로 사용 가능 (시계방향)
- border: size style color; 순으로 사용 가능

[CSS Properties 참고 사이트](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#index)
[CSS 게임으로 공부하기! 사이트](https://flukeout.github.io/)

## %와 vw, vh

- %의 의미: **부모**의 몇 퍼센트 만큼을 차지한다는 뜻. ex) height:100%
- vw, vh: viewport-height라는 뜻. **사용자에게 보이는 스크린 크기**를 기준으로 함. 100vh는 스크린을 100% 채우겠다는 뜻.

[UI 색깔 찾기 좋은 사이트 COLOR TOOL](https://m2.material.io/resources/color/#!/?view.left=0&view.right=0&primary.color=CE93D8)

## flexbox

[flexbox 연습하기 좋은 웹게임](https://flexboxfroggy.com/#ko)