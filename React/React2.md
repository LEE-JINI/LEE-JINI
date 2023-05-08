

<br> 
<h1>React</h1>
<br>




#2


컴포넌트 ( Component )

1. 컴포넌트 합성
2. props
3. children props

<br>

# 컴포넌트 합성

```javascript
function Content() {
  return (
    <>
    <h2> 고양이는 액체일까? </h2>

    <img
      src="https://youtu.be/fPKTScaonVU"
      alt=''
      width="100%"

    ></img>

    </>
  )
}

function Comments(){
  return (
<ul>
  <li>유치하게 등수는.. 3빠</li>
  <li> 2빠 </li>
  <li> 1빠 </li>
</ul>

  )
}

function Suggested() {
  return (
    <ul>
      <li></li>
      <li></li>
      <li></li>
    </ul>
  )
}

function Snippet(){
  return (
    <>
    <header>
      <h1> Youtube </h1>
    </header>

    <main>
      <Content />

      <h2> 댓글 </h2>
      <Comments />
    </main>

    <aside>
      <h2> 추천 영상 </h2>
      <Suggested />
    </aside>
    
    </>
  )
}
```

<br>

# props
컴포넌트에 전달되는 데이터 


```javascript
function Snippet(){

// 지역변수
const irishBeer = {
  name: "기네스",
  origin: "아일랜드",
  available: false
}

return (
  <>
  <h1> 맥주 </h1>
  <Beer beer={irishBeer} />
  </>
)
}

// 지역변수에 Beer 컴포넌트가 접근 해야할 때 데이터를 전달함.
// 함수는 매개변수를 받을 수 있듯이 컴포넌트는 props 를 받을 수 있음.
function Beer({beer}){
  return (
    <ul>
      <li> 이름 : {beer.name}</li>
      <li> 원산지 : {beer.origin}</li>
      <li> 판매중 : {beer.available ? "예" : "아니오" }</li>
    </ul>
  )
}
```

<br>

# 컴포넌트 합성 + props 문제 

```javascript
function Snippet(){
  // Snippet이 화면에 렌더링 됨
  // 데이터는 지역변수임
  const DATA = {
    video: {
      id: 'v0',
      title: "고양이는 액체일까?",
      source: "https://youtu.be/fPKTScaonVU"
    },
    commnents: [
      {id: 'c0', content: '1빠'},
      {id: 'c1', content: '2빠'},
      {id: 'c2', content: '3빠'},
    ],
    suggestedVideos: [
      { id: 's0', title: "고양이는.."},
      { id: 's1', title: "고양이는.."},
      { id: 's2', title: "고양이는.."}
    ]
  }

// 이 3개가 컴포넌트 합성 되어있음.
return (
  <>
  <header>
    <h1> Youtube </h1>
  </header>
  <main>
    // 전역변수인 데이터 접근하기 위해 props 사용
    <Video video={DATA.video} />

    <h2> 댓글 </h2>
    <Commnents commnents={DATA.commnents} />

  </main>
  <aside>
    <h2> 추천영상 </h2>
    < SuggestedVideos suggestedVideos = {DATA.suggestedVideos} />
  </aside>
  </>
)
}

// 컴포넌트
function Video ({video}){

  return (
    <>
    <h2>{video.title}</h2>
    <img src={video.source} width="100%"/>
    </>
  )
}

function Commnents ({commnents}){

  let com = commnents.map(coment => (
      <li key={coment.id}>{coment.content}</li>
  ))

  return (
    <ul>
      {com}
    </ul>
  )
}

function SuggestedVideos ({suggestedVideos}) {

  let sugg = suggestedVideos.map((sug, index) => (
    <li key={sug.id}> {sug.title}</li>
  ))

  return(
    <ul>
      {sugg}
    </ul>
  )
}
```
<br><br>

# children props
컴포넌트를 트리 구조로 작성할 수 있다.

```javascript
function Layout({children}){
  return(
    <>

      <h1> Instargram </h1>
      <nav>
        <ul>
          <li> Home </li>
          <li> Post </li>
          <li> Posts </li>
        </ul>
      </nav>

    <main style={{ padding: "1rem 0"}}>
      {children}
    </main>

    <footer>
        <small> 2023 &copy; Instargram</small>
    </footer>
    </>
  )
} // 여기 메인에 들어가는 children 은 Atricle 컴포넌트가 들어감.

function Atricle() {

  return(
    <>
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5K2hHft7N_Wac201KXS7S_WwPSFUWm6Rnrw&usqp=CAU" width="100%" />
    <p>
      <b> Spongeee </b>
       뚱이랑 한 컷
    </p>
    <small> 1일 전</small>
    </>
  )

}

function Snippet(){
  return(
    <Layout>
      <Atricle />
    </Layout>
  ) 
} // Layout Atricle 트리구조
```

<br><br>


# useContext Hook
children 컴포넌트에 데이터를 전달할 수 있다.  
hook 이라는 말이 들어가면 리액트에서 제공하는 함수.  
사용하려면 import { createContext, useContext } from 'react'; 해줘야 함.

```javascript
// children 들이 접근할 수 있는 전역 변수 생성
const AuthContext = createContext();

// 유저 데이터를 관리하는 컴포넌트
function AuthProvider({children}){

  // 유저 데이터, 지역변수라 만약 레이아웃이나 children에서 접근 하려면 useContext Hook 을 사용해서 전달.
  const value = { username: 'bunny'  }


  return (

    // children 을  children 들이 접근할 수 있는 전역 변수안에다가 감쌈. value 는 유저 데이터
    // useContext value 이름도 고정
    <AuthContext.Provider value={value}>
      {children}
    </AuthContext.Provider>
  )

} // 여기의 children 은 Layout , children 이름은 바꾸지 못 함.

function Layout({children}){
  return(
    <>

      <h1> Instargram </h1>
      <nav>
        <ul>
          <li> Home </li>
          <li> Post </li>
          <li> Posts </li>
        </ul>
      </nav>

    <main style={{ padding: "1rem 0"}}>
      {children}
    </main>

    <footer>
        <small> 2023 &copy; Instargram</small>
    </footer>
    </>
  )
} // 여기 메인에 들어가는 children 은 Atricle 컴포넌트가 들어감.

function Atricle() {

  return(
    <>
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5K2hHft7N_Wac201KXS7S_WwPSFUWm6Rnrw&usqp=CAU" width="100%" />
    <p>
      <b> Spongeee </b>
       뚱이랑 한 컷
    </p>
    <small> 1일 전</small>
    </>
  )

}

function Snippet(){
  return(
    <AuthProvider>
    <Layout>
      <Atricle />
    </Layout>
    </AuthProvider>
  ) 
} // 화면에서 달라지는건 없음.

```
<br>

<h6> 4/26 수업, 5/8 복습 정리</h6>

<br>
