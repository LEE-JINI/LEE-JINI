---
layout : single
title : "JavaScript #2"
categories: JavaScript
---
<br> 
<h1>JavaScript</h1>
<br>

#2  
조건문  
반복문  
변수와 상수  
함수
 
<br><br>

**타입 연산자**  
1. typeof  
2. instanceof

```JavaScript
var foo = 'bar';
console.log(typeof foo);
```

<br>

**Q. 연산자 문제**  
나이가 13세 이상이고 19세 이하인 사람  
age >= 13 && age <= 19

<br><br>

**조건문**  
1. if 조건문  
2. switch 조건문  
3. ? 삼항연산자 조건문


```JavaScript
1. if 조건문  
	if (조건) {  
		조건이 참일 경우 실행되는 코드  
	}  
```
```JavaScript
var year = 2023;

if ( year === 2023 ){
    console.log('이번년도')
}

if (year === 2022) {
	console.log('작년')
} else if (year === 2023) {
	console.log('올 해')
} else if (year === 2024) {
	console.log('내년')
} else {
	console.log('가까운 년도가 아닙니다')
}
```
<br>

```JavaScript
2. switch 조건문
	엄격동등비교를 수행한다
```

```JavaScript
var year = 2023;

switch(year) {
	case 2022:
		console.log('작년');
		break;
	case 2023:
		console.log('올해')
		break;
	case 2024:
		console.log('내년')
		break;
	default:
		console.log('가까운 년도가 아닙니다')
}
```
<br>

```JavaScript
3. 삼항연산자
	조건 ? 값1 : 값2
	조건이 참이면 값1 리턴
	조건이 거짓이면 값 2 리턴

var year = 2023;
console.log(year === 2023 ? '올해' : '올해가 아닙니다');
```

<br><br>

**문제**  
나이가 성인이면 "성인입니다" 성인이 아니면 "성인이 아닙니다" 를 출력하는 조건문을 만들어 보시오.  

```JavaScript
1. if 조건문
if ( 20 <= age ) {
    console.log("성인입니다")
} else { console.log ("성인이 아닙니다")}

1. 삼항연산자 조건문
console.log( age === 20 ? "성인입니다" : "성인이아닙니다" )
```

<br><br>

**반복문**
1. for 반복문  
2. while 반복문  

```JavaScript
for 반복문

for (var i=0; i<10; i++) {
	console.log(i + '번 실행되었습니다')
}

1에서 10까지의 합을 구한다

var sum = 0;

for (var i=1; i<=10; i++) {
	sum += i; // sum = sum + i
}

console.log(sum);
```
<br>

```JavaScript
while 반복문

let i = 0;

while(i < 10) {

	console.log(i + '번 실행되었습니다');

	i++;
}
```
<br>

**Q. 반복문**  
1/1, 1/2, 1/3, ... 1/10 까지의 합을 구해보시오
```JavaScript
var sum = 0;
for ( var i=1; i<11;i++){
	sum += (1/i);
}
console.log(sum);
```

<br><br>

**변수와 상수**
1. 변수 : var, let
2. 상수 : const
3. 변수/상수의 범위

<br>

```JavaScript
1 var ( 재선언 가능 )

var foo = 'bar'; // 변수 초기화 ( 선언 시 정의 )
console.log(foo) // bar

var foo = 'bar'; // 초기화
foo = 'baz'; // 재정의(재할당)
console.log(foo) // baz

var foo; // 선언
foo = 'bar'; // 정의
console.log(foo) // bar

var foo = 'bar' // 선언
var foo = 'baz' // 재선언
console.log(foo) // baz
```

```JavaScript
2 let (재선언 불가)

let foo = 'bar'
console.log(foo); // bar

let foo = 'bar';
foo = 'baz' // 재정의
console.log(foo) // baz

let foo; // 선언
foo = 'bar' // 정의
console.log(foo) // bar

let foo = 'bar'
let foo = 'baz' // 재선언 불가
```

```JavaScript
3 const (constant) 상수
// 재정의, 재선언 불가

const foo = 'bar'
console.log(foo) // bar

const foo;
foo = 'bar'; // 에러
```
<br><br>

**변수/상수의 범위**  
1. 전역 범위
2. 블록 범위
3. 지역 (함수) 범위

```JavaScript
1 전역 범위
	함수 또는 블록 밖에서 선언된 변수가 갖는 범위

전역(global) 변수
어디에서든지 접근 가능하다

var varInGlobal = true;

{ // 블록
	console.log(varInGlobal) // true
}

function f() {
	console.log(varInGlobal) // true
}

f() // 함수 사용
```

```JavaScript
2 지역 범위(함수 범위)
	함수안에서 선언된 변수가 갖는 범위

    function f() {
	// 함수내에서만 접근 가능
	var varInFunction = true;
}
console.log(varInFunction) // 에러
```
```JavaScript
3 블록 범위
블록안에서 선언된 변수가 갖는 범위

{
	var varInBlock = true;
	let letInBlock = true;
	const constInBlock = true;
}

console.log('var', varInBlock) // true , 블록 밖에서 접근 가능
console.log('let', letInBlock) // 에러 , 블록 밖에서 접근 불가능
console.log('const', constInBlock); // 에러 , 블록 밖에서 접근 불가능
```
<br><br>

**함수**  
정의 : 호출될 때만 실행되는 코드

1. 함수 선언 방법
2. 게양
3. 인자
4. return 
5. 콜백
<br><br>

**함수 선언 방법**
1. 함수 선언식
2. 함수 표현식
3. 화살표 함수


``` JavaScript
함수 선언식
function f() {
	console.log('foo')
}
```
``` JavaScript
함수 표현식
변수에 익명함수를 할당한다
var f = function () {
	console.log('foo')
}
```
``` JavaScript
화살표 함수
var f = () => {
	console.log('foo')
}
```
<br><br>

**게양 (Hoisting);**  
함수의 실행 시점이 함수 정의 시점보다 먼저인 것
``` JavaScript
f() // 함수선언식에만 적용된다

// 함수의 정의가 호출 시점보다 올라간다
function f() {
	console.log('foo');
}

// 익명 함수를 게양하게 되면 오류 발생
f()
let f = function () {
	console.log('foo')
}
```
<br>

**parameter (인자, 매개변수)**
``` JavaScript
function add(x, y) { // x, y는 파라미터
	console.log(x + y);
}

add(1, 2)
```
<br>


**return**
``` JavaScript
function add(x, y) {
	return x + y;
}

var r = add(1, 2);

console.log(r)
```
<br>

**콜백 (callback)**  
다른 함수의 인자가 되는 함수
``` JavaScript

    function f(callback) {
	let r = callback(); // f 함수 내부에서 콜백이 실행되었다
	console.log(r)
}

function cb() { // 콜백
	return 'foo'
}

f(cb);
```
<br>

**콜백 예시**
``` JavaScript
function getTime() {
	let time = new Date().toLocaleTimeString(); // 현재시간
	console.log(time);
}

// setInterval(callback, ms) , JS 제공 글로벌 함수
// ms마다 callback을 실행하는 함수
setInterval(getTime, 1000);

```
<br>

<h6>3/15 수업 , 3/27 정리 복습</h6>