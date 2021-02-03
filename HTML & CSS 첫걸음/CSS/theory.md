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

<br>

## 선택자
<hr>

위에서 설명했듯 선택자는 HTML의 특정한 요소를 선택하는 사인(sign)이다.
여러 종류가 있는데 우선 그중 2가지만 알아보자.

<br>

### 태그로 찾기
<hr>

선택자를 입력하는 부분에 적용하려는(찾으려는) 태그의 이름을 입력한다.

~~~CSS
/*<h1>은 글자색이 빨강이야!*/
h1 {
  color: red;
}
/*<p>는 글자색이 파랑이야!*/
p {
  color: blue;
}
~~~

~~~HTML
<h1>제목1</h1> <!--red-->
<h1>제목2</h1> <!--red-->
<p>본문1</p> <!--blue-->
<p>본문2</p> <!--blue-->
~~~

만약 ‘제목1’과 ‘본문1’에만 색상을 추가하고 싶다면 어떻게 해야 할까?
‘태그 선택자’만 가지고는 어렵다.

<br>

### 클래스로 찾기
<hr>

좀 더 명확하게 원하는 요소를 찾기 위해서 '클래스 선택자'라는 것이 존재한다.
예제를 보자.

~~~CSS
/*class="title"은 글자색이 빨강이야!*/
.title {
  color: red;
}
/*class="main-text"는 글자색이 파랑이야!*/
.main-text {
  color: blue;
}
~~~

~~~HTML
<h1 class="title">제목1</h1> <!--red-->
<h1>제목2</h1>
<p class="main-text">본문1</p> <!--blue-->
<p>본문2</p>
~~~

`class`라는 HTML 속성에 원하는 별명을 입력한다.
제목에는 `title`을 본문에는 `main-text`라는 별명을 지정했다.
이제 CSS에서 이 별명을 기준으로 요소를 찾을 수 있다.
단, 주의할 점은 선택자에 앞에 `.`이 붙는다는 것이다.
`.`은 클래스를 나타내며 CSS의 `.title`은 HTML의 `class="title"`와 동일하다.
`.`이 없는 선택자 `title`은 태그 `<title>`를 의미하게 되니 전혀 다른 뜻으로 인식된다.
이처럼 `.`과 같은 특수한 기호들을 이용해서 HTML과 CSS를 매칭하므로 누락하기 쉽다. 따라서 꼼꼼한 선택자 작성이 중요하다.

<br>

## 속성
<hr>

이제 속성을 알아보자.
크기, 여백, 색상 같은 눈에 보이는 스타일을 지정할 수 있다.

<br>

### 크기
<hr>

\- width(가로 너비)

요소의 가로 너비를 지정한다.
단위는 `px`(pixels)을 사용한다.

~~~CSS
div {
  width: 300px;
  요소가로너비: 너비값;
}
~~~

<br>

\- height(세로 너비)

요소의 세로 너비를 지정한다.

~~~CSS
div {
  height: 150px;
  요소세로너비: 너비값;
}
~~~

<br>

\- font-size(글자 크기)

요소 내용(Text)의 글자 크기를 지정한다.

~~~CSS
div {
    font-size: 16px;
    글자크기: 크기값;
}
~~~

