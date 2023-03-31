
<br> 
<h1>JavaScript</h1>
<br>

#6  
window 객체  
선택자  
엘리먼트 속성  


1. 메시지 또는 컨펌 등
window.alert()
window.confirm()

```
window.alert('저장되었습니다.'); // 팝업창
window.confirm('제출하시겠습니까?') // 확인 창
```

2. 유저 정보 획득
   유저 정보에 기반한 웹 서비스 개발 시 사용된다
   ex) 위치기반 서비스, 모바일 또는 pc용 웹앱

window.navigator.geolocation
window.navigator.userAgent
console.log(window.navigator.userAgent) // 접속 환경 ( 유저정보 )
console.log(window.navigator.geolocation) // 유저의 위치

3. 브라우저 기록
앱 내의 뒤로가기 버튼 만들기 등에 사용될 수 있다.
window.history
console.log(window.history)

4. 데이터 요청
window.fetch()
window.XMLHttpRequest()
console.log(window.fetch)
console.log(window.XMLHttpRequest)

5. 웹 스토리지
브라우저에 데이터를 저장할 수 있도록 한다
ex) 로그인 토큰, 테마, 장바구니 등등
window.document.cookie
window.localStorage
console.log(window.document.cookie)
console.log( window.localStorage)
// 세션 스토리지, 로컬 스토리지 거의 같은데 세션 스토리지는 탭을 끄면 저장된 것들 다 날아감.

6. 뷰 개발
window.document
window.document.documentElement
window.innerHeight

```html showlines
<script>
console.log(window.document) // html 문서
console.log(window.document.documentElement)
console.log(window.innerHeight) // 뷰(화면)의 높이
</script>
```


<br><br>

**선택자**



<h6>3/27 수업 & 3/29 수업 초반, 3/31 정리 복습</h6>