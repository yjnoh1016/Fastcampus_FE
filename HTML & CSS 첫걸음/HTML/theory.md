# HTML
<br>

## 정말 쉬운 HTML 문법
<hr>

<br>

### 기본 형태
<hr>

태그는 각자의 의미를 가지고 있으며 다음과 같은 형태를 가진다.

~~~HTML
<TAG></TAG>
<TAG>CONTENT</TAG>
~~~

~~~HTML
<h1>토끼와 거북이</h1>
<p>옛날 옛적에 토끼와 거북이가 살았다 ...</p>

<!-- 다음과 같이 이해할 수 있다. -->
<주제1>토끼와 거북이</주제1>
<문단>옛날 옛적에 토끼와 거북이가 살았다 ...</문단>
~~~

또한 태그는 열리고(open) 닫히는(close) 태그 구조를 가지고 있으며 이는 한 쌍이다.
(시작하고(start) 종료되는(end) 구조라고 부르기도 한다)
이 구조는 태그의 범위를 만들어 준다.

~~~HTML
<h1>토끼와 거북이</h1>

<!-- 다음과 같이 이해할 수 있다. -->
<주제1여기서열림>토끼와 거북이</주제1여기서닫힘>
~~~

입문자가 주의할 점은 닫히는 태그는 태그 이름 앞에 `/` (슬래시)가 붙는다는 것이다.

<br>

### 속성(Attributes)과 값(Value)
<hr>

태그(요소)의 기능을 확장하기 위해 '속성'을 사용할 수 있다.

~~~HTML
<TAG 속성="값"></TAG>
~~~

~~~HTML
<img src="./my_photo.jpg" alt="내 프로필 사진" />
<div class="name">홍길동</div>

<!-- 다음과 같이 이해할 수 있다. -->
<이미지삽입 소스위치="./my_photo.jpg" 대체텍스트="내 프로필 사진" />
<의미없는분할 태그별명="name">홍길동</의미없는분할>
~~~


`<img/>` 는 이미지를 삽입할 때 사용하는 태그이다.
하지만 태그만 사용하면 어떤 이미지를 삽입하는지 알 수 없기 때문에 `src`(source)라는 속성을 사용해서 삽입할 이미지의 경로를 지정한다. 그리고 `alt`(alternative)라는 속성은 이미지를 출력하지 못하는 상황에 이미지 대신 보여질 텍스트를 지정한다.
`<div></div>`는 의미를 가지지 않는 태그로 어떤 내용이든 묶어낼(Wrap) 수 있다.
위에선 `'홍길동'`이라는 텍스트를 묶었으나 그 내용이 무엇을 의미하는지 알 수 없기 때문에 `name`이라는 태그 별명(`class`)을 추가했다.

<br>

### 부모와 자식 요소
<hr>

태그A가 태그B의 콘텐츠로 사용되면, 태그B는 태그A의 부모 요소, 태그A는 태그B의 자식 요소라고 힌다.

~~~HTML
<PARENT>
  <CHILD></CHILD>
</PARENT>
~~~

~~~HTML
<section class="fruits">
  <h1>과일 목록</h1>
  <ul>
    <li>사과</li>
    <li>딸기</li>
    <li>바나나</li>
    <li>오렌지</li>
  </ul>
</section>

<!-- 다음과 같이 이해할 수 있다. -->
<섹션영역 태그별명="fruits">
  <주제1>과일 목록</주제1>
  <순서없는목록>
    <항목>사과</항목>
    <항목>딸기</항목>
    <항목>바나나</항목>
    <항목>오렌지</항목>
  </순서없는목록>
</섹션영역>
~~~

`<section></section>` 안에는(콘텐츠) `<h1></h1>`, `<ul></ul>`, `<li></li>`가 있고 `<ul></ul>` 안에는(콘텐츠) `<li></li>`가 있다.
(이하 닫히는 태그는 생략)
이러한 구조에서 `<section>`는 `<h1>`과 `<ul>`의 부모 요소이다.
또한 `<ul>`은 `<li>`의 부모 요소이다.
반대로 `<h1>`과 `<ul>`은 `<section>`의 자식 요소이다.
또한 `<li>`는 `<ul>`의 자식 요소이다.

여기서 `<ul>`은 `<section>`의 자식 요소이면서 `<li>`의 부모 요소이다.
이처럼 부모와 자식 요소는 상대적인 개념이다.
(조금 더 나아가면 `<section>`은 `<li>`의 조상(상위) 요소, 반대로 `<li>`는 `<section>`의 후손(하위) 요소라고 한다)

우리가 기본적인 가계도를 통해 할아버지, 엄마, 삼촌, 형제 같은 호칭을 정의하듯(혹은 반대로 호칭을 통해 가계도를 이해하듯), HTML의 구조도 위와 같은 개념으로 호칭을 정의하여 추후 선택자(Selector)를 통해 CSS와 JS로 HTML을 다룰 때 중요하게 사용된다.

<br>

### 빈 태그
<hr>

HTML에는 닫히는 개념이 없는 태그들이 있다.
다음과 같은 형태를 가진다.

~~~HTML
<!-- `/`가 없는 빈 태그 -->
<TAG>

<!-- `/`가 있는 빈 태그 -->
<TAG/>
<TAG />
~~~

HTML5에서는 위 2가지 형태를 다 사용할 수 있는데, XHTML 버전이나 린트(Lint) 환경 혹은 프레임워크 세팅에 따라 `/`를 사용하는 것이 필수가 될 수 있다.

어떤 형태를 써야 한다는 갑론을박이 있는데 이는 실제론 중요치 않다. 원하는 형태를 사용하되 혼용하지 말아야 한다.

<br>

## HTML 문서의 범위
<hr>

`index.html` 같은 HTML 파일은 우리는 HTML 문서라고 표현할 수 있다.
HTML 문서의 범위를 나타내는(의미하는) 태그들을 알아보자.

~~~HTML
<!DOCTYPE html>
<html>
  <head>
    문서의 정보
  </head>
  <body>
    문서의 구조
  </body>
</html>
~~~

~~~HTML
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="author" content="홍길동">
    <meta name="description" content="우리 사이트가 최고!">
    <title>내 사이트</title>
    <link rel="stylesheet" href="./css/main.css">
    <script src="./js/main.js"></script>
</head>
<body>
    <section>
      <h1></h1>
      <div>
        <ul>
          <li></li>
          <li></li>
        </ul>
      </div>
    </section>
</body>
</html>
~~~

<br>

### HTML(전체 범위)
<hr>

`<html>`는 HTML 문서의 전체 범위를 지정한다.
웹 브라우저가 해석해야 할 HTML 문서가 어디에서 시작하며, 어디에서 끝나는지 알려주는 역할을 한다.

<br>

### HEAD(정보 범위)
<hr>

웹 브라우저가 해석해야 할 HTML 문서의 정보 범위를 지정한다.
여기서 말하는 정보에는 웹 페이지의 제목, 웹 페이지의 문자 인코딩 방식, 연결할 외부 파일의 위치, 웹 페이지를 구조화하기 위한 기본 세팅 값 같은 것들을 말한다.
다르게는 ‘화면을 구성하기 위한 기본 설정’이라고 표현할 수 있다.

<br>

### DOCTYPE(DTD, 버전 지정)
<hr>

DOCTYPE(DTD, Document Type Definition)은 마크업 언어에서 문서 형식을 정의한다.
이는 웹 브라우저에 우리가 제공할 HTML 문서를 어떤 HTML 버전의 해석 방식으로 구조화하면 되는지를 알려준다.
(HTML은 크게 1, 2, 3, 4, X-, 5 버전이 있다)

현재의 표준 모드는 HTML5 이다.

~~~HTML
<!-- HTML 5 -->
<!DOCTYPE html>

<!-- XHTML 1.0 Transitional -->
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
~~~

<br>

## HTML 문서의 정보
<hr>

`<head></head>` 안에서 사용하는 태그들은 HTML 문서의 정보를 가지고 있다.

<br>

### TITLE(웹 페이지의 제목) 
<hr>

HTML 문서의 제목을 정의한다.
웹 브라우저 각 사이트 탭에서 이름으로 표시된다.

~~~HTML
<head>
  <title>네이버</title>
</head>
~~~

<br>

### META(웹 페이지의 정보)
<hr>

HTML 문서(웹페이지)에 관한 정보(표시 방식, 제작자(소유자), 내용, 키워드 등)를 검색엔진이나 브라우저에 제공한다.
빈(Empty) 태그이다.

~~~HTML
<head>
  <meta charset="UTF-8">
  <meta name="author" content="홍길동">
  <meta name="description" content="우리 사이트가 최고!">
</head>

<!-- 다음과 같이 이해할 수 있다. -->
<문서의정보범위>
  <정보 문자인코딩방식="UTF-8">
  <정보 정보종류="사이트제작자" 정보값="홍길동">
  <정보 정보종류="사이트설명" 정보값="우리 사이트가 최고!">
</문서의정보범위>
~~~

`<meta>`에서 사용할 수 있는 속성은 다음과 같다.
각 태그는 자신이 사용할 수 있는 속성과 값이 정해져 있다.
어떤 속성을 사용할 수 있고, 사용할 수 없는지 구분할 수 있어야 한다.
잘 사용하지 않는 속성도 있기 때문에 당장 모든 속성과 값을 암기할 필요는 없다.
(‘전역(Global) 속성’이라고 해서 어느 태그에서나 사용할 수 있는 속성들도 있지만 지금은 확인할 필요가 없다)

|속성|의미|값|
|:--:|:--:|:--:|
|`charset`|문자인코딩 방식|`UTF-8`, `EUC-KR` 등..|
|`name`|검색엔진 등에 제공하기 위한 정보의 종류(메타 데이터)|`author`, `description`, `keywords`, `viewport` 등..|
|`content`|`name`이나 `http-equiv` 속성의 값을 제공||

<br>

### LINK(CSS 불러오기) 
<hr>

외부 문서를 연결할 때 사용한다.
특히 HTML 외부에서 작성된 CSS 문서(`xxx.css` 파일)를 불러와 연결할 때 사용한다.
빈(Empty) 태그이다.

~~~HTML
<head>
  <link rel="stylesheet" href="./css/main.css">
  <link rel="icon" href="./favicon.png">
</head>

<!-- 다음과 같이 이해할 수 있다. -->
<문서의정보범위>
  <외부문서연결 관계="CSS" 문서경로="./css/main.css">
  <외부문서연결 관계="사이트대표아이콘" 문서경로="./favicon.png">
</문서의정보범위>
~~~

|속성|의미|값|
|:--:|:--:|:--:|
|`rel`|(필수)현재 문서와 외부 문서와의 관계를 지정|`stylesheet`, `icon` 등..|
|`href`|외부 문서의 위치를 지정|경로|

<br>

### STYLE(CSS 작성하기)
<hr>

CSS를 외부 문서에서 작성하여 연결하는 것이 아니고 HTML 문서 내부에 작성할 때 사용한다.

~~~HTML
<style>
  img {
    width: 100px;
    height: 200px;
  }
  p {
    font-size: 20px;
    font-weight: bold;
  }
</style>

<!-- 다음과 같이 이해할 수 있다. -->
<스타일정의>
  <!-- CSS 코드 -->
</스타일정의>
~~~

<br>

### SCRIPT(JS 불러오거나 작성하기)
<hr>

HTML 문서에서 CSS는, 작성된 CSS를 `<link>`로 불러오거나 `<style></style>`안에 작성할 수 있다.
JS는 `<script></script>`로 이 2가지 방식을 모두 사용할 수 있다.

~~~HTML
<!-- 불러오기 -->
<script src="./js/main.js"></script>

<!-- 작성하기 -->
<script>
  function windowOnClickHandler(event) {
    console.log(event);
  }
  window.addEventListener('click', windowOnClickHandler);
</script>

<!-- 다음과 같이 이해할 수 있다. -->

<!-- 불러오기 -->
<자바스크립트 문서경로="./js/main.js"></자바스크립트>

<!-- 작성하기 -->
<자바스크립트>
  <!-- JS 코드 -->
</자바스크립트>
~~~

<br>

## HTML 문서의 구조
<hr>

`<body></body>` 안에서 사용하는 태그들은 HTML 문서의 구조를 나타낸다.

<br>

### DIV(막 쓰는 태그)
<hr>

`<div></div>`의 ‘div’는 ‘division’으로 약자로 ‘분할’을 뜻하고 ‘문서의 부분이나 섹션을 정의’한다.
명확한 의미를 가지지 않기 때문에 정말 많은 경우 단순히 특정 범위를 묶는(wrap) 용도로 사용한다.
보통 이렇게 묶인 부분들에 CSS나 JS를 적용하게 된다.

~~~HTML
<body>
  <div>
    <p></p>
  </div>
  <div>
    <div>
      <h1></h1>
      <p></p>
    </div>
  </div>
</body>

<!-- 다음과 같이 이해할 수 있다. -->
<body>
  <묶음1>
    <p></p>
  </묶음1>
  <묶음2>
    <묶음2-1>
      <h1></h1>
      <p></p>
    </묶음2-1>
  </묶음2>
</body>
~~~

```
DIV는 아무 의미가 없다.
```

<br>

### IMG(이미지 넣는 태그)
<hr>

`<img>`는 HTML에 이미지를 삽입할 때 사용한다.
(웹 페이지에 이미지를 삽입하는 방식은 크게 2가지로, 'HTML에서 삽입(IMG)'과 'CSS에서 삽입(background)'이 있다)

~~~HTML
<body>
  <img src="./kitty.png" alt="냥이">
</body>

<!-- 다음과 같이 이해할 수 있다. -->
<body>
  <이미지 경로="./kitty.png" 대체텍스트="냥이">
</body>
~~~

|속성|의미|값|
|:--:|:--:|:--:|
|`src`|(필수)이미지의 URL|URL|
|`alt`|(필수)이미지의 대체 텍스트(alternate)를 지정|경로|

위 표에서 ‘(필수)’라고 되어 있는 속성들(src, alt)은 `<img>`를 사용할 때 반드시 포함되어야 할 속성(필수 속성, Required Attributes)이다.
만약 `<img src="./kitty.png">`라고 작성하여 `alt` 속성이 누락되었다면 이는 웹 표준에 어긋닌다.

<br>

## 웹 표준 검사하기
<hr>

우리가 작성한 HTML 문서가 표준에 부합하는지 테스트를 해볼 수 있다.
<a href="https://validator.w3.org/#validate_by_upload">
    W3C validator
</a>
에 접속하여 작성한 HTML 문서를 업로드하고 테스트를 시작해보자!
기본적인 표준 여부를 판단할 수 있다.
특히 입문자라면 익숙해질 때까지는 자주 확인하는 것이 좋다.

위에서 `<img src="./kitty.png">`라고 작성했을 때 결과는 에러가 있다고 니온다.
HTML 문서를 작성하면서 지켜야하는 이러한 규칙들이 많이 있다.

```
테스트 통과가 웹 표준/웹 접근성의 준수 여부를 최종적으로 결정하진 않는다. 이 테스트는 사실 기본 문법 검사에 가깝다.
```

또는 사이트(페이지) 주소로 검사할 수도 있다.