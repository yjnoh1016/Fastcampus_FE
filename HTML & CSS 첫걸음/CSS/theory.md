# CSS
<br>

## 이보다 쉬울 수 없는 CSS 문법
<hr>

CSS 문법은 HTML 보다 더 쉽다.
아래 예시처럼 선택자, 속성, 값이 있으며 무엇을 의미하는지 이해하는 것으로 기본 문법은 충분하다!

~~~CSS
div {
  font-size: 20px;
  color: red;
}

/* 다음과 같이 이해할 수 있다. */
선택자 {
  속성: 값;
  속성: 값;
}
~~~

<br>

### 선택자의 역할
<hr>

선택자는 HTML에 스타일(CSS)을 적용하기 위해 HTML의 특정한 요소를 선택하는 사인(sign)이다.
“빨강 글자색(CSS, `color: red;`)을 저기 제목(HTML, `<h1></h1>`)에 적용하겠어!”, “파랑 글자색(CSS, `color: blue;`)은 여기 본문(HTML, `<p></p>`)에 적용하겠어!”와 같이 적용할 스타일을 속성(`color`)과 값(`red`, `blue`)으로 나타내고 적용할 대상(H1, P)을 선택자로 나타낸다.

위 내용을 코드로 구성하면 다음과 같다.

~~~HTML
<div>
  <h1>제목..</h1>
  <p>본문..</p>
</div>
~~~

~~~CSS
h1 {
  color: red;
}
p {
  color: blue;
}
~~~

<br>

### 속성(Properties)과 값(Value)
<hr>

속성과 값은 글자색은 무엇, 너비는 얼마, 여백은 얼마 같은 스타일을 지정할 때 사용힌다.

~~~CSS
div {
  color: red; /* 글자색은 빨강 */
  font-size: 20px; /* 글자 크기는 20px */
  width: 300px; /* 가로 너비는 300px */
  margin: 20px; /* 바깥 여백은 20px */
  padding: 10px 20px; /* 안쪽 여백은 위아래 10px, 좌우 20px */
  position: absolute; /* 위치는 부모 요소 기준, 이게 무슨 뜻일까? */
}
~~~

속성과 값은 많이 아는 것이 중요하다.
글자 크기를 키우고 싶은데 `font-size`가 어떤 역할을 하는지 모른다면 글자 크기를 조절할 방법이 없다.
또한 위치(좌표)를 지정하고 싶은데 `position` 속성을 모르거나 혹은 그 속성의 값으로 사용하는 `absolute`가 어떤 의미를 갖는지 모르면 역시 방법이 없다.

`I like`처럼 영어가 주어와 동사로 이루진 문법이 전부라고 가정해 보자. 문법은 매우 쉽겠지만 주어에 들어갈 단어는 `You`, `She`, `They` 등이 많은 단어가 있을 것이고, 동사에 들어갈 단어는 `love`, `work`, `eat` 등 수많은 단어들이 들어갈 수 있을 것이다.
많은 단어를 아는 만큼 풍부하고 멋진 문장을 만들 수 있듯, 많은 속성과 값을 아는 만큼 멋진 스타일을 만들어낼 수 있다!

<br>

## CSS 선언 방식
<hr>

이제 내가 작성한 CSS 코드를 어떻게 HTML에 적용할 수 있는지 알아보자.

<br>

### 태그에 직접 작성하기(인라인)
<hr>

이 방법은 HTML 태그에 직접 작성하기 때문에 선택자가 필요하지 않다.

~~~HTML
<div style="color: red;">태그에 직접 작성1</div> <!-- red -->
<div style="color: red;">태그에 직접 작성2</div> <!-- red -->
<div style="color: red;">태그에 직접 작성3</div> <!-- red -->
<div style="color: red;">태그에 직접 작성4</div> <!-- red -->
~~~

<br>

### HTML에 포함하기(내장)
<hr>

CSS만 따로 작성하기 때문에 선택자가 필요하다.
CSS 코드가 HTML의 `<style></style>` 안에 포함되어 있다.

~~~HTML
<head>
  <style>
    div {
      color: red;
    }
  </style>  
</head>
<body>
  <div>HTML에 포함1</div> <!-- red -->
  <div>HTML에 포함2</div> <!-- red -->
  <div>HTML에 포함3</div> <!-- red -->
</body>
~~~

<br>

### HTML 외부에서 불러오기
<hr>

CSS 코드를 완전히 분리할 수 있다.
분리된 하나의 CSS 파일을 여러 HTML 파일이 불러와서 사용할 수 있다.

~~~HTML
<!-- HTML 1 -->
<head>
  <link rel="stylesheet" href="/css/main.css">
</head>
<body>
  <div>HTML에 외부에서 불러오기1</div> <!-- red -->
</body>
~~~

~~~HTML
<!-- HTML 2 -->
<head>
  <link rel="stylesheet" href="/css/main.css">
</head>
<body>
  <div>HTML에 외부에서 불러오기2</div> <!-- red -->
</body>
~~~

~~~CSS
/* main.css */
div {
  color: red;
}
~~~
