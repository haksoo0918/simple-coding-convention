# Simple Coding Convention

## 공통

- 인코딩은 UTF-8을 기본으로 한다.
- 들여쓰기는 2공백으로 한다.
- 빈줄은 두줄이상 사용하지 않는다.
- 주석의 성격에 따라 목적을 명시한다.
  - 변수나 함수의 상세설명을 주석의 기본으로 하고 따로 목적을 명시하지 않는다.
  - 기본 기능을 제외하고 임시적으로 내용을 감출때나, 삭제 예정의 목적 등으로 주석을 사용할땐, '임시', '삭제예정'등의 목적을 주석 제일 앞에 명시한다.

## HTML

- 테그나 속성은 특별한 경우를 제외하고 소문자를 사용한다.
- 속성값은 큰따옴표`" "`를 사용하여 감싼다.(data 속성으로 json을 사용할때 등의 특별한 상황은 제외)

```html
<html lang="ko">
```

- `head`와 `body` 바로 안쪽은 들여쓰기 하지 않는다.

```html
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<!-- ... 생략 ... -->
</head>

<body>

<div class="wrapper">
  <div class="container">
    <!-- ... 생략 ... -->
  </div>
</div>

<script>
// ... 생략 ...
</script>
</body>
</html>
```

- 속성중 id나 class를 앞쪽에 배치한다.
- 속성순서 필수속성(img 에 alt 등) > id > class > 기타 속성 > data 속성 > 속성값을 할당하지 않아도 되는 속성(input 에 require, readonly 등)

```html
<input type="submit" name="name" id="name" class="form-control"  title="이름" data-toggle="tooltip" readonly>
```

- 단일테그 끝에 마침표시는 생략한다.(br 등)

```html
<br /> <!-- ( X ) -->
<br>   <!-- ( O ) -->
```

- layout 에서 container 또는 wrap 의 역활을 하는 테그는 마침테그 이후에 주석으로 역활을 명시해준다.

```html
<div class="container">
  .......
</div>
<!-- / .container -->
```

### 참조

- https://github.com/h5bp/html5-boilerplate

---

## CSS

- 공통 스타일은 'common.css'로, 그 외는 화면이나 목적에 맞는 이름을 부여한다.
- 최상단에 파일의 이름이나 작성자, 작성일 등의 설명 주석을 적는다.(자바스크립도 동일)

```css
/**
 * project: 프로젝트명
 * file name: 목적.css
 * author: [이름, ..]
 * modify: [이름, ..]
 * write date: 2000-00-00
 * last modify date: 2000-00-00
 */
```

- 속성값을 따옴표로 감싸야 하는 경우에만 사용하고, 가능한 생략한다. 따옴표도 작은따옴표`' '`를 사용하여 감싼다.

```css
font-family: 'dotum';
```

- 속성은 한줄에 한줄씩 처리한다.
- 되도록 class 셀렉터를 사용한다.
- 기본 네이밍 스타일은 케밥 케이스(kebab-case)를 사용한다.
- 오직 스크립트만을 위한 클래스는 'js-' 접두어를 붙여 사용한다.
- 여럿이 프로젝트를 진행할땐, 추가 또는 수정한 부분은 날짜와 수정내용, 작성자 등을 간략하게 기입한다.

```css
/* li width 값 수정 - 2019-10-15 - haksoo */
```

- CSS 파일 구성은 [SMACSS](http://smacss.com/) 를 따른다.
- 기본 테그 및 유틸 성격의 클래스 스타일을 정의할땐 OOCSS 를 따른다.
- 모듈 기반의 클래스 스타일을 정의할땐 [BEM](http://getbem.com/) 을 따른다.

### 참조

- https://gomdoreepooh.github.io/notes/smacss-bem-oocss
- https://mytory.net/archives/8986
- https://frontdev.tistory.com/entry/CSS-%EB%B0%A9%EB%B2%95%EB%A1%A0Methodologies

---

## JavaScript

- 가능한 strict 모드를 기본으로 사용한다.(ie9 를 맞춰야 하는 경우 생략할수 있다.)

```javascript
'use strict';
```

- 글러벌 변수는 필요한 경우 외에는 사용하지 않는다.
- 함수 선언식 보다 함수 표현식 사용을 권장.

```js
// 함수 선언식
function getData() {
  // ...
}

// 함수 표현식
var getData = function() {
  // ...
};
```

- 제어문이나 함수 등에서 블럭 중괄호는 같은 줄에서 시작한다.
- 네이밍 스타일은 카멜 케이스(camelCase)를 사용한다.
- Vender 등 특별한 경우 외에는 HTML 문서 최하단 `</body>` 위에 정의한다.
- 문자열은 작은 따옴표`' '`를 사용하여 감싼다.(json 등 특별한 상황 제외)

```javascript
var str = 'Hello World';
```

---

## ID & Class Name

- 시멘틱을 최대한 고려한다.
- 스타일이나 기능을 위한 id는 가능한 배제한다.(필요한 경우만 사용)
- 네이밍 스타일은 케밥 케이스(kebab-case)를 사용한다.

## Image File Name

- 약속어를 미리 정하고 사용한다. (예: [NHN Coding Convention](http://nuli.navercorp.com/sharing/fe/coding) - B.1 네이밍 약속어 참조)
- 형태, 목적(의미), 상태 순서로 이름을 정한다.
- 네이밍 스타일은 스네이크 케이스(snake_case)를 사용한다.

## Etc File Name

- 공통으로 사용되는 파일은 'common'이란 이름을 사용한다.
- 서비스 내용을 파일 이름으로 사용한다.
- 네이밍 스타일은 프로젝트별 상황에 맞게 사용하나 기본적으로 케밥 케이스(kebab-case)를 사용한다.
