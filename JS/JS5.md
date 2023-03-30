
<br> 
<h1>JavaScript</h1>
<br>

#5  
비동기 작업  
프로미스  
ES6 문법  
정규식  
JSON

<br><br> 


**비동기 작업 (Asynchronous operations)**   
블록킹을 방지하기 위해 사용된다  
블록킹? 특정한 작업이 오래 걸려서 다음 작업이 실행되지 못 하는 상태
ex) 서버에 데이터 요청 등
1. 동기 작업
2. 비동기 작업

<br>

- 동기 작업 (Synchronous operation)  
호출된 순서대로 코드가 실행된다 , 작성하는 코드 대부분이 동기작업
```JavaScript 
function f() {
	console.log('작업 1')
}
f();
console.log('작업 2')
// 작업 1
// 작업 2
```

- 비동기 작업 (Asynchronous operation)  
빠른 것부터 처리된다
```JavaScript
// 서버에 데이터를 요청하고 받는데 1초가 걸린다고 가정
function fetchData(callback){
	var date = {foo : 'bar'};

	// setTimeout(callback, ms): ms 뒤에 callback을 실행한다
	setTimeout(function(){ // 첫번째인자 콜백(익명함수)
		callback(null,data);
	},1000) // 두번째인자 1000

}

// fetchData 호출부분 callback , 익명함수 사용
fetchData(function (error,data){
	if(error){
		return console.error(error);
	}
	console.log('서버에서 받은 데이터:',data);
})
console.log('다음 작업'); // 1초 동안 블로킹이 발생 되니까 이거 먼저 실행되고 fetchData 함수 실행함.
```
<br><br>

**프로미스**  
비동기 작업의 성공 실패 여부와 그 결과를 나타내는 객체  
비동기 작업의 가독성을 향상시키기 위해 사용된다  
1. 프로미스 객체의 구조
2. 실제 예시
3. async/await

<br>

 **프로미스 객체의 구조**
- 프로미스 인스턴스 생성
	생성자 함수에 두개의 매개변수를 가진 콜백을 전달한다  
	첫번째 매개변수(resolve): 비동기 작업이 성공했을 경우 호출한다  
	두번째 매개변수(rejected): 비동기 작업이 실패했을 경우 호출한다
- 프로미스의 상태  
	fullfilled: 작업의 성공  
	rejected: 작업의 실패  
	pending: 작업이 끝나기를 기다리는 상태, 보류 상태
- 프로미스 인스턴스의 메서드  
	Promise.then(): 성공했을 경우 데이터를 다루는 메서드  
	Promise.catch(): 실패했을 경우 에러를 다루는 메서드  
	Promise.finally(): 실패/성공 여부와 상관없이 실행되는 코드를 다루는 메서드

<br>

 ```JavaScript 
 //매개변수 중 첫번째는 성공, 두번째는 실패 시 호출 됨
const promise = new Promise(function(res,rej){ // 두개의 매개변수를 가진 콜백함수
	res({foo:'bar'});
})
console.log(promise); // fullfilled, 성공 

const promise = new Promise(function (res, rej) {
	rej({error:'...'}) // rejected, 실패 ( 에러출력 )
})

const promise = new Promise(function (res, rej) {})
console.log(promise); // pending, 현재 성공이나 실패 둘 다 보류임.
```
 ```JavaScript 
const promise = new Promise(function (res, rej) {
	res({ foo: 'bar' })
})

// 인스턴스 메소드
promise	
	// 데이터를 다루는 부분
	.then(function (value) { 
		console.log(value)
	})
	// 에러 다루는 부분
	.catch(function (error) {
		console.error(error);
	})
	// 실패/성공 여부와 상관없이 실행
	.finally{}
```

<br>

**실제 사용 예시: 서버에 데이터 요청 (비동기)**
```JavaScript
//서버에 데이터를 요청하는 함수, 결과를 프로미스 객체로 리턴한다
function fetchData(){
	const promise = new Promise(function (res,rej){
		res({foo:'bar'});
	})
}

fetchData(){
	.then((data) =>{ // 화살표 익명 함수
		console.log('서버에서 받은 데이터:', data);
	})
	.catch((error) => {
		console.error(error);
	})
}
console.log('다음 작업')
```
<br>

**async / await**  
프로미스가 결과값을 반환할 때까지 기다린다  
프로미스의 **가독성**을 향상시키기 위한 문법
try / catch 에서 에러를 처리한다

 ```JavaScript
function fetchData() {
	const promise = new Promise((res, rej) => {
		res({ foo: 'bar' });
	})
	return promise;
}
f();
console.log('다음 작업')

// 위의 사용예시 코드와 같은 의미의 코드임, 가독성 ( 에러처리 따로 )
async function f(){
	try{
		
		const data = await fetchData();
		// await 프로미스 객체 앞에 붙음. fetchData 객체가 프로미스 리턴하니까.
		console.log('서버에서 받은 데이터:',data);

	} catch (error) {
		console.error(error)
	}
}
```
<br><br>

**ES6 문법 (2015)**  
새로운 문법이 많이 나온 버전
- let, const
- 화살표 함수
- 구조분해할당 v
- 스프레드 연산자 v
- 클래스
- 프로미스
- 심볼
- Array.map()

<br>

**구조분해할당 - 배열**  
간단한 문법을 사용하여 배열의 아이템을 변수에 할당할 수 있다

```JavaScript
var beers = ['기네스', '하이네켄', '버드와이저'];

var beer1 = berrs[0];
var beer2 = beers[1];
var beer3 = beers[2];

console.log(beer1); // 기네스
console.log(beer2); // 하이네켄
console.log(beer3); // 버드와이저

// 구조분해할당
var [beer1, beer2, beer3] = beers;
console.log(beer1); // 기네스
console.log(beer2); // 하이네켄
console.log(beer3); // 버드와이저
```
<br>

**구조분해할당 - 객체**  
간단한 문법으로 객체의 속성을 변수에 할당할 수 있다
```JavaScript
var irishBeer = {name : '기네스', origin:'아일랜드', available: false};

var name = irishBeer.name;
var origin = irishBeer.origin;
var available = irishBeer.available;

console.log('이름:',name);
console.log('원산지:',아일랜드);
console.log('판매중:', available ? '예' : '아니오') 

// 구조분해할당
var { name, origin, available } = irishBeer; // {속성,속성,...}
console.log(name, origin, available);
```
<br>

**구조분해할당 - 매개변수**
```JavaScript
var irishBeer = { name: '기네스', origin: '아일랜드', available: false };

function f(beer){
	console.log(beer);

	var name = beer.name;
	var origin = beer.origin;
	var available = beer.available;
	console.log(name, origin, available);
}
f(irishBeer);

// 구조 분해 할당
function f({name, origin, available}){
	console.log(name,origin,available);
}
f(irishBeer);
```
<br>

**스프레드 연산자 - 배열**  
배열의 아이템을 간단하게 복사할 수 있다  
...복사할 배열

```JavaScript
var beers = ['기네스', '하이네켄'];
var newBeer = '버드와이저'
var updatedBeers = [...beers, newBeer]; // beers 배열 복사
console.log(updatedBeers); // 기네스, 하이네켄, 버드와이저


var europeanBeers = ['기네스', '하이네켄'];
var asianBeers = ['아사히', '클라우드'];
var worldBeers = [...europeanBeers, ...asianBeers];
console.log(worldBeers); // 기네스, 하이네켄, 아사히, 클라우드
```
<br>

**스프레드 연산자 - 객체**  
객체의 속성을 간단하게 복사할 수 있다  
...복사할 객체

```JavaScript
var beer = {
	name : '기네스',
	origin: '아일랜드',
	available: false
}

// 기네스가 재입고 되었다, 기존방식
// beer.available = true;
// console.log(beer);

var copy_beer = { ...beer, available: ture}
console.log(copy_beer);
```
<br>

**ES6 문제**  
1. 구조분해할당  
구조분해할당 문법을 사용해서 각각의 맥주를 변수에 할당해보시오  
```JavaScript
var asianBeers = ['클라우드', '아사히']  

// 원래
var beer1 = asianBeers[0];
var beer2 = asianBeers[2];
ver [beer1, beer2] = asianBeers;
```
2. 스프레드 연산자  
스프레드 연산자를 사용해 치즈의 home을 '삼산동' 으로 업데이트 해보시오
```JavaScript
var cat = {
	name: '치즈',
	age: 1,
	home: null,
	sound: function () {
		return '야옹'
	}
}
var copy_cat = { ...cat, home: '삼산동' }
console.log(updatedCat);
```
<br><br>


**객체와 JSON** 
JSON (JavaScript Object Notation)  
자바스크립트 객체를 저장(쿠키같은) 또는 이동(서버 클라이언트..)하기 위하여 사용되는 텍스트 포멧
1. 객체와 JSON
2. JSON.stringify()
3. JSON.parse()

<br>

**객체와 JSON**
```JavaScript
var o = {foo: 'bar'}
var json = '{"foo": "bar"}' // o 객체를 JSON 포맷으로 표현
console.log(typeof o); // object
console.log(typeof json) // string
```

**JSON.stringify()**  
객체를 JSON 포맷으로 변환한다
```JavaScript
var o = { foo: 'bar' };
var json = JSON.stringify(o);
console.log(json); // JSON 포맷
console.log(typeof json) // string
```
**JSON.parse()**  
JSON 포맷을 객체로 변환한다
```JavaScript
var json = '{ "foo": "bar" }'; // JSON 포맷을 o 객체로 표현
var o = JSON.parse(json);

console.log(o) // 객체
console.log(typeof o) // object
```

<h6>3/22 수업 & 3/27 수업 초반 , 3/30 정리 복습</h6>