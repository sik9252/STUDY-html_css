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
