

<br> 
<h1>JavaScript</h1>
<br>

#8  
예제 

<br>


<h1> 뉴스레터 </h1>

<style>
    #form {
        width: 20rem;
    }

    #form_g {
        display: flex;
    }
    input{
        padding: 0.5rem;
        flex-grow: 1;
    }
    .hidden{
        display: none;
    }
</style>


<form id="form">
    <div id="form_g">
        <input type="text" placeholder="lee@naver.com">
        <button type="submit"> 구독하기 </button>
    </div>
</form>
<div id="sub" class="hidden">
    <h1> 구독해 주셔서 감사합니다</h1>
    <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque consequuntur natus repellat iure nihil
        exercitationem ipsum ut autem dolores! Aperiam magnam porro incidunt eveniet dignissimos id. Iusto molestias
        exercitationem illo.</p>
</div>

<script>

    var form = document.getElementById('form');
    var sub = document.getElementById('sub');

    form.addEventListener('submit', (e) => {
        e.preventDefault(); // 폼을 제출하지 않는다
        console.log(e) // 이벤트 객체
        // AJAX 요청 (서버에 데이터 전송)
        form.classList.add('hidden');
        sub.classList.remove('hidden');
    })

</script>


```html
<h1> 뉴스레터 </h1>

<style>
    #form {
        width: 20rem;
    }

    #form_g {
        display: flex;
    }
    input{
        padding: 0.5rem;
        flex-grow: 1;
    }
    .hidden{
        display: none;
    }
</style>


<form id="form">
    <div id="form_g">
        <input type="text" placeholder="lee@naver.com">
        <button type="submit"> 구독하기 </button>
    </div>
</form>
<div id="sub" class="hidden">
    <h1> 구독해 주셔서 감사합니다</h1>
    <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque consequuntur natus repellat iure nihil
        exercitationem ipsum ut autem dolores! Aperiam magnam porro incidunt eveniet dignissimos id. Iusto molestias
        exercitationem illo.</p>
</div>

<script>

    var form = document.getElementById('form');
    var sub = document.getElementById('sub');

    form.addEventListener('submit', (e) => {
        e.preventDefault(); // 폼을 제출하지 않는다
        console.log(e) // 이벤트 객체
        // AJAX 요청 (서버에 데이터 전송)
        form.classList.add('hidden');
        sub.classList.remove('hidden');
    })

</script>

```


<style>
    #list {
        padding: 0;
        margin: 0;
        list-style: none;
    }
    .item {
        padding: 0.5rem;
    }

    #search {
        width: 20rem;
        padding: 0.5rem;
    }

    .hidden {
        display: none;
    }
</style>

<h1> 실시간 검색</h1>
<input id="search" type="text" placeholder="검색">

<ul id="list">
    <li class="item">Guinness</li>
    <li class="item">Heineken</li>
    <li class="item">Budwiser</li>
    <li class="item">Kloud</li>
    <li class="item">Asahi</li>
</ul>

<script>

    var search = document.getElementById('search');

    search.addEventListener('keyup', (e) => {
        // attribute (value)
        var value = e.target.value.toLowerCase(); // search 에 입력된 값
        var items = document.getElementsByClassName('item');
        console.log(value);

        for (var i = 0; i < items.length; i++) {
            var item_con = items[i].textContent.toLowerCase();

            if (item_con.includes(value)) {
                // 해당 아이템을 보이게 한다
                items[i].classList.remove('hidden');
            } else {
                // 해당 아이템을 보이지 않게 한다
                items[i].classList.add('hidden');
            }
        }
    })
</script>

```html
<style>
    #list {
        padding: 0;
        margin: 0;
        list-style: none;
    }
    .item {
        padding: 0.5rem;
    }

    #search {
        width: 20rem;
        padding: 0.5rem;
    }

    .hidden {
        display: none;
    }
</style>

<h1> 실시간 검색</h1>
<input id="search" type="text" placeholder="검색">

<ul id="list">
    <li class="item">Guinness</li>
    <li class="item">Heineken</li>
    <li class="item">Budwiser</li>
    <li class="item">Kloud</li>
    <li class="item">Asahi</li>
</ul>

<script>

    var search = document.getElementById('search');

    search.addEventListener('keyup', (e) => {
        // attribute (value)
        var value = e.target.value.toLowerCase(); // search 에 입력된 값
        var items = document.getElementsByClassName('item');
        console.log(value);

        for (var i = 0; i < items.length; i++) {
            var item_con = items[i].textContent.toLowerCase();

            if (item_con.includes(value)) {
                // 해당 아이템을 보이게 한다
                items[i].classList.remove('hidden');
            } else {
                // 해당 아이템을 보이지 않게 한다
                items[i].classList.add('hidden');
            }
        }
    })
</script>
```
  
```html
    <style>
        .group {
            margin-bottom: 0.5rem;
        }

        label {
            display: block;
        }

        input {
            padding: 0.5rem;
            width: 15rem;
        }

        button {
            padding: 0.5rem;
        }

        .red {
            color: red;
        }

        .hidden {
            display: none;
        }
    </style>


    <h1> Contact Form </h1>

    <form id="form">
        <div class="group">
            <label for="">First name</label>
            <input name="fname" type="text" placeholder="Jin">
            <p id="f_err" class="red hidden"></p>
        </div>

        <div class="group">
            <label for="">Last name</label>
            <input name="lname" type="text" placeholder="Lee">
            <p id="l_err" class="red hidden"></p>
        </div>

        <div class="group">
            <label for="">E-mail</label>
            <input name="email" type="email" placeholder="Lee@naver.com">
            <p id="e_err" class="red hidden"></p>
        </div>

        <button type="submit">submit</button>
    </form>

    <script>

        var form = document.getElementById('form');
        var fnameError = document.getElementById('f_err');
        var lnameError = document.getElementById('l_err');
        var emailError = document.getElementById('e_err')

        form.addEventListener('submit', (e) => {

            e.preventDefault(); // 폼을 제출하지 않는다

            var formData = new FormData(e.target);// 이벤트 객체에서 값을 받아옴
            var fname = formData.get('fname');
            var lname = formData.get('lname');
            var email = formData.get('email');

            // trim(): 문자열의 앞, 뒤 공백을 제거한다
            if (!fname.trim()) { // 공백 제거가 안된다 = 값이 없다, 값이 없으면
                errorHandler('아이디를 입력해주세요', fnameError);
            } else if (fname.length < 3) {
                errorHandler('아이디를 3글자 이상 입력해 주세요', fnameError)
            } else { // 값이 있으면
                errorHandler(null, fnameError)
            }
            // 성 유효성 검사
            if (!lname.trim()) {
                errorHandler('성을 입력하세요', lnameError);
            } else {
                errorHandler(null, lnameError);
            }
            // 이메일 유효성 검사
            if (!email.trim()) {
                errorHandler('이메일은 필수입니다', emailError);
            } else {
                errorHandler(null, emailError)
            }
        })

        function errorHandler(error, container) {
            if (error) {
                container.classList.remove('hidden');
                container.textContent = error;
            } else {
                container.classList.add('hidden');
            }
        }
    </script>
```

 ```html
     <style>
        label {
            display: block;
        }

        input {
            padding: 0.5rem;
            width: 15rem;
        }
        .red {
            color: red;
        }

        .green {
            color: green;
        }
    </style>

    <h1> 유저이름 실시간 유효성 검사 </h1>

    <div>
        <label> username </label>
        <input type="text" id="name">
        <p id="msg"> 유저 이름을 입력하세요 </p>
    </div>

    <script>

        const name = document.getElementById('name');
        const msg = document.getElementById('msg');

        name.addEventListener('keyup', (e) => {
            try {
                var username = e.target.value; // e 타겟으로 입력 값 받아오고
                console.log(username);
                if (!username) { // 유저 이름 없으면 = false 면
                    throw '유저이름은 필수입니다'
                }
                if (username.length < 5) {
                    throw '유저이름이 너무 짧습니다'
                }

                // 정규식 (regular expression): 문자열을 검색하기 위한 패턴을 제공한다
                if (username.match(/[^a-z0-9_]/)) {
                    throw '알파벳 소문자, 숫자 그리고 언더스코어만 사용가능합니다'
                }
                msg.innerHTML = '<span class="green">사용가능한 유저이름입니다</span>'
            } catch (error) {
                msg.innerHTML = `<span class="red">${error}</span>`
            }
        });

    </script>
```

```html
  <style>

header{
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  border-bottom: 1px solid #ddd;
}
.hidden{
  display: none;
}
main{
  margin-top: 4rem;
}
#btn{
  border: none;
  width: 50px;
  height: 50px;
  background-color: gray;
  font-size: 30px;
}
nav{
  backdrop-filter: blur(8px);
} /* 배경 블러처리 */
nav ul{
  margin: 0;
  padding: 0;
} /* top 여백 없는 설정 */
nav li{
  list-style: none;
}
nav a {
      display: block;
      text-align: center;
      padding: 0.5rem;
      text-decoration: none;
      color: #555;
      border-top: 1px solid #ddd;
    }
    nav a:hover {
      color: #000;
    }
</style>

<header>
  <div>
    <button id="btn">&#9776;</button>
  </div>
  <nav id="nav" class="hidden">
    <ul>
      <li> <a href="#"> link </a></li>
      <li> <a href="#"> link </a></li>
      <li> <a href="#"> link </a></li>
    </ul>
  </nav>
</header>

<main>
<h1>TOP</h1>
<p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga ducimus quibusdam reprehenderit quaerat, in ullam a itaque quos numquam explicabo non incidunt, velit rem obcaecati optio harum aperiam ut aliquam?</p>
</main>

<script>

var btn = document.getElementById('btn');
var nav = document.getElementById('nav');


btn.addEventListener('click', (e) => {
  nav.classList.toggle('hidden');
})

 // 범위: window(화면전체)
 window.addEventListener('click', (e) => {
      console.log(e.target); // 이벤트가 발생한 엘리먼트 값 가져오기
      
      // 화면에서 햄버거 버튼이 아닌 곳을 클릭했을 때
      if (e.target !== btn) {
        nav.classList.add('hidden')
      }
    })

</script>
```


```html
  <style>
    body {
      height: 1000px;
      margin: 0;
    } /* margin: 0 을 줘야지 빈공간 없이 딱 붙음 */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      height: 50px;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: transparent;
      transition: background-color 0.5s;
    }
    /* transition 애니메이션 효과 */

    .bg-image {
      background-image: linear-gradient(to right, #0ef, #0af);
      height: 400px;
    }

    .active {
      background-color: #fff;
    }
    /* 활동하면 바뀔 배경 색 */
  </style>

  <header id="header"> Transparent NavBar </header>
  <div class="bg-image"></div>

  <script>

    var header = document.getElementById('header');

    // 윈도우 변경이 있을 때 이벤트를 주는거니까
    window.addEventListener('scroll', (e) => {
      var scrollTop = document.documentElement.scrollTop;
      // 윈도우 document의 documentElement 인 scrollTop의 값을 가져오겠다.
      console.log(scrollTop);

      if(scrollTop>50){ // 스크롤 탑이 50 보다 높으면 ( 스크롤을 내리면 )
         header.classList.add('active')
      } else {
        header.classList.remove('active')
      } 
    }) 
  
  </script>
  ```

  
  ```html
    <style>
    body {
      height: 1000px;
    }

    #header {
      position: fixed;
      top: 0;
      left: 0;
      border-bottom: 1px solid #ddd;
      padding: 1rem;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      transform: top 0.2s;
      background-color: #ddd;
    }

    main {
      margin-top: 75px;
    }

    #header.hidden {
      top: -50px;
    }
  </style>

  <header id="header"> Header </header>
  <main>
    <h1>Switch NavBar</h1>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Esse ad odio doloremque corrupti architecto quam error
      natus illo commodi adipisci deleniti eligendi officiis molestiae eum iste, tenetur, rerum, eius fuga.</p>
  </main>

  <script>
    var header = document.getElementById('header');
    var p_top = 0; // 이전의 스크롤 값

    window.addEventListener('scroll', (e) => {

      // 현재 스크롤 값
      var s_top = document.documentElement.scrollTop;
      console.log(s_top);
      console.log(p_top);


      if ((s_top - p_top) > 0) {
        header.classList.add('hidden');
      } // 스크롤을 내리고 있을 때, 현재 스크롤 - 이전의 스크롤
      else { // 스크롤 올리고 있을 때
        header.classList.remove('hidden');
      }
      p_top = s_top;
    })

  </script>
  ```
  
<h6>3/31 수업 & 4/3 수업, 4/12 정리 복습</h6>