<br> 
<h1>HTML</h1>
<br>

#2
HTML 태그
 
<br>

**시맨틱 태그?**  
문서의 구조와 의미를 전달하는 태그
```
<header>, <section>, <article>, <main>, <summary>, <mark>, <time>
```

**header 태그, 머리말**
- 페이지나 섹션의 머리말 표현
- 페이지 제목, 페이지를 소개하는 간단한 설명
  
**nav 태그, 목차**
- 하이퍼링크들을 모아 놓은 특별한 섹션
- 페이지 내 목차를 만드는 용도
  
**section 태그**
- 문서의 장(chapter, section) 혹은 절을 구성하는 역할
- 일반 문서에 여러 장이 있듯이 웹 페이지에 여러 section가능
- 헤딩 태그(h1~h6)를 사용하여 절 혹은 섹션의 주제 기입
  
**article 태그, 절**
- 본문과 연관 있지만, 독립적인 콘텐트를 담는 영역
- 혹은 보조 기사, 블로그 포스트, 댓글 등 기타 독립적인 내용
aside 에 담는 내용이 많은 경우 여러 section  둘 수 있음

**aside 태그 , 노트**
- 본문에서 약간 벗어난 노트나 팁 
- 신문, 잡지에서 주요 기사 옆 관련 기사, 삽입 어구로 표시된 논평 등
- 페이지의 오른쪽이나 왼쪽에 주로 배치
  
**footer 태그, 꼬리말**
- 꼬리말 영역, 주로 저자나 저작권 정보

**권장사항**
- 제목과 소개, audio태그 는 header 태그로 작성
- 본문은 section 으로 묶고 본문 내 각 절이나 영역은 article로 작성
- header, section, article, aside 등에는 헤딩 태그( h1~h6 )를 이용하여 제목을 붙임

<br><br>

**시맨틱 블록 태그**  

figure 태그  
책이나 보고서 등 본문에 삽입하는 사진, 차트, 삽화, 소스 코드 등을 통상적으로 '그림'으로 표현

<br>

details 와 summary 태그  
details : 상세 정보를 담는 시맨틱 블록 태그  
summary : detalis 로 구성되는 블록의 제목 표현  
```html
<details>
   <summary>Question 1</summary>
   <p>웹 개발자가 알아야 하는 언어 3 가지?</p>
</details>
```

<br>

**시맨틱 인라인 태그**
```
<mark> 태그 : 중요한 텍스트임을 표시
<time> 태그 : 텍스트의 내용이 시간임을 표시
<meter> 태그 : 주어진 범위나 %의 데이터 량 표시
<progress> 태그 : 작업의 진행 정도 표시
```
```html
<p>내일 <mark>HTML5 시험</mark><br>
시간은 <time>09:00</time><br>
난이도 <meter value="0.8">80%</meter><br>
자료 업로딩(20%)
	<progress value="2" max="10"></progress><br>
</p>
<br><br>

```

<br><br>

**웹 폼**  
웹 페이지에서 사용자 입력을 받는 폼  
로그인, 등록, 검색, 예약, 쇼핑 등...  
input, textarea, select 등..  

<br>

**폼 태그**  
 form 태그로 둘러 싸는 모양

name 속성 : 폼의 이름 지정  
action 속성 : "폼 데이터를 처리할 응용프로그램 url"
- 폼 데이터를 처리할 웹 서버 응용프로그램의 이름
- submit 버튼이 눌리면 action에 지정된 웹 서버 응용프로그램 실행 요청
- method 속성 : 폼 데이터를 웹 서버로 전송하는 형식, GET / POST
- target 속성 : 응용 프로그램으로부터 받은 데이터를 출력할 윈도우 이름

```html
<input type = "text">
// 한줄짜리 입력창
<input type ="password">
// 암호 입력창 * 로 출력됨
<textarea>
// 여러줄 입력창

<form>
	이름 : <input type="text" value=""><br>
	암호 : <input type="password" value="" maxlength="4"><br>
	자소서 : <textarea cols="20" rows="5">
							이곳에 자기소개서 작성
				  </textarea>
</form>
```
<br>

**datalist 태그** ( 콤보박스 )  
목록 리스트 작성하는 태그  
option 태그로 항목 하나 표현
```html
나라 : <input type="text" list="countries">
			<datalist id="countries">
				<option value="가나">
				<option value="스위스">
				<option value="브라질">
			</datalist>
보고싶은 것 : <input type="text" list="what"> <br>
<datalist id="what">
<option value="산">
</datalist>
```

<br>

**버튼**
```html
<input type=“button|reset|submit|image” value=“버튼의 문자열”>
<button type=“button|reset|submit”>버튼의 문자열</button>
```
type : button|reset|submit|image  
value : 버튼에 출력되는 문자열  
src : type img 인 경우에만 필요, 이미지의 url

<br>

**체크박스, 라디오 버튼**
```html
<input type="checkbox">
<input type=“radio”>
```
value : 폼 요소가 선택된 상태일 때, 웹서버에 전송되는 값  
checked : 초기 선택상태
```html
<form>
	짜장면 <input type="checkbox" value="1">
	짬뽕 <input type="checkbox" value="2" checked>
	탕수육 <input type="checkbox" value="3">
</form>
<!-- 짜장면, 짬뽕, 탕수육 = 캡션, 짬뽕이 초기 값 -->
```


```html
<form>
	<input type="radio" name="china" value="1">
			짜장면<img src="media/jajang.png"><br>
	<input type="radio" name="china" value="2" checked>
			짬뽕<img src="media/jjambbong.png"><br>
	<input type="radio" name="china" value="3">
			탕수육<img src="media/tangsuyuk.png">
</form>
<!-- 같은 name 을 가진 버튼 중 하나만 가능함. -->
```

<br>

select 태그 , 콤보박스  
option 태그로 항목 하나 표현  

select 태그 속성  
- size : 콤보박스 창 크기 ( 최대 보이는 항목 ) , 디폴트 1  
- multiple : 다수 항목 선택
  
option 태그 속성  
- value : 웹 서버에 전송되는 값  
- selected : 초기 선택 값  

<br>

**label 태그**  
캡션과 폼 요소를 묶어서 명료하게 함.
```html
<form name="fo" method="get">
	<label>사용자 ID : <input type="text" size="15" value="">
	</label><br>
	<label for="pass">비밀 번호 : </label>
	<input id="pass" type="password" size="15" value="">
	<input type="submit" value="완료">
</form>
```

라벨로 버튼 + 캡션 가능
```html
<form>
	<label>
		<input type="radio" name="china" value="1">
		짜장면 <img src="media/jajang.png">
	</label><br>
	<label>
		<input type="radio" name="china" value="2" checked>
		짬뽕 <img src="media/jjambbong.png">
	</label><br>
	<label>
		<input type="radio" name="china" value="3">
		탕수육 <img src="media/tangsuyuk.png">
	</label>
```
<br><br>
html 에서의 색 표현  
rgb, #rrggbb 8비트 범위(0~255)로 16진수(0~FF)로 표기

<br>

컬러 다이얼로그
```
<form>
	색 선택
	<input type="color" value="#00BFFF" 
				onchange=
					"document.body.style.color=this.value">
</form>
```
document.body.style.color > 선택한 색을 브라우저의 바탕 글자에 적용하는 자바스크립트 코드


**시간요소**
```html
<input type="month|week|date|time|datetime-local">
<input type="month" value="2016-09">
<input type="week" value="2016-W36">
<input type="date" value="2016-09-01">
<input type="datetime-local"   value="2016-09-01T21:30:10.32">
<input type="time" value="21:30">
```
스핀버튼, 슬라이드 숫자 입력
스핀버튼 : 정교한 값 입력
```html
<input type="number" min="0.0" max="10.0" step= "0.5">
spin 버튼 클릭시 0.0~10.0 사이에서 0.5씩 증감
슬라이드 : 대략적인 값 입력
<input type="range" min="0" max="100" list="temperatures">
<datalist id="temperatures">
	<option value="10" label="Low">
	<option value="50" label="Medium">
	<option value="90" label="High">
</datalist>
```


**placeholder** 입력할 정보 힌트
```html
<input type="email"	placeholder="id@host">
```
<br>

**형식을 가진 텍스트**  
email , url, tel, search  
이 타입들은 placeholder 에 설정해둔 형식대로 입력하지 않으면 오류메시지 출력
