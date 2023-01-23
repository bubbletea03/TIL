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

- 세로축(반대축) 정렬 : `align-items`
- 예를 들어 `align-items: center` 하면 세로축(반대축)으로 딱 가운데 맞춰짐

[flexbox 연습하기 좋은 웹게임](https://flexboxfroggy.com/#ko)

## 각종 속성들

- 리스트 태그에서 `list-style: none` 하면 그 ● 모양 없앨 수 있음


## CSS 변수

```css
:root {
    --text-color: ~~;
    --background-color: ~~;
    --accent-color: ~~;
}
```
이렇게 써놓고

```css
a {
    color: var(--text-color);
}
```
이런 식으로 사용하면 됨.
- 사용자 정의 변수(?)는 앞에 --를 붙이는 게 컨벤션인듯.


## Grid
- `flex`는 1차원이라면, `grid`는 2차원 레이아웃을 만들기 위해 사용한다.
- `grid-template-columns(또는 rows) : 100px 100px 100px` 이런 식으로 하면 3개의 열이 만들어지는 방식이다.
- 반복해서 적는 것은 `repeat(3, 100px)` 로 간추릴 수 있다.

+ `25% 25% 25% 25%` 처럼 `%`로 부모 태그 기준의 비율을 구현할 수 있다.
+ `1fr 1fr 1fr`로 1:1:1 비율을 구현 가능하다. `1fr 2fr 1fr`은 1:2:1이다.

그 외 참고: 
- `minmax` 함수
- `gap`
- `grid-column(또는 row)-start`, `grid-column(또는 row)-end` - 셀 병합할 때 사용
- `grid-template-areas` - 셀 병합할 때 사용