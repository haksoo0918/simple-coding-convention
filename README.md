# Simple Coding Convention

## 공통
- 인코딩은 UTF-8을 기본으로 한다.
- 들여쓰기는 1탭으로 하고 탭크기는 4로 한다.
- 빈줄은 두줄이상 사용하지 않는다.

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
- 속성순서 id > class > 필수속성(img 에 alt 등) > 기타 속성 > data 속성 > 속성값을 할당하지 않아도 되는 속성(input 에 require 등)
```html
<button id="btn_reg" class="btn btn-primary" type="submit" title="등록" data-toggle="tooltip">등록</button>
```
- 단일테그 끝에 마침표시는 생략한다.(br 등)
- layout 에서 container 또는 wrap 의 역활을 하는 테그는 마침테그 이후에 주석으로 역활을 명시해준다.
```html
<div class="container">
	.......
</div>
<!-- / .container -->
```

## CSS
- 공통 스타일은 'common.css'로, 그 외는 화면파일과 동일한 이름을 부여한다.
- 최상단에 파일의 이름이나 작성자, 작성일 등의 설명 주석을 적는다.
```css
/**
 * [project name] 공통 스타일
 * file name: common.css
 * author: haksoo
 * modify: [other]
 * date: 2000-00-00
 * last modify date: 2000-00-00
 */
```
- 속성값을 따옴표로 감싸야 하는 경우에만 작은따옴표`' '`를 사용하여 감싼다.
```css
font-family: 'dotum';
```
- 속성은 한줄에 한줄씩 처리한다.
- 되도록 class 셀렉터를 사용한다.
- 주석기호와 내용사이에는 공백을 사용하여 뛰운다.
- 되도록이면 추가 또는 수정한 부분은 날짜와 수정내용, 작성자 등을 간략하게 기입한다.
```css
/* li width 값 수정 - 20150511 haksoo */
```

## SCSS
- 아직은 아무생각이 없음.

## JavaScript
- strict 모드를 기본으로 사용한다.
```javascript
'use strict';
```
- Vender 등 특별한 경우 외에는 HTML 문서 최하단 `</body>` 위에 정의한다.
- 문자열은 작은 따옴표`' '`를 사용하여 감싼다.(json 등 특별한 상황을 제외)
```javascript
var str = 'Hello World';
```
- 제어문이나 함수 등에서 중괄호는 같은 줄에서 시작한다.
```javascript
function () {
	// todo
}
```

## ID & Class Name
- ~~언더바`_`를 사용하여 이름을 정한다.~~ 재정의 필요.
- 목적(의미), 세부사항 순서로 이름을 정한다.
```
tab_container
```

## Image File Name
- 약속어를 미리 정하고 사용한다.([NHN Coding Convention](http://nuli.navercorp.com/sharing/fe/coding) 을 참조한다.)
- 형태, 목적(의미), 상태 순서로 이름을 정한다.
```
btn_reg_over.png
```

## Etc File Name
- 공통으로 사용되는 파일은 'common'이란 이름을 사용한다.
- 서비스 내용을 파일 이름으로 사용한다.
