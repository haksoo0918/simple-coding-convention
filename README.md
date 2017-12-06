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
- 속성값을 따옴표로 감싸야 하는 경우에만 작은따옴표`' '`를 사용하여 감싼다.
```css
font-family: 'dotum';
```
- 속성은 한줄에 한줄씩 처리한다.
- 되도록 class 셀렉터를 사용한다.
- 주석기호와 내용사이에는 공백을 사용하여 뛰운다.
- 추가 또는 수정한 부분은 날짜와 수정내용, 작성자 등을 간략하게 기입한다.
```css
/* li width 값 수정 - 20150511 haksoo */
```

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
