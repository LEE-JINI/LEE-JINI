<br>


#1  
HTML 의 구조  

<br>

element 엘리먼트  
HTML 문서를 개발하기 위한 재료  

트리  
엘리먼트의 부모, 자식 및 형제 관계의 구조  

arribute 속성  
엘리먼트의 기능을 확장한다  

<br>

  <article>
    <h3>세계 맥주</h3>
    <ul>
      <li>
        <a href="https://www.guinness.com" target="_blank">기네스</a>
      </li>
      <li>하이네켄</li>
      <li>버드와이저</li>
    </ul>
  </article>

  ```html
    <article>
    <h3>세계 맥주</h3>
    <ul>
      <li>
        <a href="https://www.guinness.com" target="_blank">기네스</a>
      </li>
      <li>하이네켄</li>
      <li>버드와이저</li>
    </ul>
  </article>
  ```


엘리먼트
- 텍스트처리
h1 - h6 , p , span , a , br


  <h1>h1- h6</h1>
  <p>Heading (제목)</p>
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <h3>Heading 3</h3>
  <h4>Heading 4</h4>
  <h5>Heading 5</h5>
  <h6>Heading 6</h6>

  ```html
  <h1>h1- h6</h1>
  <p>Heading (제목)</p>
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <h3>Heading 3</h3>
  <h4>Heading 4</h4>
  <h5>Heading 5</h5>
  <h6>Heading 6</h6>
  ```

  <h1>p</h1>
  <p>paragraph (문장)</p>
  <p>
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
    Minima impedit delectus reiciendis nisi molestiae. 
    Nostrum iste minima asperiores laboriosam aliquid! 
    Ducimus itaque minus ab, est commodi harum dolore libero sunt?
  </p>

```html
  <h1>p</h1>
  <p>paragraph (문장)</p>
  <p>
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
    Minima impedit delectus reiciendis nisi molestiae. 
    Nostrum iste minima asperiores laboriosam aliquid! 
    Ducimus itaque minus ab, est commodi harum dolore libero sunt?
  </p>
```

 <h1>span</h1>
  <p>텍스트에서 특정 부분을 선택한다</p>
  <p>
    <span style="font-weight: bold">기네스</span> 기네스는 아일랜드의 맥주이다
  </p>

  ```html
   <h1>span</h1>
  <p>텍스트에서 특정 부분을 선택한다</p>
  <p>
    <span style="font-weight: bold">기네스</span> 기네스는 아일랜드의 맥주이다
  </p>
  ```

  <h1>a</h1>
  <p>anchor (링크)</p>
  <a href="https://google.com">Google</a>

  ```html
  <h1>a</h1>
  <p>anchor (링크)</p>
  <a href="https://google.com">Google</a>
  ```

  <h1>br</h1>
  <p>breaking rule (줄바꿈)</p>
  <p>
    기네스는 아일랜드의 맥주이다 <br> 하이네켄은 네덜란드의 맥주이다
  </p>

  ```html
    <h1>br</h1>
  <p>breaking rule (줄바꿈)</p>
  <p>
    기네스는 아일랜드의 맥주이다 <br> 하이네켄은 네덜란드의 맥주이다
  </p>
  ```
  

- 레이아웃
header, nav, article, sectiom, ul li, table, div, hr, foother

  <h1>header</h1>
  <p>웹 페이지의 최상단 부분</p>
  <header>
    <h1>기네스</h1>
    <p>아일랜드 맥주</p>
  </header>


  ```html
    <h1>header</h1>
  <p>웹 페이지의 최상단 부분</p>
  <header>
    <h1>기네스</h1>
    <p>아일랜드 맥주</p>
  </header>
  ```


<h1>nav</h1>
  <p>navigation (메뉴)</p>
  <nav>
    <h3>메뉴</h3>
    <ul>
      <li>
        <a href="#">Home</a>
      </li>
      <li>
        <a href="#">About</a>
      </li>
      <li>
        <a href="#">Blog</a>
      </li>
    </ul>
  </nav>

  ```html
  <h1>nav</h1>
  <p>navigation (메뉴)</p>
  <nav>
    <h3>메뉴</h3>
    <ul>
      <li>
        <a href="#">Home</a>
      </li>
      <li>
        <a href="#">About</a>
      </li>
      <li>
        <a href="#">Blog</a>
      </li>
    </ul>
  </nav>
  ```

    <h1>article</h1>
  <p>기사, 짧은 글 등</p>
  <article>
    <h3>기네스</h3>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. 
      Voluptatum perferendis, fuga minima nobis placeat debitis error illo 
      repellendus odio. Consectetur vero accusamus sit ratione facere nemo 
      tempora, rem cum quidem.
    </p>
  </article>

  ```html
    <h1>article</h1>
  <p>기사, 짧은 글 등</p>
  <article>
    <h3>기네스</h3>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. 
      Voluptatum perferendis, fuga minima nobis placeat debitis error illo 
      repellendus odio. Consectetur vero accusamus sit ratione facere nemo 
      tempora, rem cum quidem.
    </p>
  </article>
  ```


  <h1>section</h1>
  <p>섹션</p>
  <section>
    <h1>세계 맥주</h1>
    <article>
      <h3>기네스</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab praesentium reprehenderit laborum dolores, excepturi, consequatur rem similique eius dicta, ratione quam quod perspiciatis minus? Pariatur nostrum corrupti veritatis aperiam porro!
      </p>
    </article>
    
    <article>
      <h3>하이네켄</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati rerum accusantium, voluptas exercitationem necessitatibus iusto veniam ex commodi totam, debitis itaque minus error inventore? Nam reiciendis assumenda tempora deserunt id.</p>
    </article>
  </section>

  ```html
  <h1>section</h1>
  <p>섹션</p>
  <section>
    <h1>세계 맥주</h1>
    <article>
      <h3>기네스</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab praesentium reprehenderit laborum dolores, excepturi, consequatur rem similique eius dicta, ratione quam quod perspiciatis minus? Pariatur nostrum corrupti veritatis aperiam porro!
      </p>
    </article>
    
    <article>
      <h3>하이네켄</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati rerum accusantium, voluptas exercitationem necessitatibus iusto veniam ex commodi totam, debitis itaque minus error inventore? Nam reiciendis assumenda tempora deserunt id.</p>
    </article>
  </section>
  ```

<h1>ul, li</h1>
  <p>ul: unordered list, li: list item</p>
  <h1>세계맥주</h1>
  <ul>
    <li>기네스</li>
    <li>하이네켄</li>
    <li>버드와이저</li>
  </ul>
  <h1>ol, li</h1>
  <p>ol: ordered list, li: list item</p>
  <ol>
    <li>기네스</li>
    <li>하이네켄</li>
    <li>버드와이저</li>
  </ol>

  ```html
  <h1>ul, li</h1>
  <p>ul: unordered list, li: list item</p>
  <h1>세계맥주</h1>
  <ul>
    <li>기네스</li>
    <li>하이네켄</li>
    <li>버드와이저</li>
  </ul>
  <h1>ol, li</h1>
  <p>ol: ordered list, li: list item</p>
  <ol>
    <li>기네스</li>
    <li>하이네켄</li>
    <li>버드와이저</li>
  </ol>
  ```

 <h1>Table</h1>
  <p>테이블, 표</p>
  <p>tr: table row, td: table data, th: table heading</p>
  <table border="1">
    <thead>
      <tr>
        <th>이름</th>
        <th>원산지</th>
        <th>판매중</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>기네스</td>
        <td>아일랜드</td>
        <td>아니오</td>
      </tr>
      <tr>
        <td>하이네켄</td>
        <td>네덜란드</td>
        <td>예</td>
      </tr>
      <tr>
        <td>버드와이저</td>
        <td>미국</td>
        <td>예</td>
      </tr>
    </tbody>
  </table>

  ```html
   <h1>Table</h1>
  <p>테이블, 표</p>
  <p>tr: table row, td: table data, th: table heading</p>
  <table border="1">
    <thead>
      <tr>
        <th>이름</th>
        <th>원산지</th>
        <th>판매중</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>기네스</td>
        <td>아일랜드</td>
        <td>아니오</td>
      </tr>
      <tr>
        <td>하이네켄</td>
        <td>네덜란드</td>
        <td>예</td>
      </tr>
      <tr>
        <td>버드와이저</td>
        <td>미국</td>
        <td>예</td>
      </tr>
    </tbody>
  </table>
  ```

  <h1>div</h1>
  <p>divide (나눈다)</p>
  <div>
    <h3>기네스</h3>
    <p>기네스는 아일랜드 맥주이다</p>
  </div>
  <div>
    <h3>하이네켄</h3>
    <p>하이네켄은 네덜란드 맥주이다</p>
  </div>

  ```html
  <h1>div</h1>
  <p>divide (나눈다)</p>
  <div>
    <h3>기네스</h3>
    <p>기네스는 아일랜드 맥주이다</p>
  </div>
  <div>
    <h3>하이네켄</h3>
    <p>하이네켄은 네덜란드 맥주이다</p>
  </div>
  ```



  <h1>hr</h1>
  <p>horizontal rule (수평선)</p>
  <hr>
  <h1>세계맥주</h1>
  <ul>
    <li>기네스</li>
    <li>하이네켄</li>
    <li>버드와이저</li>
  </ul>
  <hr>

  ```html
   <h1>hr</h1>
  <p>horizontal rule (수평선)</p>
  <hr>
  <h1>세계맥주</h1>
  <ul>
    <li>기네스</li>
    <li>하이네켄</li>
    <li>버드와이저</li>
  </ul>
  <hr>
  ```

  <h1>footer</h1>
  <p>웹페이지의 최하단 부분</p>
  <footer>
    <p>2023 &copy; 기네스</p>
    <a href="#">개인정보 처리방침</a>
  </footer>


  ```html
   <h1>footer</h1>
  <p>웹페이지의 최하단 부분</p>
  <footer>
    <p>2023 &copy; 기네스</p>
    <a href="#">개인정보 처리방침</a>
  </footer>
  ```


- form ( 양식 )
form, input, button


 <h1>Form (양식)</h1>
  <p>유저로부터 데이터를 입력받는다</p>

  <style>
    label {display: block} 
  </style>

  <form action="">
    <h1>Contact</h1>
    <div>
      <label for="username">성 함</label>
      <input type="text" name="username" id="username">
    </div>
    <div>
      <label for="email">이메일</label>
      <input type="text" id="email" name="email">
    </div>
    <div>
      <label for="message">메시지</label>
      <textarea name="message" id="message" cols="30" rows="10"></textarea>
    </div>
    <div>
      <label>
        <input type="checkbox" name="agree">
        개인정보 처리방침에 동의합니다
      </label>
    </div>
    <button type="submit">전송하기</button>
  </form>

  ```html
   <h1>Form (양식)</h1>
  <p>유저로부터 데이터를 입력받는다</p>

  <style>
    label {display: block} 
  </style>

  <form action="">
    <h1>Contact</h1>
    <div>
      <label for="username">성 함</label>
      <input type="text" name="username" id="username">
    </div>
    <div>
      <label for="email">이메일</label>
      <input type="text" id="email" name="email">
    </div>
    <div>
      <label for="message">메시지</label>
      <textarea name="message" id="message" cols="30" rows="10"></textarea>
    </div>
    <div>
      <label>
        <input type="checkbox" name="agree">
        개인정보 처리방침에 동의합니다
      </label>
    </div>
    <button type="submit">전송하기</button>
  </form>
  ```


- 이미지
  img

  <h1>img</h1>
  <p>이미지를 추가한다</p>
  <p>
    src: 이미지의 주소(source), 
    alt: 이미지 가져오기가 실패했을 때 대신 보여줄 텍스트 (alternative)
  </p>
  <img src="https://image.xportsnews.com/contents/images/upload/article/2022/1206/mb_1670300078707386.jpg" alt="다나카상">


```html
<h1>img</h1>
  <p>이미지를 추가한다</p>
  <p>
    src: 이미지의 주소(source), 
    alt: 이미지 가져오기가 실패했을 때 대신 보여줄 텍스트 (alternative)
  </p>
  <img src="https://image.xportsnews.com/contents/images/upload/article/2022/1206/mb_1670300078707386.jpg" alt="다나카상">

```



  <h1>HTML 엔티티 (Entity)</h1>
  <p>
    1. HTML에서 예약된 문자(HTML 코드로 인식될 수 있는 문자)를 출력하기 위해 사용된다
    <br>
    2. 키보드로 입력하기 어려운 문자를 출력할 때 사용된다 (이모티콘 등)
    <br>
    3. 엔티티 네임과 엔티티 넘버로 구분된다
  </p>
  <h1>엔티티 네임</h1>
  <ul>
    <li>&lt; &gt; </li>
    <li>&amp;</li>
    <li>&quot;</li>
    <li>&copy;</li>
  </ul>
  <h1>엔티티 넘버</h1>
  <ul>
    <li>&#60; &#62;</li>
    <li>&#38;</li>
    <li>&#34;</li>
    <li>&#169;</li>
  </ul>


```html
  <h1>HTML 엔티티 (Entity)</h1>
  <p>
    1. HTML에서 예약된 문자(HTML 코드로 인식될 수 있는 문자)를 출력하기 위해 사용된다
    <br>
    2. 키보드로 입력하기 어려운 문자를 출력할 때 사용된다 (이모티콘 등)
    <br>
    3. 엔티티 네임과 엔티티 넘버로 구분된다
  </p>
  <h1>엔티티 네임</h1>
  <ul>
    <li>&lt; &gt; </li>
    <li>&amp;</li>
    <li>&quot;</li>
    <li>&copy;</li>
  </ul>
  <h1>엔티티 넘버</h1>
  <ul>
    <li>&#60; &#62;</li>
    <li>&#38;</li>
    <li>&#34;</li>
    <li>&#169;</li>
  </ul>

```


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
