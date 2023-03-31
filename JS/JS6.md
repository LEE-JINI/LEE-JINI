
<br> 
<h1>JavaScript</h1>
<br>

#6  
JS 와 HTML  
window 객체  
선택자  
속성과 메소드  
이벤트  
캔버스 API  

<br><br>

**window 객체**  
웹 개발을 위한 도구모음

<br>

1. **메시지 또는 컨펌** 등  
   - window.alert()  
   - window.confirm()  

```
window.alert('저장되었습니다.'); // 팝업창
window.confirm('제출하시겠습니까?') // 확인 창
```
2. **유저 정보 획득**  
유저 정보에 기반한 웹 서비스 개발 시 사용된다  
 ex) 위치기반 서비스, 모바일 또는 pc용 웹앱  
   - window.navigator.geolocation  
   - window.navigator.userAgent  
```html
<script>
console.log(window.navigator.userAgent) // 접속 환경 ( 유저정보 )
console.log(window.navigator.geolocation) // 유저의 위치
</script>
```
3. **브라우저 기록**  
앱 내의 뒤로가기 버튼 만들기 등에 사용될 수 있다.
   - window.history
```html
<script>
console.log(window.history)
</script>
```
4. **데이터 요청**
   - window.fetch()
   - window.XMLHttpRequest()
```html
<script>
console.log(window.fetch)
console.log(window.XMLHttpRequest)
</script>
```
5. **웹 스토리지**  
브라우저에 데이터를 저장할 수 있도록 한다  
ex) 로그인 토큰, 테마, 장바구니 등등
   - window.document.cookie
   - window.localStorage
```html
<script>
console.log(window.document.cookie)
console.log( window.localStorage)
// 세션 스토리지, 로컬 스토리지 거의 같은데 세션 스토리지는 탭을 끄면 저장된 것들 다 날아감.
</script>
```
6. **뷰 개발**
   - window.document
   - window.document.documentElement
   - window.innerHeight

```html
<script>
console.log(window.document) // html 문서
console.log(window.document.documentElement)
console.log(window.innerHeight) // 뷰(화면)의 높이
</script>
```


<br><br>

**선택자**
   - id 선택자
   - class 선택자
   - children 선택자
<br>

**id 선택자**
```html
<ul>
    <li id="foo">foo</li>
    <li>bar</li>
    <li>baz</li>
</ul>

<script>
    var foo = document.getElementById('foo'); // id 선택, window 생략가능
    console.log(foo)
</script>
```
**class 선택자**
```html
<ul>
    <li class="item">foo</li>
    <li class="item">bar</li>
    <li class="item">baz</li>
</ul>

<script>
    var items = document.getElementsByClassName('item'); // 클래스 선택
    console.log(items);
    console.log(items.length) // 3
    console.log(items[1]) // bar
</script>
```
**children 선택자**
```html
<ul id="list">
    <li>foo</li>
    <li>bar</li>
    <li>baz</li>
</ul>

<script>
    var list = document.getElementById('list');
    var items = list.children; // chrldern 선택자
    console.log(itmes); // HtmlColleciton(length)
</script>

```
<br><br>

**엘리먼트 속성**
   - attribute
   - classList
   - createElement
   - innerHtml
<br>

**attribute**  
엘리먼트의 attribute (속성)
```html
<input 
type="text"
id="input"
name="q"
style="padding: 0.5rem; width: 16rem;"
value="구글 검색">

<script>
    var input = document.getElementById('input');
    // attribute에 접근
    console.log(input.type); // text
    console.log(input.style.padding) // 0.5rem
    // CSS 스타일은 접근 못 함.

    // attribute 수정
    input.value="네이버 검색"
</script>
```
<img src="/Img/JS6_1.png">

<br>

**classList**  
엘리먼트의 클래스 리스트를 저장한다.
```html
<style>
    .text-italic {
        font-style: italic;
    }
    .underline {
        text-decoration: underline;
    }
    .font-bold {
        font-weight: bold;
    }
</style>

<ul>
    <li class="font-bold text-italic" id="foo">foo</li>
    <li>bar</li>
    <li>baz</li>
</ul>

<script>
    var foo = document.getElementById('foo');
    console.log(foo.classList); // DOMTokenList(length)
    console.log(foo.classList[0]) // font-bold
    console.log(foo.classList[1]) // text-italic
    console.log(foo.classList.length) // 2 (클래스 개수)

    // 클래스 이름 추가
    foo.classList.add('underline');

    // 클래스 이름 삭제
    foo.classList.remove('font-bold');
</script>

```


**createElement**  
 새로운 엘리먼트를 생성한다
```html
<ul id="list">
    <li>foo</li>
    <li>bar</li>
</ul>

<script>
    var list = document.getElementById('list');
    var li = document.createElement('li'); // li 엘리먼트 생성
    console.log(li);

    // textContent 엘리먼트의 텍스트 컨텐츠를 저장한다.
    li.textContent = 'baz'
    li.appendChild(); // li 엘리먼트를 마지막 칠드런으로 주입함.
    console.log(li); // foo bar baz
</script>

```
**innerHtml**  
문자열의 형태로 tree를 저장한다.
```html
<div id="container">
    <ul>
        <li>foo</li>
        <li>bar</li>
        <li>baz</li>
    </ul>
</div>

<script>
    var container = document.getElementById('container');
    console.log(container.innerHTML); // 위의 ul 트리 저장
    console.log(typeof container.innerHTML); // sting
    
    // innerHTML 업데이트
    container.innerHTML = `
    <ul>
        <li>기네스</li>
        <li>하이네켄</li>
        <li>버드와이저</li>
    </ul>
    `
    console.log(container.innerHTML);
    // 기네스 하이네켄 버드와이저로 업데이트 됨.

</script>
```

<br><br>

**이벤트**  
웹페이지 내에서 유저의 행위  
ex) 클릭, 스크롤, 터치 등
```html
<button id="btn">Button</button>
<script>
    var btn = document.getElementById('btn');
    // addEventListener ( 이벤트이름, 이벤트핸들러 )
    btn.addEventListener('click', () => {
        alert('lol')
    }) // 화살표 함수
</script>
```

<br><br>

**캔버스 API**  
html에서 자바스크립트를 이용해서 그래픽 표현 가능  
    ex) 그래프 그리기, 사진편집, 애니메이션, 웹 게임 등

```html
<style>
    #canvas {
        background-color: black;
    }
</style>
<canvas id="canvas" width="300" height="200"></canvas>

<script>
    var canvas = document.getElementById('canvas');
    var ctx = canvas.getContext('2d') // 펜

    // 얼굴
    ctx.fillStyle = '#0af'; // 채우기 색 (파랑)
    ctx.fillRect(0,100,100,100); // fillRect (x, y, width, height), 색 채워진 직사각형
    
    // 눈
    ctx.fillStyle = '#000';
    ctx.fillRect = (20,120,20,20);
    ctx.fillRect = (60,120,20,20);

    // 입
    ctx.fillStyle = '#000';
    ctx.fillRect = (20,160,10,10);
    ctx.fillRect = (20,170,60,10);
    ctx.fillRect = (70,160,10,10);

</script>
```


<h6>3/27 수업 & 3/29 수업 초반, 3/31 정리 복습</h6>