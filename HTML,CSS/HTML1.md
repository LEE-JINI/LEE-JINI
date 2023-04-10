
<br><br>

#1  
HTML 

<br>


**html 태그의 특징**  
```
<html></html> : 시작태그와 종료 태그가 모두 있는 경우  
<br> : 시작 태그만 있는 경우  
- 태그와 속성은 대소문자 구분 없음  
- 속성 값에 불필요한 공백 문자, html5 표준에 어긋남  
```
<br>

**html 태그**  
글자태그 h1~h6 , p , br, hr, a, b, i, small, sub, ins, del  
목록태그 ul/ol, li  
테이블태그 tabel, tr, th, td  
미디어태그 img , audio, video  

<br>


**글자태그**
```
<p> 태그 : 단락 나누기  
<hr> 태그 : 수평선 긋기  
<br> 태그 : 줄바꿈  
<pre> 태그  : 개발자 포맷 그대로 출력  
<span> 태그 : 한 부분만 스타일 적용  
```

<br>

예약어, 키보드로 입력이 어려운 기호들 > 엔터티, 코드값 사용  

```
< : &lt;
> : &gt;
```
<img src="/Img/H1_엔터티.png" width="700px">


<br>

**블록태그**
  - 항상 새 라인에서 시작하여 출력
  - 양 옆에 다른 콘테트a를 배치하지 않고 한 라인 독점 사용
  - div, p, h1, ul 등..

<br>

**인라인 태그**
  - 블록 속에 삽입되어 블록의 일부로 출력
  - span 등..

<br>

**메타 데이터** : 데이터를 설명하는 데이터  
ex) 사진 : 사진찍은 장소, 시간 등..

<br><br>

**html 메타 데이터를 담기 위한 태그**  
```
<base>, <link>, <script>, <style>, <title>, <meta>  
```

<br>


**base 태그** : 기본 url 과 페이지 출력될 윈도우 지정  

```html
<a href="http://www.mysite.com/score/math.html">수학</a>
<a href="http://www.mysite.com/score/science.html">과학</a>
```
```html
<head>
	<base href="http://www.mysite.com/score/">
</head>
<a href="math.html">수학</a>
<a href="science.html">과학</a>  // 로 변경 가능 
```
 
<br>

**link 태그** : 외부 자원 연결에 사용
```
<link type="text/css" rel="stylesheet" href="mystyle.css">  
```

<br>

**meta 태그** : 다양한 메타 데이터 표현  
웹 페이지의 저작자, 인코딩 방식, 내용 등...
```html
<meta name="author" content="황기태">  
// 웹 페이지의 저작자가 황기태임을 표기  
<meta name="keywords" content="컴퓨터, 소프트웨어, 스마트폰">  
// 웹 페이지의 키워드 ( 검색엔진에 의해 검색됨 )  
<meta charset=“utf-8”>  
// 웹 페이지에 사용하는 문자 코드 지정  
```

<br><br>


**이미지 삽입**  
img 태그의 속성 
src = "이미지 파일의 url"  
alt = "이미지 없거나 손상시 대체되는 문자열"  
width, height = "가로 세로 설정"

<br>

../___.jpg ( 상위폴더 )  
___.jpg ( 현폴더 )  
media/___.jpg ( 하위 폴더 )  

<br><br>


**리스트**  
  1. 순서 있는 리스트 ol  
  2. 순서 없는 리스트 ul  
  3. 정의 리스트 di  
     - dt : 용어  
     - dd : 설명  

<br>

속성 type, start ...  
tyep : 마커 종류 , 1,a,A,I,i  
start : 마커의 시작 값  


<br><br>


**표 태그**  
```
<table> : 표 컨테이너  
<caption> : 표 제목, 반드시 첫 번째로 삽입   
<thead> : 헤딩 셀 그룹  
<tfoot> : 바닥 셀 그룹  
<tbody> : 데이터 셀 그룹  
<th> : 열 제목 (헤딩) 셀  
<tr><td> ~ <td> </tr> : 행  

<tr> : 행  
<td> : 행의 값, ( 열 )  

<td> : 데이터 셀  
```
<br>

**표 예제**

<table border="1"> 
	<caption>1학기 성적</caption>
	<thead>
		<tr><th>이름</th><th>HTML</th><th>CSS</th></tr>
	</thead>
	<tfoot>
		<tr><th>합</th><th>225</th><th>230</th></tr>
	</tfoot>
	<tbody>
		<tr><td>황기태</td><td>80</td><td>70</td></tr>
		<tr><td>이재문</td><td>95</td><td>99</td></tr>
		<tr><td>이병은</td><td>40</td><td>61</td></tr>
	</tbody>
</table> 

```html
<table border="1"> 
	<caption>1학기 성적</caption>
	<thead>
		<tr><th>이름</th><th>HTML</th><th>CSS</th></tr>
	</thead>
	<tfoot>
		<tr><th>합</th><th>225</th><th>230</th></tr>
	</tfoot>
	<tbody>
		<tr><td>황기태</td><td>80</td><td>70</td></tr>
		<tr><td>이재문</td><td>95</td><td>99</td></tr>
		<tr><td>이병은</td><td>40</td><td>61</td></tr>
	</tbody>
</table> 
```
셀 병합 속성 : colspan 가로 병합, rowspan 세로 병합 

<img src="/Img/H1_테이블%20속성.png.png" width="700px">
<img src="/Img/H1_테이블%20태그.png엔터티.png" width="700px">

<br><br>

**a 태그의 속성**  
href : 이동할 html 페이지 url 또는 html 페이지 내 앵커 이름   
target : 링크에 연결된 html 페이지가 출력될 윈도우 이름 지정  
  - _blank : 새 윈도우에서 열기
  - _self : 현재 윈도우에서 열기
  - _parent : 부모 윈도우에서 열기
  - _top : 브라우저 윈도우 에서 열기 ( 최상위 브라우저 윈도우)

<img src="/Img/H1_윈도우%20정리.png.png" width="700px">

<br>

target 속성 사용 예  
링크 클릭시 frame1 이름의 프레임에 http://www.w3c.org 출력  
```html
<iframe src="http://www.w3c.org" name="frame1"></iframe>
....
<a href="http://www.w3c.org" target="frame1">W3C</a>

링크 클릭시 새 윈도우(탭)에 W3C 사이트 출력
<a href="http://www.w3c.org" target="_blank">W3C</a>
```

**1. 절대경로**  
http ://naver.com - 네이버의 메인 페이지  
/animal.jpg - 현재 웹 사이트 최상위 위치(root)의 animal.jpg 파일  
**2. 상대경로**  
animal.jpg - 현재 폴더의 animal.jpg  
image/animal.jpg – 현재 폴더 하위에 있는 image 폴더에서 읽어옴  
../animal.jpg - 웹 페이지가 있는 폴더의 상위 폴더에 있는 파일  
../kim/animal.jpg  - 상위 폴더에서 kim 폴더를 찾아 들어가 읽어옴  
**3. 아이디 경로**  
 #name - id 속성이 name인 태그의 위치로 이동  

<br><br>

**앵커란?**  
html 페이지 내의 특정 위치  
```html
<a id="앵커이름">서론</a>  
<a href=“#앵커이름”>서론으로 가기</a>  
서론으로 가기 누르면 서론으로 이동함.
```

<br>

**앵커 예제**

<ul>
	<li><a href="#love">Love me tender</a>
	<li><a href="#can">Can't help falling in love</a>
	<li><a href="#it">It's now or never</a>
</ul>
<h3 id="love">Love me tender</h3>
	Love me tender, Love me sweet, Never let me go.<br>
	You have made my life complete, <br>
	And I love you so.<br>
	Love me tender, Love me true, <br>
	All my dreams fulfilled.<br>
	For my darling I love you, And I always will.<br>
<h3 id="can">Can't help falling in love</h3>
	Love me tender, Love me sweet, Never let me go.<br>
	You have made my life complete, And I love you so.<br>
	Love me tender, Love me true, All my dreams fulfilled.<br>
	For my darling I love you, And I always will.<br>
<h3 id="it">It''s now or never</h3>
	It's now or never, Come hold me tight<br>
	Kiss me my darling, Be mine tonight<br>
	Tomorrow will be too late,<br>
	It's now or never. My love won't wait.<br>

```html
<ul>
	<li><a href="#love">Love me tender</a>
	<li><a href="#can">Can't help falling in love</a>
	<li><a href="#it">It's now or never</a>
</ul>
<h3 id="love">Love me tender</h3>
	Love me tender, Love me sweet, Never let me go.<br>
	You have made my life complete, <br>
	And I love you so.<br>
	Love me tender, Love me true, <br>
	All my dreams fulfilled.<br>
	For my darling I love you, And I always will.<br>
<h3 id="can">Can't help falling in love</h3>
	Love me tender, Love me sweet, Never let me go.<br>
	You have made my life complete, And I love you so.<br>
	Love me tender, Love me true, All my dreams fulfilled.<br>
	For my darling I love you, And I always will.<br>
<h3 id="it">It''s now or never</h3>
	It's now or never, Come hold me tight<br>
	Kiss me my darling, Be mine tonight<br>
	Tomorrow will be too late,<br>
	It's now or never. My love won't wait.<br>
```

<br><br>

**하이퍼링크란?**  
다른 html 페이지의 연결, 텍스트나 이미지로 작성  

a 태그 사용해서 다운로드 하기  
a 태그 속성 입력 위치에 download 삽입  

<br><br>

**인라인 프레임**  
html 내에 html 페이지 삽입  
<iframe> 속성  
src ="url 주소"  
srcdoc = "html 태그로 작성된 텍스트로서 출력될 내용"  
name = "프레임 윈도우 이름, 다른 웹 페이지에서 target 속성값으로 사용함"  

```html
<iframe src="iframe1.html" width="200" height="150"></iframe>
<iframe src="iframe2.html" width="200" height="100"></iframe>

srcdoc="<html><body>hello</body></html>"
- iframe 안에 코드로 생성된 hello 출력됨
```

<br><br>

**미디어삽입**  
html5 표준 브라우저는 플러그인 없이 재생  

**video 태그** 속성  
src : 비디오 파일의 url  
width, heigth : 가로세로 설정  
controls : 재생, 재생시간, 중단, 음소거 등 버튼 출력  
autoplay : 즉시재생  
loop : 반복 재생  
muted : 오디오 끌 때  
<br>
비디오 소스 별도 지정 방법  
```
<source src="url" type="비디오의 마임타입">   
```

<br>

**audio 태그** 속성  
src : 비디오 파일의 url  
controls : 재생, 재생시간, 중단, 음소거 등 버튼 출력  
autoplay : 즉시재생  
loop : 반복 재생  

<br>

비표준 미디어 재생시  
embed, object 태그 사용함  

<br>