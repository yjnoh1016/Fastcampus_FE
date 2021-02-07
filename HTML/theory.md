# HTML

<a href="https://developer.mozilla.org/ko/docs/Web/HTML/Element">MDN</a>
<a href="https://www.w3schools.com/tags/default.asp">W3Schools</a>

## 주요 범위
<hr>

<br>

### \<html>
<hr>

HTML 문서의 범위를 설정.

|속성|의미|값|
|:--:|:--:|:--:|
|lang|문서의 언어(ISO 639-1)|`ko`, `en` …|

<br>

### \<head>
<hr>

HTML 문서의 정보를 설정.

<br>

### \<body>
<hr>

HTML 문서의 구조를 설정.

~~~CSS
body { display: block; }
~~~

<br>

## 메타 데이터
<hr>

<br>

### \<title>
<hr>

브라우저의 제목 표시줄이나 페이지 탭에 보여지는 문서의 제목을 설정.

<br>

### \<base />
<hr>

HTML 문서에 포함된 모든 상대 URL들의 기준 URL를 설정.

- 한 문서에 하나의 `<base/>` 요소만 포함 가능.

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|href|기준 URL|URL||
|target|A 요소처럼 target 속성을 사용하는 요소의 기본값|`_self`, `_blank`|`_self`|

<br>

### \<link />
<hr>

외부 리소스의 연결 및 현재 문서와의 관계를 명시.<br>
(HTML, CSS, ICON 등 가져오기)

|속성|의미|값|
|:--:|:--:|:-:|
|rel|(필수)현재 문서와 외부 리소스와의 관계(Link Types)|`stylesheet`, `icon`…|
|href|외부 리소스의 URL|URL|
|type|외부 리소스의 MIME 타입|`text/css`, `image/x-icon`…|

<br>

### \<meta />
<hr>

기타 메타 데이터 요소(`<link />`, `<style>` 같은)로 나타낼 수 없는 메타데이터를 나타내기 위해 설정.<br>
(검색엔진이나 브라우저에 정보 제공)

|속성|의미|값|
|:--:|:--:|:-:|
|charset|문자인코딩 방식|`UTF-8`, `EUC-KR`…|
|name|메타 데이터의 이름(정보의 종류)|`author`, `description`…|
|http-equiv|서버/사용자 에이전트의 작동방식 변경에 대한 지시(HTTP 응답 헤더 제공)|`refresh`, `X-UA-Compatible`…|
|content|`name`, `http-equiv`의 값||

~~~HTML
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no, maximum-scale=1, minimum-scale=1" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
~~~

<br>

### \<style>
<hr>

스타일 정보(CSS)를 설정.

|속성|의미|값|
|:--:|:--:|:-:|
|type|MIME 타입|`text/css`|

<br>

## 콘텐츠 구분
<hr>

<br>

### \<h1>, \<h2>, \<h3>, \<h4>, \<h5>, \<h6>
<hr>

문서의 정보 계층을 구조화.<br>
(Heading, 문서나 구분된 영역의 제목을 설정, 문서의 목차)

- 숫자가 낮을수록 높은 단계(중요한)의 제목.

~~~CSS
h1, h2, h3, h4, h5, h6 { display: block; }
~~~

<br>

### \<header>
<hr>

문서의 헤더를 설정.<br>
(보통 로고, 제목, 검색 등을 포함)

~~~CSS
header { display: block; }
~~~

<br>

### \<footer>
<hr>

문서의 푸터를 설정.<br>
(보통 작성자, 저작권, 관련 문서 등을 포함)

~~~CSS
footer { display: block; }
~~~

<br>

### \<main>
<hr>

문서의 주요 콘텐츠를 설정.

- IE 지원 불가
- 한 문서에 하나의 `<main>`요소만 포함 가능.

~~~CSS
main { display: block; }
~~~

<br>

### \<article>
<hr>

독립적으로 구분되거나 재사용 가능한 영역을 설정.<br>
(매거진/신문 기사, 블로그 등)

- 일반적으로 `<h1>` ~ `<h6>`를 포함하여 식별.
- 작성일자와 시간을 `<time>`의 `datetime` 속성으로 작성.

~~~CSS
article { display: block; }
~~~

<br>

### \<section>
<hr>

문서의 일반적인 영역을 설정.

- 일반적으로 `<h1>` ~ `<h6>`를 포함하여 식별.

~~~CSS
section { display: block; }
~~~

<br>

### \<aside>
<hr>

문서의 별도 콘텐츠를 설정.<br>
(보통 광고나 기타 링크 등의 사이드바(Side bar)를 설정)

~~~CSS
aside { display: block; }
~~~

<br>

### \<nav>
<hr>

다른 페이지 링크를 제공하는 영역을 설정.<br>
(Navigation, 보통 메뉴(Home, About, Contact), 목차, 색인 등을 설정)

~~~CSS
nav { display: block; }
~~~

<br>

### \<address>
<hr>

`<body>`, `<article>`, `<footer>` 등에서 연락처 정보를 제공하기 위해 포함하여 사용.

~~~CSS
address { display: block; }
~~~

<br>

### \<div>
<hr>

본질적으로 아무것도 나타내지 않는 콘텐츠 영역을 설정.<br>
(Division, 꾸미는 목적을 사용)

~~~CSS
div { display: block; }
~~~

<br>

## 문자 콘텐츠
<hr>

<br>

### \<ol>, \<ul>, \<li>
<hr>

각 항목(`<li>`)의 정렬된 목록(`<ol>`)이나 정렬되지 않은 목록(`<ul>`)을 설정.<br>
(Ordered List, Unordered List, List Item, 순서가 필요하거나(`<ol>`) 순서가 필요하지 않은(`<ul>`) 목록을 정의)

- `<ol>`과 `<ul>`은 자식으로 `<li>`만 포함 가능.
- `<li>`는 단독으로 사용할 수 없으며, `<ol>`이나 `<ul>`에 자식으로 포함되어야 함.
- 정렬된 목록(`<ol>`)의 항목 순서는 중요도를 의미할 수 있음.

~~~CSS
ol, ul { display: block; }
li { display: list-item; }
~~~

<br>

#### \<ol>
<hr>

정렬된 목록을 설정.


|속성|의미|값|특징|
|:--:|:--:|:-:|:--:|
|start|항목에 매겨지는 번호의 시작 값|숫자(Number)||
|type|항목에 매겨지는 번호의 유형|`a`, `A`, `i`, `I`, `1`||

<br>

#### \<li>
<hr>

항목을 설정.


|속성|의미|값|특징|
|:--:|:--:|:-:|:--:|
|value|항목의 순서를 설정|숫자(Number)|이하 항목들의 순서가 다시 지정됨|

<br>

### \<dl>, \<dt>, \<dd>
<hr>

용어(`<dt>`)와 정의(`<dd>`) 쌍들의 영역(`<dl>`)을 설정.<br>
(Description List, Definition Details, Definition Term)

- `<dl>`은 `<dd>`, `<dt>`만을 포함해야 함.
- 키(key)/값(value) 형태를 표시할 때 유용.

~~~HTML
<dl>
  <dt>Coffee</dt>
  <dd>Coffee is a brewed drink prepared from roasted coffee beans, the seeds of berries from certain Coffea species.</dd>
  <dt>Milk</dt>
  <dd>Milk is a nutrient-rich, white liquid food produced by the mammary glands of mammals.</dd>
</dl>
~~~

~~~CSS
dl, dt, dd { display: block; }
~~~

<br>

### \<p>
<hr>

하나의 문단을 설정.<br>
(Paragraph)

- 일반적으로 정보통신보조기기 등은 다음 문단(`<p>`)으로 넘어갈 수 있는 단축키를 제공함.

~~~CSS
p { display: block; }
~~~

<br>

### \<hr />
<hr>

문단의 분리(주제에 의한)를 위해 설정.<br>
(Horizontal Rule)

- 대부분의 경우 수평선(`border`)으로 표시(표현적 관점)되나 의미적 관점으로만 사용해야 함.

~~~CSS
hr { display: block; }
~~~

<br>

### \<pre>
<hr>

서식이 미리 지정된 텍스트를 설정.<br>
(Preformatted Text)

- 텍스트의 공백과 줄바꿈을 유지하여 표시할 수 있음.
- 기본적으로 Monospace 글꼴 계열로 표시됨.

~~~CSS
pre { display: block; }
~~~

<br>

### \<blockquote>
<hr>

일반적인 인용문을 설정.<br>
(Block Quotation)

|속성|의미|값|
|:--:|:--:|:-:|
|cite|인용된 정보의 URL|URL|

~~~CSS
blockquote { display: block; }
~~~
