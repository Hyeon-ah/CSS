# WEB2 - CSS
## 1. CSS 등장 이전의 상황
### 1.1 HTML이란
	+  정보를 표현하기 위해 고안된 언어
### 1.2 디자인 기술 2가지
	+ 쉬운 방법: HTML 문법에 태그를 추가하는 것(ex.font tag)
	+ 어렵지만 근본적인 해결책: CSS
<해볼 것>
- HTML 문법에 태그 추가폰트 컬러 설정
```
<font color="red"></font>
```


## 2. CSS의 등장
### 2.1 HTML 문법으로 "지금부터 CSS 문법을 인식해"라고 말해줘야 함 
```
<style>
 a {
 	color:red;
 }
</style>
```
###2.2 CSS 언어란?
	+ HTML이 정보에 전념하게 하도록 HTML로부터 디자인 기능을 뺏어온 
	+ 훨씰 더 효율적

# 3. 혁명적 변화
- CSS를 웹페이지에 삽입
- 선택자와 속성이라는 것을 학습

3.1.CSS를 웹페이지에 삽입하는 두 가지 방법
- `<style></style>` 태그 쓰는거
- `style =` 속성을 쓰는 것
	+ <선택자, 효과, 속성 예시>
		+ `a {}`: 선택자(selector)
		+ `color:black`: 효과(decoration), 하나의 선택자 안에 여러개의 효과 사용 가능, 세미콜론(;)사용해야 함.
		+ `<li><a href="2.html" style="color:red">CSS</a></li>`에서 `style="color:red"`: style이라는 속성

# 4. CSS 속성을 스스로 알아내는 방법
- ex
	+ `css text size property` 검색
	+ `css text center property` 검색



# 5. CSS 선택자를 스스로 알아내는 방법
<1_revised2.html 파일>
- class: 하나로 묶는다 -> `.`으로 표현
- class라는 속성의 값은 여러개가 들어올 수 있고 띄어쓰기로 구분, 
하나의 태그에는 여러개의 속성들어올 수 있고, 여러개의 선택자를 통해 하나의 태그를 공동으로 들어갈 수 있다.
- 근데 이건 좋은 방법이 아님 --> 보다 가까이에 있는 명령이 더 큰 영향력을 갖는다.
- 그래서 더 높은 선택자를 사용해야 함 --> `id`
- id선택자(id=)와 class선택자(.saw)가 붙으면 id선택자(id=)가 이긴다!!
- class선택자(.saw)와 tag선택자(a {} )가 붙으면 class 선택자가 이긴다.
- **즉, id선택자(id=) > class선택자(.saw) >  tag선택자(a {} )**
	+ 좀 더 구체적인 것이 포괄적인것보다 우선순위 높임.
	+ class는 마지막에 나오는 것이 가장 큰 영향력임
	+ id 값은 단 한번만 등장해야 함!!
- https://www.w3schools.com/cssref/css_selectors.asp

# 6. 박스 모델
## 6.1 `<h1>`과 `<a href:"">`태그의 기본값
- `<h1></h1>`: block level element
- `<a href:"">`: inline level element
- 하지만 기본값을 css를 통해 언제든 변경 가능
	+ `display:inline;` 또는 `display:block;`을 통해
## 6.2 박스 모델 써먹기
- 2_1.html 참고
- border, border-right, solid, margin, padding 등 

# 7. 그리드
## 7.1 그리드 기본 사용법
- grid는 최신기술, https://caniuse.com/에서 기술사용가능여부 확인하기
- 무색무취의 태그1:  `<div>`, `</div>`
	+ 아무런 의미가 없고 디자인의 용도로만 쓰는 태그
	+ block level element-> 화면 전체를 씀
- 무색무취의 태그2:  `<span>`, `</span>
	+ inline level element
- 두 태그를 나란히 배치하고 싶거나, 어떻게 배치하고 싶다면 그것을 감싸는 부모 태그가 필요 <br>
ex) `<div id="grid">`
- 화면 전체를 쓰게 자동으로 조절되는 단위: fr<br>
ex)개수대로 `grid-template-columns: 150px  1fr 50px;`라고 하면 3개중 처음과 마지막은 크기를 유지하되, 두 번째 div는 남은 화면 전체를 쓴다.

## 7.2 그리드 활용하기
- 하나의 태그로 묶어주고 묶을 그 태그에 부모를 또 배정해줄 수 있음.
- style을 할때 id를 #으로 지정해주면 더 확실하게 할 수 있음.
- 페이지의 `검사`기능을 이용해 여백 조정하는 것 연습하기
	+ `padding-left`가 있지만, `padding: Apx Bpx Cpx Dpx`로 순서대로 상-우-하-좌 설정가능함.
	+ 박스모델과 관련됨-> https://www.zerocho.com/category/CSS/post/582ddf81d4416a001860e75d

# 8. 반응형 디자인
## 8.1 반응형 디자인(Responsive web)과 미디어 쿼리 소개
- 반응형 디자인: 화면의 크기에 따라서 웹페이지의 각 요소들이 반응해서 최적회된 모양으로 바뀌게 하는 것
- 미디어쿼리(mediaquery)
```
screen width > 800px #(설명을 위한 태그임)800px보다 화면이 크다면
@media(min-width:800px) #화면의 크기가 최소 800px
	div{          # 이 태그 동작
	display:none; 
	}
```
# 9. CSS 코드의 재사용
- css 파일로 따로 저장해 사용한다면 중복을 제거할 수 있고, 트래픽 사용료를 덜 내서 경제적인 효과를 볼 수 있다. 
- css파일을 본 컴퓨터에 캐싱(저장하다)해서 네트워크를 쓰지 않아 속도도 높일 수 있다.

