# STUDY-html_css

기본적인 HTML과 CSS에 대한 공부 기록

---

<a href="https://codingapple.com/">공부할때 수강한 인강(1)</a>

---

## HTML 기초와 기본 구조

모든 html 파일은 항상 이렇게 써놓고 시작해야 한다.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

---

## HTML 기본 태그

HTML은 Markup Language로 자료가 어디에 어떻게 배치되어있나(자료의 구조)를 표현하기 위한 언어이므로 태그 안에 글을 적어주는것이 좋다.

```html
<h1></h1>
<p></p>
<img src="이미지 경로" />
<button>버튼</button>
<a href="주소">링크</a>
<ul>
  <li>항목1</li>
  <li>항목2</li>
</ul>
```

- h1 태그의 h는 heading의 약자로 글 제목을 적을때 사용한다.

  (h1~h6까지 사용할수 있고, 숫자가 커질수록 글자 크기가 작아진다)

- p 태그는 paragrpah의 약자로 문단을 나눌때 사용한다.
- img 태그는 src라는 속성에 "이미지 경로"를 넣어줘야 한다.
- 말 그대로 버튼을 생성한다.
- href 속성에 이동할 링크 주소를 적어 링크를 생성한다.
- 리스트는 `<ul><li>리스트</li></ul>` 와 같이 작성한다.
  (그리고 ul은 unorder list의 약자이고 li는 list item의 약자이다)
- 리스트에 자동 번호를 넣고싶다면 ul대신 ol(order list)을 사용하면 된다.

- 이미지 누르면 특정 사이트로 이동하게 할수 있음

  `<a href="주소"> <img src="이미지 경로"> </a>`

- <문제> 글자의 일부를 눌렀을때 네이버로 이동하게 하려면 어떻게 해야할까?

```html
<p>안녕하세요 <a href="https://naver.com">이동하기</a></p>
```

### [정리]

> 웹 페이지 만들때 모든 요소는 태그 안에 작성한다.

> 일부 태그는 속성을 기입할수 있다. ex) src, href

> 태그 안에 태그도 넣을수 있다. ex) `<ul><li></li></ul>`

---

## 기본적인 웹페이지 스타일링

html 꾸미는 법 => style 속성을 이용해 스타일명:값 형태로 작성한다.

`<img src="이미지 경로" style="width: 100px; margin: 30px"/>`

<span style="color:orange">이미지를 가운데 정렬하는 법</span>

> display: block;

> margin-left: auto;

> margin-right: auto;

이 3가지를 적어주면 된다.<br><br>

<단위 종류>

- vw: 현재 브라우저 창의 너비를 의미 따라서 16vw면 현재 브라우저 창의 16배로 설정

- %: 내 부모 사이즈에 비례 100%면 내 부모 사이즈의 100%로 설정<br><br>

<글자 스타일링 방법>

- font-size: 폰트 크기 설정
- font-weight: 폰트 굵기 설정

  `<strong></strong>` 태그를 이용해도 된다.

- font-family: 폰트 종류 설정
- color: 폰트 색상 설정
- letter-spacing: 자간 간격 조절
- text-align: center -> 글자 가운데 정렬

(text-align: right는 오른쪽 정렬, left는 왼쪽 정렬)<br><br>

<문제> 문장 중에 일부 글자만 스타일링 하고싶으면 어떻게 할까?

`<p><span style="color:red">Front-end</span> Developer</p>`

이런식으로 작성해준다.

span 태그란 글자를 감쌀수 있는 별 뜻 없는 태그라고 생각하면 된다.

---

## 레이아웃의 기초 - div

div: division의 약자로, 화면을 분할하겠다는 의미. 네모난 박스 만들고 싶을때 사용하자.
<br><br>

### `<div>` 박스 디자인에 자주 사용하는 속성들

1.  margin: 상하좌우 "바깥쪽" 여백 (margin-top/bottom/left/right도 있음)

    > margin은 음수도 가능함

    > margin: 5px 6px 7px 8px 과 같이 사용하면 순서대로 상 우 하 좌 여백을 준다.

2.  padding: 상하좌우 "안쪽" 여백

3.  border: 테두리(ex. border: 4px solid black;)

4.  border-radius: 테두리를 둥글게 하고싶을때

5.  div 박스도 가운데 정렬하고 싶으면 이미지와 마찬가지로 아래 css를 사용한다.

> display: block;

> margin-left: auto;

> margin-right: auto;

<br>

### `<div>` 박스의 특징

1. display: block 이 기본으로 있음(따라서 생략 가능)

   또한 p, h1, li 등의 태그도 display: block 속성이 기본적으로 내장되어있다.

   따라서 이 태그들을 그냥 사용하면 한 행을 전부 차지하게 되므로 display 속성에 inline, inline-block, flex 등을 이용해 다른 것을 부여해서 바꿀 수 있다.

font-size, color, font-family, text-align과 같은 속성들은 부모 태그에 적어주면 안의 자식 태그들까지 전부 상속(inherit) 된다.

---

## 레이아웃 만들기(1) - float

Tip) 여러 레이아웃을 만들기 전에 여러 레이아웃을 한번에 감싸는 박스를 만들어두면 유용하다.

생성한 박스들을 눈에 보이게 하려면 스타일에 width와 height 값을 주자.

layout1.html의 mainContent에 css를 주고나면 아래 이미지처럼 해당 박스가 leftMenu의 오른쪽이 아닌 아래쪽에 나타나는것을 볼 수 있다. 왜 그럴까?

<img src="image/mainContentEx.png" style="width:300px; height:200px"><br>

> <strong>div 박스들은 모두 display: block 속성을 내장</strong>하고 있기 때문에 가로행을 전부 차지한다.
> 따라서 leftMenu의 width: 20%여도 실제로는 화면의 가로행을 다 차지하고 있기 때문에 다음 div 박스는 아래에 위치하게 된다.

이것을 해결하는 방법에는 먼저 css에 float 속성을 이용하는 방법이 있다.

`float: left;`

이는 해당 요소를 붕 띄워서 왼쪽에 정렬하라는 의미를 가지고 있다.

오른쪽으로 정렬하고 싶으면 float: right를 사용하자.

<span style="color: orange">즉, 박스를 가로로 배치할 때 float를 사용해보자.</span>

아래 코드처럼 레이아웃 구조가 있다고 해보자.

```html
<body>
  <div class="container">
    <div class="header"></div>
    <div class="leftMenu"></div>
    <div class="mainContent"></div>
    <div class="footer"></div>
  </div>
</body>
```

```css
/* footer의 css */
.footer {
  width: 100%;
  height: 100px;
  background-color: grey;
}
```

이때 footer에 css 스타일을 작성하면 footer는 아래 이미지처럼 leftMenu와 mainContent의
뒤에 가려져서 안보이게 된다.

<img src="image/footerEx.png" style="width:300px; height:200px">

<br>
이렇게 되는 이유는 이전에 leftMenu와 mainContent의 스타일로 float를 주었기 때문에 이 둘은 공중에 떠있는 상태다. (아까 float를 사용하면 요소가 붕 뜬다고 적어놨다.)
따라서 footer는 이 붕 떠있는 요소들 뒤에 위치하게 되는 것이다.

이를 해결하려면 어떻게 해야할까?

`clear: both;`

이것을 사용하자. 이는 float 다음에 오는 요소에게 주면 float를 사용함으로써 발생하는 위와 같은 현상을 해결할 수 있다.

---

## 레이아웃 만들기(2) - inline-block

이전에 배운 float 말고 박스를 가로로 배치할 수 있는 다른 방법이 있다.

```css
.leftMenu {
  display: inline-block;
  width: 20%;
  height: 400px;
  background-color: cornflowerblue;
}
```

> display: block -> 한 행을 전부 차지한다.

> display: inline-block -> 자신의 크기만큼 자리를 차지한다.
> ex) 한글에서 이미지 넣으면 글자와 어울림하는 느낌

그런데 문제가 있다.

### inline-block 사용하면 일어나는 문제점(1)

inline-block을 사용하면 각 박스를 생성한 코드 사이의 빈 공간(ex. 스페이스바)만큼 실제 레이아웃 사이에도 공백이 생겨버려 가로배치가 아닌 세로배치가 될 수도 있다.

따라서 inline-block을 사용하려면 공백을 제거해줘야 한다.

<공백 제거 Tip>

1. html 주석을 이용해 엔터를 사용한처럼 만들어주기
2. 부모 태그에 font-size: 0px; 주기

근데 부모 태그에 font-size: 0px을 주면 그 아래 자식들 블록 안에 글을 작성하면 크기가 0이라 보이지 않게 된다. 그래서 글을 쓸 블록 태그에 다시 font-size를 줘야한다.

(즉, 공백 제거하기 귀찮으므로 그냥 float를 쓰는게 나을것 같다.)

### inline-block 사용하면 일어나는 문제점(2)

inline-block으로 생성된 박스 안에 p태그 같은거 이용해서 글쓰면 정렬이 망가진다.

왜 그럴까?

글자를 입력할때 가상의 baseline이 존재하는데 만일 baseline이 옆에 존재한다면 display: inline-block 요소들이 baseline의 위에 오려고하기 때문이다.

<strong>해결법</strong>은 해당 요소의 스타일에 `vertical-align` 속성값을 주는것!

vertical-align 속성은 상하정렬의 역할을 하는 것으로 위로 보낼건지 밑으로 보낼건지 결정하는건데 이는 inline 을 가지고 있는 요소들에만 적용이 가능하다.
