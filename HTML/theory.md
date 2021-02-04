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

외부 리소스의 연결 및 현재 문서와의 관계를 명시.
(HTML, CSS, ICON 등 가져오기)

|속성|의미|값|
|:--:|:--:|:-:|
|rel|(필수)현재 문서와 외부 리소스와의 관계(Link Types)|`stylesheet`, `icon`…|
|href|외부 리소스의 URL|URL|
|type|외부 리소스의 MIME 타입|`text/css`, `image/x-icon`…|

<br>

### \<meta />
<hr>

기타 메타 데이터 요소(`<link />`, `<style>` 같은)로 나타낼 수 없는 메타데이터를 나타내기 위해 설정.
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


