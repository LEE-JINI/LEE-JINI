


<br> 
<h1>React</h1>
<br>

#1  
리액트 튜토리얼  
리액트 기초  
리액트와 ES6  
JSX

<br>

1. 리액트 기초

   - 리액트란?  
   UI 개발용 자바스크립트 라이브러리, 페이스북이 개발  
   가장 인기있는 프론트엔드 프레임 워크

   - 리액트 특징  
   컴포넌트 기반 : 컴포넌트는 복잡한 ui 를 설계하기 위해 사용하는 독립적이고 재사용 가능한 부품이다.  
    선언적 문법 : 사용하기 쉽다

   - 구조  
   SPA 구조  
    자바스크립트를 사용하여 화면을 업데이트 한다.

<br>

2. 리액트와 ES6

    구조분해할당  
    스프레드 연산자  
    let, const  
    Array.map  

    기타..


<br>

**Array.map**  
배열의 각각의 아이템에 특정한 작업을 수행한다.  
업데이트된 배열을 리턴한다.  
for 반복문 대신 최신 문법인 map 메소드 많이 사용.

```javascript
const num = [1,2,3];
const result = num.map((item, index) =>{
  return item * 10; // 사용자 정의
}) // map 메소드가 콜백 하나를 전달받음

console.log(result);


const beers = ["Guinness","Heineken","Budwiser"];
const result2 = beers.map((beer, index) =>{ // 인덱스 사용 안 하면 지워도 됨.
  return beer.toUpperCase(); // 모든 문자를 대문자로 바꾸는 문자열 메소드
})
console.log(beers);
console.log(result2);*/
```


<br>

**JSX ( JavaScript Extension )**  
자바 스크립트의 확장 문법  
가상의 엘리먼트를 만들기 위해 사용한다  
선언적 문법  
일반 자바스크립트 객체로 변환된다

1. JSX 기초
2. JSX Fragment
3. JSX에서 변수 출력하기
4. 조건부 렌더링
5. JSX 에서 리스트 출력하기

<br><br>

<h1> Google </h1>

```javascript
// 화면에 보이는 것이 이 화면임.
function App() {
  return <Snippet/> // 우리가 만든 컴포넌트 불러오기
}

export default App;
// 앱 파일에서 import 하려면 export 해주기

// 컴포넌트 생성, 선언적 문법 ( 버츄얼 돔 )
function Snippet(){
  return(
    <form>
      <h1> Google </h1>
      <input
      type="search"
      className="class1 class2"
      // ES6 는 클래스 아니고 클래스 네임
      style={{padding: "0.5rem", width: "20rem"}}
      // 스타일 속성 값으로 객체가 사용되고 있음.
      placeholder="구글 검색"
      autoComplete="off"
      />
    </form>
  )
}

```
<br>
<h1> JSX Fragment </h1>

```javascript
function App() {
  return <Snippet/>
}

function Snippet(){

  // JSX 에서는 트리가 하나의 동일한 엘리먼트로 감싸져야 함.
  // div 또는 Fragment 사용 <></>

  return(
   // <div> 
   <>
      <h1> JSX Fragment </h1>
      <ul>
        <li> list item </li>
        <li> list item </li>
        <li> list item </li>
      </ul>
  </>
    //</div>
  )
} // div 사용 안하면 에러남 . 그래서 이걸 안 쓰려면 ? <> 태그
```
<br>
<h1>JSX 에서 변수 출력하기</h1>

```javascript
function App() {
  return <Snippet/>
}

// JSX 에서 변수 출력하기
function Snippet(){
  let cat = {
    name: "치즈",
    age: 2,
    home: null,
    sound: function(){
      return "야옹"
    }
  }

  // 변수 출력할 때는 중괄호 사용하면 됨.
return (
  <ul>
    <li> 이름: {cat.name}</li>
    <li> 나이: {cat.age}</li>
    <li> 집: {cat.home}</li>
    <li> 소리: {cat.sound()}</li>
  </ul>
)
}
```
<br>
 <h1> 조건부 렌더링 </h1>

```javascript
function App() {
  return <Snippet/>
}

// 조건부 렌더링 if 문 대신해서 사용하는 듯...?
function Snippet(){
  return(
    <>
    <h1> 조건부 렌더링 </h1>

    <h3> && ( 논리연산자 AND ) </h3>
    <p>
      expr1 && expr2 <br/>
      expr1 이 참으로 간주되면 expr2 를 렌더링 한다
    </p>
    <p> {true && "나는 보입니다"} </p>
    <p> {null && "나는 안보입니다"} </p>

    <h3> || ( 논리연산자 OR ) </h3>
    <p>
      expr1 || expr2 <br/>
      표현식1이 참으로 간주되면 표현식1을 렌더링 한다.<br/>
      표현식1이 거짓으로 간주되면 표현식2을 렌더링 한다.
    </p>
    <p> {"나는 보입니다" || "나는 안보입니다"} </p>
    <p> {null || "나는 보입니다"} </p>

    <h3> ? ( 삼항연산자 ) </h3>
    <p>
     조건 ? 표현식1 : 표현식2<br/>
     조건이 참이면 표현식1을 렌더링<br/>
     조건이 거짓이면 표현식2를 렌더링
    </p>
    <p> {true ? "조건이 참입니다" : "조건이 거짓입니다"} </p>
    <p> {false ? "조건이 참입니다" : "조건이 거짓입니다"} </p>

    </>
  )
}
```

<br>
 <h1> 리스트 출력하기 </h1>

```javascript
function Snippet(){

  const beers = [
    {name: "기네스", origin: "아일랜드"},
    {name: "하이네켄", origin: "네덜란드"},
    {name: "버드와이저", origin: "미국"}
  ]

  const beerList = beers.map((beer, index) => (
    <li key={index}>{beer.name}, {beer.origin}</li>
  ))
  // 중간에 소괄호가 나온다는건 엘리먼트가 나온다는 예측 가능.
  // list 출력할 때 map 메소드 사용, 반복문 대신해서 사용하는 것이라..
  // key는 버츄얼 돔을 리턴하는데 필요한 알고리즘, 리스트에는 key 꼭 존재!
  return(
    <>
    <h3> 세계맥주 </h3>
    <ul>
      {beerList}
    </ul>
    </>
  )
}
```

<br>
 <h1> JSX 퀴즈 </h1>

```javascript

function Snippet(){

  const beers = [
    {name: "기네스", origin: "아일랜드", available: false},
    {name: "하이네켄", origin: "네덜란드", available:  true},
    {name: "버드와이저", origin: "미국", available:  true}
  ]

  // 키 값으로 name이나 origin이나 다른거 줘도 상관 없음.
  const beerList = beers.map((beer, index) => (
    <tr key={index}>
      <td>{beer.name}</td>
      <td>{beer.origin}</td>
      <td>{beer.available ? "예" : "아니오"}</td>
    </tr>
  ))

  return(
    <>
    <h3> Beers </h3>

    <table border={1}>
    <thead>
      <tr>
        <th>이름</th>
        <th>원산지</th>
        <th>판매중</th>
      </tr>
    </thead>
    <tbody>
      {beerList}
    </tbody>
    </table>
    </>
  )
}
```
<br>

<h6> 4/24 수업, 5/5 복습 정리</h6>

<br>
