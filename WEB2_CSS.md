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
<1_revesed2.html 파일>
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