# HTML

<a href="https://developer.mozilla.org/ko/docs/Web/HTML/Element">MDN</a>
<a href="https://www.w3schools.com/tags/default.asp">W3Schools</a>

## 주요 범위

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

<br>

## 인라인 텍스트

<br>

### \<a>
<hr>

다른 페이지, 같은 페이지 위치(`#`, 해시 태그), 파일, 이메일 주소, 전화번호 등 다른 URL로 연결할 수 있는 하이퍼링크를 설정.<br>
(Anchor, 외부로 내보내기)

|속성|의미|값|기본값|특징|
|:--:|:--:|:-:|:---:|:--:|
|download|이 요소가 리소스를 다운로드 하는 용도로 사용됨을 의미|불린(Boolean)|||
|href|링크 URL|URL||생략 가능|
|rel|현재 문서와 링크 URL의 관계(Link Types)|`license`, `prev`, `next`…|||
|target|링크 URL의 표시(브라우저 탭) 위치|`_self`, `_blank`|`_self`||
|type|링크 URL의 MIME 타입|`text/html`…|||

~~~CSS
a { display: inline; }
~~~

<br>

### \<abbr>
<hr>

약어를 지정.<br>
(Abbreviation, 보통 `title` 속성을 사용하여 전체 글자나 설명을 제공)

~~~HTML
Using <abbr title="HyperText Markup Language">HTML</abbr> is fun and easy!
~~~

~~~CSS
abbr { display: inline; }
~~~

<br>

### \<b>
<hr>

문체가 다른 글자의 범위를 설정.<br>
(Bring Attention)

- 특별한 의미를 가지지 않음.
- 읽기 흐름에 도움을 주는 용도로 사용.
- 다른 태그가 적합하지 않은 경우 마지막 수단으로 사용.
- 기본적으로 글자가 두껍게(Bold) 표시됨.

~~~CSS
b { display: inline; }
~~~

<br>

### \<mark>
<hr>

사용자의 관심을 끌기 위해 하이라이팅할 때 사용.<br>
(Mark Text, 형광펜을 사용하여 관심있는 부분을 표시하는 것과 같은 의미)

- 기본적으로 형광펜을 사용한 것처럼 글자 배경이 노란색(Yellow)으로 표시됨.

~~~CSS
mark { display: inline; }
~~~

<br>

### \<em>
<hr>

단순한 의미 강조를 표시.<br>
(Emphasis)

- 중첩이 가능.
- 중첩될수록 강조 의미가 강해짐.
- 정보통신보조기기 등에서 구두 강조로 발음됨.
- 기본적으로 이탤릭체(Italic type)로 표시됨.

~~~CSS
em { display: inline; }
~~~

<br>

### \<strong>
<hr>

의미의 중요성을 나타내기 위해 사용.<br>
(Strong Importance)

- 기본적으로 글자가 두껍게(Bold) 표시됨.

~~~CSS
strong { display: inline; }
~~~

<br>

### \<i>
<hr>

`<em>`, `<strong>`, `<mark>`, `<cite>`, `<dfn>` 등에서 표현할 수 있는 적합한 의미가 아닌 경우 사용.<br>
(평범한 글자와 구분(아이콘이나 특수기호 같은)하기 위해 사용)

- 기본적으로 이탤릭체(Italic type)로 표시됨.

~~~CSS
i { display: inline; }
~~~

<br>

### \<dfn>
<hr>

용어를 정의할 때 사용.<br>
(Definition)

~~~CSS
dfn { display: inline; }
~~~

<br>

### \<cite>
<hr>

창작물에 대한 참조를 설정.<br>
(책, 논문, 영화, TV 프로그램, 노래, 게임 등의 제목)

- 기본적으로 이탤릭체(Italic type)로 표시됨.

~~~HTML
<cite>The Scream</cite> by Edward Munch. Painted in 1893.
~~~

~~~CSS
cite { display: inline; }
~~~

<br>

### \<q>
<hr>

짦은 인용문을 설정.<br>
(Inline Quotation)

- 긴 인용문을 설정할 경우 `<blockquote>`를 사용.

|속성|의미|값|
|:--:|:--:|:-:|
|cite|인용된 정보의 URL|URL|

~~~CSS
q { display: inline; }
~~~

<br>

### \<u>
<hr>

밑줄이 있는 글자를 설정.<br>
(Underline)

- 순수하게 꾸미는 용도의 요소로 사용.
- `<a>`와 헷갈릴 수 있는 위치에서 사용하지 않도록 주의.
- `<span style="text-decoration: underline;">`을 활용할 수 있을 경우에는 사용을 권장하지 않음.

~~~CSS
u { display: inline; }
~~~

<br>

### \<code>
<hr>

컴퓨터 코드 범위를 설정.<br>
(Inline Code)

`<code>document.getElementById('id-value')</code> is a piece of computer code.`

- 기본적으로 고정폭(Monospace) 글꼴 계열로 표시됨.

~~~CSS
code { display: inline; }
~~~

<br>

### \<kbd>
<hr>

텍스트 입력 장치(키보드)에서 사용자 입력을 나타내는 텍스트 범위를 설정.<br>
(Keyboard Input)

~~~HTML
<p><kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>K</kbd></p>, <kbd>ESC</kbd>
~~~

~~~CSS
kbd { display: inline; }
~~~

<br>

### \<sup>, \<sub>
<hr>

위 첨자(`<sup>`)와 아래 첨자(`<sub>`)를 설정.<br>
(Superscripted text, Subscript text)

~~~HTML
X<sup>4</sup> + Y<sup>2</sup>, H<sub>2</sub>O
~~~

~~~CSS
sup, sub { display: inline; }
~~~

<br>

### \<time>
<hr>

날짜나 시간을 나타내기 위한 목적으로 사용.

|속성|의미|값|
|:--:|:--:|:-:|
|datetime|유효한 날짜 문자|Date|

- IE 지원 불가

~~~HTML
<p>The Cure will be celebrating their 40th anniversary on <time datetime="2018-07-07">July 7</time> in London's Hyde Park.</p>
~~~

~~~CSS
time { display: inline; }
~~~

<br>

### \<span>
<hr>

본질적으로 아무것도 나타내지 않는 콘텐츠 영역을 설정.

~~~CSS
span { display: inline; }
~~~

<br>

### \<br />
<hr>

줄바꿈을 설정.

~~~CSS
br { display: inline; }
~~~

<br>

## 수정

<br>

### \<del>
<hr>

삭제된(변경된) 텍스트의 범위를 지정.

|속성|의미|값|
|:--:|:--:|:-:|
|cite|변경을 설명하는 리소스의 URI|URI|
|datetime|변경이 일어난 유요한 날짜 문자|Date|

~~~CSS
del { display: inline; }
~~~

<br>

### \<ins>
<hr>

새로 추가된(변경된) 텍스트의 범위를 지정.

|속성|의미|값|
|:--:|:--:|:-:|
|cite|변경을 설명하는 리소스의 URI|URI|
|datetime|변경이 일어난 유요한 날짜 문자|Date|

~~~CSS
ins { display: inline; }
~~~

<br>

## 멀티미디어

<br>

### \<img />
<hr>

이미지를 삽입.

|속성|의미|값|
|:--:|:--:|:-:|
|src|(필수)이미지 URL|URL|	
|alt|(필수)이미지의 대체텍스트||	
|width|이미지의 가로 너비||	
|height|이미지의 세로 너비||	
|srcset|브라우저에게 제시할 이미지 URL과 원본 크기의 목록을 정의|`w`, `x`|
|sizes|미디어 조건과 해당 조건일 때 이미지 최적화 크기의 목록을 정의||	

~~~HTML
<!-- srcset, sizes -->
<!-- 다양한 디스플레이 해상도에 맞는 최적의 이미지를 브라우저가 선택해서 사용 -->
<img srcset="./small.jpg 320w,
             ./medium.jpg 640w,
             ./large.jpg 1024w"
     sizes="(max-width: 480px) 300px,
            (max-width: 800px) 600px,
            900px"
     src="./small.jpg"
     alt="The image" />
<img srcset="./image.jpg,
             ./image-1.5x.jpg 1.5x,
             ./image-2x.jpg 2x"
     src="./image.jpg"
     alt="The image" />
~~~

~~~CSS
img { display: inline; }
~~~

<br>

### \<audio>
<hr>

소리 콘텐츠(MP3)를 삽입.

- `autoplay`가 지정된 경우, `preload`는 무시됨.

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|autoplay|준비되면 바로 재생|불린(Boolean)||	
|controls|제어 메뉴를 표시|불린(Boolean)||	
|loop|재생이 끝나면 다시 처음부터 재생|불린(Boolean)||	
|preload|페이지가 로드될 때 파일을 로드할지의 지정(힌트 제공)|`none`: 로드하지 않음, <br> `metadata`: 메타데이터만 로드, <br>`auto`: 전체 파일 로드|`metadata`|
|src|콘텐츠 URL|URL||	
|muted|음소거 여부|불린(Boolean)||

~~~CSS
audio { display: inline; }
~~~

<br>

### \<video>
<hr>

동영상 콘텐츠(MP4)를 삽입.

- `autoplay`가 지정된 경우, `preload`는 무시됨.

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|autoplay|준비되면 바로 재생|불린(Boolean)||	
|controls|제어 메뉴를 표시|불린(Boolean)||	
|loop|재생이 끝나면 다시 처음부터 재생|불린(Boolean)||
|muted|음소거 여부|불린(Boolean)||
|poster|동영상 썸네일 이미지 URL|URL||	
|preload|페이지가 로드될 때 파일을 로드할지의 지정(힌트 제공)|`none`: 로드하지 않음, <br> `metadata`: 메타데이터만 로드, <br>`auto`: 전체 파일 로드|`metadata`|
|src|콘텐츠 URL|URL||	
|widht|동영상 가로 너비|||
|height|동영상 세로 너비|||

~~~CSS
video { display: inline; }
~~~

<br>

### \<figure>, \<figcaption>
<hr>

`<figure>`는 이미지나 삽화, 도표 등의 영역을 설정.<br>
`<figcaption>`는 `<figure>`에 포함되어 이미지나 삽화 등의 설명을 표시.(Figure Caption)

~~~HTML
<figure>
  <img src="milk.jpg" alt="A milk">
  <figcaption>Milk is a nutrient-rich, white liquid food produced by the mammary glands of mammals.</figcaption>
</figure>
~~~

~~~CSS
figure { display: block; }
figcation { display: inline; }
~~~

<br>

## 내장 콘텐츠

<br>

### \<iframe>
<hr>

다른 HTML 페이지를 현재 페이지에 삽입.<br>
(중첩된 브라우저 컨텍스트(프레임)를 표시)

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|name|프레임의 이름|||		
|src|포함할 문서의 URL|URL||	
|width|프레임의 가로 너비|||		
|height|프레임의 세로 너비|||		
|allowfullscreen|전체 화면 모드 사용 여부|불린(Boolean)||	
|frameborder|프레임 테두리 사용 여부|`0`, `1`|`1`|
|sandbox|보안을 위한 읽기 전용으로 삽입|불린(Boolean) or <br>`allow-form`: 양식 제출 가능, <br>`allow-scripts`: 스크립트 실행 가능 , <br>`allow-same-origin`: 같은 출처(도메인)의 리소스 사용 가능	

~~~HTML
<iframe width="1280" height="720" src="https://www.youtube.com/embed/Q9yn1DpZkHQ" frameborder="0" allowfullscreen></iframe>
~~~

~~~CSS
iframe { display: inline; }
~~~

<br>

### \<canvas>
<hr>

Canvas API이나 WebGL API를 사용하여 그래픽이나 애니메이션을 랜더링.

|속성|의미|
|:--:|:--:|
|width|캔버스의 가로 너비|
|height|캔버스의 세로 너비|

~~~CSS
canvas { display: inline; }
~~~

<br>

## 스크립트

<br>

### \<script>
<hr>

스크립트 코드를 문서에 포함하거나 참조(외부 스크립트).

|속성|의미|값|특징|
|:--:|:--:|:-:|:--:|
|async|스크립트의 비동기적(Asynchronously) 실행 여부|불린(Boolean)|`src` 속성 필수|
|defer|문서 파싱(구문 분석) 후 작동 여부|불린(Boolean)|`src` 속성 필수|
|src|참조할 외부 스크립트 URL|URL|포함된 스크립트 코드는 무시됨|
|type|MIME 타입|`text/javascript`(기본값)||

~~~CSS
script { display: none; }
~~~

<br>

### \<noscript>
<hr>

스크립트를 지원하지 않는 경우에 삽입할 HTML을 정의.

~~~HTML
<noscript>
  <p>Your browser does not support JavaScript!</p>
</noscript>
~~~

~~~CSS
noscript { display: inline; }
~~~

<br>

## 표 콘텐츠

<br>

~~~HTML
<table>
  <caption>Fruits</caption>
  <colgroup>
    <col span="2" style="background-color: yellowgreen;">
    <col style="background-color: tomato;">
  </colgroup>
  <thead>
    <tr>
      <th>ID</th>
      <th>Name</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>F123A</td>
      <td>Apple</td>
      <td>$22</td>
    </tr>
    <tr>
      <td>F098B</td>
      <td>Banana</td>
      <td>$19</td>
    </tr>
  </tbody>
</table>
~~~

<br>

### \<table>, \<tr>, \<th>, \<td>
<hr>

데이터 표(`<table>`)의 행(줄 / `<tr>`)과 열(칸, 셀(Cell) / `<th>`, `<td>`)을 생성.<br>
(Table Row, Table Header, Table Data)

~~~CSS
table { display: table; }
tr { display: table-row; }
th, td { display: table-cell; }
~~~

<br>

#### \<th>
<hr>

'머리글 칸'을 지정

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|abbr|열에 대한 간단한 설명|||		
|headers|관련된 하나 이상의 다른 머리글 칸 `id` 속성 값|||		
|colspan|확장하려는(병합) 열의 수	||`1`|
|rowspan|확장하려는(병합) 행의 수||`1`|
|scope|자신이 누구의 ‘머리글 칸’인지 명시|`col`: 자신의 열 <br>`colgroup`: 모든 열 <br>`row`: 자신의 행 <br>`rowgroup`: 모든 행 <br>`auto`|auto|

<br>

#### \<td>
<hr>

'일반 칸'을 지정

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|headers|관련된 하나 이상의 다른 머리글 칸 `id` 속성 값|||
|colspan|확장하려는(병합) 열의 수||`1`|
|rowspan|확장하려는(병합) 행의 수||`1`|

<br>

### \<caption>
<hr>

표의 제목을 설정.

- 열리는 TABLE 태그 바로 다음에 작성해야 함.
- \<table> 당 하나의 \<caption>만 사용 가능.

~~~CSS
caption { display: table-caption; }
~~~

<br>

### \<colgroup>, \<col />
<hr>

표의 열들을 공통적으로 정의하는 컬럼(`<col>`)과 그의 집합(`<colgroup>`).<br>
(Column, Column Group)

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|span|연속되는 열 수|숫자(Number)|`1`|

~~~CSS
colgroup { display: table-column-group; }
col { display: table-column; }
~~~

<br>

### \<thead>, \<tbody>, \<tfoot>
<hr>

표의 머리글(`<thead>`), 본문(`<tbody>)`, 바닥글(`<tfoot>`)을 지정.

- 기본적으로 테이블의 레이아웃에 영향을 주지 않음.

~~~CSS
thead { display: table-header-group; }
tbody { display: table-row-group; }
tfoot { display: table-footer-group; }
~~~

<br>

## 양식

<br>

### \<form>
<hr>

웹 서버에 정보를 제출하기 위한 양식 범위를 정의.

- `<form>`이 다른 `<form>`을 자식 요소로 포함할 수 없음.

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|action|전송한 정보를 처리할 웹페이지의 URL|URL||	
|autocomplete|사용자가 이전에 입력한 값으로 자동 완성 기능을 사용할 것인지 여부|`on`, `off`|`on`|
|method|서버로 전송할 HTTP 방식|`GET`, `POST`|`GET`|
|name|고유한 양식의 이름|||		
|novalidate|서버로 전송시 양식 데이터의 유효성을 검사하지 않도록 지정|||		
|target|서버로 전송 후 응답받을 방식을 지정|`_self`, `_blank`|`_self`|

~~~CSS
form { display: block; }
~~~

<br>

### \<input />
<hr>

사용자에게 입력 받을 데이터 양식.

|속성|의미|값|기본값|특징|
|:--:|:--:|:-:|:---:|:--:|
|autocomplete|사용자가 이전에 입력한 값으로 자동 완성 기능을 사용할 것인지 여부|`on`, `off`|`on`||	
|autofocus|페이지가 로드될 때 자동으로 포커스|불린(Boolean)||문서 내 고유해야 함|
|checked|양식이 선택되었음을 표시|불린(Boolean)||`type` 속성 값이 `radio`, `checkbox`일 경우만|
|disabled|양식을 비활성화|불린(Boolean)|||		
|form|`<form>`의 `id` 속성 값|||해당 `<form>`의 후손이 아닐 경우만|
|list|참조할 `<datalist>`의 `id` 속성 값||||			
|max|지정 가능한 최대 값|숫자(Number)||`type` 속성 값이 `number`일 경우만, `min`속성보다 큰 값만 허용|
|min|지정 가능한 최소 값|숫자(Number)||`type` 속성 값이 `number`일 경우만, `max`속성보다 작은 값만 허용|
|maxlength|입력 가능한 최대 문자 수|숫자(Number)|`524288`|`type` 속성 값이 `text`, `email`, `password`, `tel`, `url`일 경우만|
|multiple|둘 이상의 값을 입력 할 수 있는지 여부|불린(Boolean)||`type` 속성 값이 `email`, `file`일 경우만, `email`일 경우 `,`로 구분|
|name|양식의 이름||||			
|placeholder|사용자가 입력할 값의 힌트|||`type` 속성 값이 `text`, `search`, `tel`, `url`, `email`일 경우만
|readonly|수정 불가한 읽기 전용|불린(Boolean)|||		
|step|유효한 증감 숫자의 간격|숫자(Number)|`1`|`type` 속성 값이 `number`, `range`일 경우만|
|src|이미지의 URL|URL||`type` 속성 값이 `image`일 경우만|
|alt|이미지의 대체 텍스트|||`type` 속성 값이 `image`일 경우만|
|type|입력 받을 데이터의 종류|별도 정리|`text`||
|value|양식의 초기 값||||

<br>

### 데이터 종류(Type)의 값(Values)
<hr>

`type`속성에 입력할 수 있는 값의 목록.

~~~HTML
<input type="button" />
<input type="checkbox" />
<input type="file" />
<input type="text" />
~~~

|값|데이터 종류|특징|
|:-:|:------:|:--:|
|button|일반 버튼|`<button>`처럼 사용|
|checkbox|체크박스||	
|color|색상|IE 지원 불가|
|email|이메일||	
|file|파일||	
|hidden|보이지 않지만 전송할 양식|`value` 속성으로 값을 지정|
|image|이미지 제출 버튼|`<img />`처럼 사용|
|number|숫자||	
|password|비밀|가려지는 양식|
|radio|라디오 버튼|같은 `name` 속성 그룹 내 하나만 선택 가능|
|range|범위 컨트롤|`min`, `max`, `step`, `value`(기본값) 속성 사용|
|reset|초기화|해당 `<form>` 범위 내 모든 양식|
|search|검색||	
|submit|제출 버튼|해당 `<form>` 범위 내 고유한 양식|
|tel|전화번호||	
|text|일반 텍스트||	
|url|절대 URL||

~~~CSS
input { display: inline-block; }
~~~

<br>

### \<label>
<hr>

라벨 가능 요소(labelable)의 제목(Caption).

- `for`속성으로 라벨 가능 요소를 참조하거나 콘텐츠로 포함.
- 라밸 가능 요소: `<button>`, `<input>`, `<progress>`, `<select>`, `<textarea>`

|속성|의미|
|:--:|:--:|
|for|참조할 라벨 가능 요소의 `id` 속성 값|

~~~HTML
<!-- 라벨 가능 요소를 참조 -->
<input type="checkbox" id="user-agreement" />
<label for="user-agreement">동의하십니까?</label>

<!-- 라벨 가능 요소를 포함 -->
<label><input type="checkbox" />동의하십니까?</label>
~~~

~~~CSS
label { display: inline; }
~~~

<br>

## \<button>
<hr>

선택 가능한 버튼을 지정.

|속성|의미|값|특징|
|:--:|:--:|:-:|:--:|
|autofocus|페이지가 로드될 때 자동으로 포커스|불린(Boolean)|문서 내 고유해야 함|
|disabled|버튼을 비활성화|불린(Boolean)||	
|form|`<form>`의 `id` 속성 값||해당 `<form>`의 후손이 아닐 경우만|
|name|폼 데이터와 함께 전송되는 버튼의 이름|||		
|type|버튼의 타입|`button`, `reset`, `submit`||

~~~CSS
button { display: inline-block; }
~~~

<br>

### \<textarea>
<hr>

여러 줄의 일반 텍스트 양식.

|속성|의미|값|기본값|특징|
|:--:|:--:|:-:|:---:|:--:|
|autocomplete|사용자가 이전에 입력한 값으로 자동 완성 기능을 사용할 것인지 여부|`on`, `off`|`on`||	
|autofocus|페이지가 로드될 때 자동으로 포커스|불린(Boolean)||문서 내 고유해야 함|
|disabled|양식을 비활성화|불린(Boolean)|||		
|form|`<form>`의 `id` 속성 값|||해당 `<form>`의 후손이 아닐 경우만|
|maxlength|입력 가능한 최대 문자 수|숫자(Number)|무한||	
|name|양식의 이름||||			
|placeholder|사용자가 입력할 값의 힌트||||			
|readonly|수정 불가한 읽기 전용|불린(Boolean)|||		
|rows|양식의 줄 수|숫자(Number)|`2`||

~~~CSS
textarea { display: inline-block; }
~~~

<br>

### \<fieldset>, \<legend>
<hr>

같은 목적의 양식을 그룹화(`<fieldset>`)하여 제목(`<legend>`)을 지정.

~~~HTML
<form>
  <fieldset>
    <legend>Coffee Size</legend>
    <label>
        <input type="radio" name="size" value="tall" />
        Tall
    </label>
    <label>
        <input type="radio" name="size" value="grande" />
        Grande
    </label>
    <label>
        <input type="radio" name="size" value="venti" />
        Venti
    </label>
  </fieldset>
</form>
~~~

~~~CSS
fieldset, legend { display: block; }
~~~

<br>

#### \<fieldset>
<hr>

같은 목적의 양식을 그룹화.

|속성|의미|값|
|:--:|:--:|:-:|
|disabled|그룹 내 모든 양식 요소를 비활성화|불린(Boolean)|
|form|그룹이 속할 하나 이상의 `<form>`의 `<id>`속성 값||
|name|그룹의 이름||

<br>

### \<select>, \<datalist>, \<optgroup>, \<option>
<hr>

옵션(`<option>`, `<optgroup>`)의 선택 메뉴(`<select>`)나 자동완성(`<datalist>`)을 제공.

~~~HTML
<select>
  <optgroup label="Coffee">
    <option>Americano</option>
    <option>Caffe Mocha</option>
    <option label="Cappuccino" value="Cappuccino"></option>
  </optgroup>
  <optgroup label="Latte" disabled>
    <option>Caffe Latte</option>
    <option>Vanilla Latte</option>
  </optgroup>
  <optgroup label="Smoothie">
    <option>Plain</option>
    <option>Strawberry</option>
    <option>Banana</option>
    <option>Mango</option>
  </optgroup>
</select>
~~~

~~~CSS
select { display: inline-block; }
datalist { display: none; }
optgroup, option { display: block; }
~~~

<br>

#### \<select>
<hr>

옵션을 선택하는 메뉴.

|속성|의미|값|기본값|
|:--:|:--:|:-:|:---:|
|autocomplete|사용자가 이전에 입력한 값으로 자동 완성 기능을 사용할 것인지 여부|`on`, `off`	|`on`|	
|disabled|선택 메뉴를 비활성화|불린(Boolean)||	
|form|선택 메뉴가 속할 하나 이상의 `<form>`의 `id` 속성 값|||		
|multiple|다중 선택 여부|불린(Boolean)||	
|name|선택 메뉴의 이름|||		
|size|한 번에 볼 수 있는 행의 개수|숫자(Number)|`0`(`1`과 같음)|

<br>

#### \<datalist>
<hr>

`<input>`에 미리 정의된 옵션을 지정하여 자동완성(Autocomplete) 기능을 제공하는 데 사용.

- `<input>`의 list 속성 바인딩.
- `<option>`을 포함하여 정의된 옵션을 지정

~~~HTML
<input type="text" list="fruits">

<datalist id="fruits">
  <option>Apple</option>
  <option>Orange</option>
  <option>Banana</option>
  <option>Mango</option>
  <option>Fineapple</option>
</datalist>
~~~

<br>

#### \<optgroup>
<hr>

`<option>`을 그룹화.

|속성|의미|값|
|:--:|:--:|:-:|
|label|(필수)옵션 그룹의 이름||
|disabled|옵션 그룹을 비활성화|불린(Boolean)|

<br>

#### \<option>
<hr>

선택 메뉴 (`<select>`)나 자동완성(`<datalist>`)에서 사용될 옵션.

- 선택적 빈(Empty) 태그로 사용 가능.

|속성|의미|값|특징|
|:--:|:--:|:-:|:--:|
|disabled|옵션 그룹을 비활성화|불린(Boolean)||
|label|표시될 옵션의 제목||생략되면 포함된 텍스트를 표시|
|selected|옵션이 선택되었음을 표시|불린(Boolean)||	
|value|양식으로 제출될 값||생략되면 포함된 텍스트를 값으로 사용|

<br>

### \<progress>
<hr>

작업의 완료 진행률을 표시.

|속성|의미|값|특징|
|:--:|:--:|:-:|:--:|
|max|작업의 총량|숫자(Number)||	
|value|작업의 진행량|숫자(Number)|`max` 속성을 생략할 경우 `0`~`1` 사이의 숫자여야 함|  

~~~HTML
<progress value="70" max="100">70 %</progress>
~~~

~~~CSS
progress { display: inline-block; }
~~~

<br>

## 전역 속성(Global Attributes)

모든 HTML 요소에서 공통적으로 사용 가능한 속성.

<br>

### class
<hr>

공백으로 구분된 요소의 별칭을 지정. <br>
CSS 혹은 JavaScript의 요소 선택기(CSS 선택자나 GetElementsByClassName, QuerySelectorAll 같은)를 통해서 요소를 선택하거나 접근.

<br>

### id
<hr>

문서에서 고유한 식별자(idenifier, ID)를 정의. <br>
CSS 혹은 JavaScript의 요소 선택기(CSS 선택자나 GetElementsByClassName, QuerySelectorAll 같은)를 통해서 요소를 선택하거나 접근.

<br>

### style
<hr>

요소에 적용할 CSS를 선언.

<br>

### title
<hr>

요소의 정보(설명)을 지정.

<br>

### lang
<hr>

요소의 언어(ISO 639-1)을 지정.

~~~HTML
<p lang="en">This paragraph is English</p>
<p lang="ko">이 단락은 한글입니다.</p>
<p lang="fr">Ce paragraphe est défini en français.</p>
~~~

<br>

### data-*
<hr>

사용자 정의 데이터 속성을 지정.
HTML에 JavaScript에서 이용할 수 있는 데이터(정보)를 지정하는 용도로 사용.

~~~HTML
<!-- data-custom-data-attributes -->
<div id="me" data-my-name="Heropy" data-my-age="851">Heropy</div>
~~~

~~~JAVASCRIPT
// dataset.customDataAttributes
const $me = document.getElementById('me');
console.log($me.dataset.myName); // "Heropy"
console.log($me.dataset.myAge // "851"
~~~

<br>

### draggable
<hr>

요소가 Drag and Drop API를 사용 가능한지 여부를 지정.

~~~HTML
<div draggable="true">The element to drag.</div>
~~~

<br>

### hidden
<hr>

요소를 숨김.

~~~HTML
<form id="hidden-form" action="/form-action" hidden>
  <!-- 숨겨진 양식들.. -->
</form>
<button form="hidden-form" type="submit">전송</button>
~~~