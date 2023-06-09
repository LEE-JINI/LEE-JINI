
<br> 
<h1>JavaScript</h1>
<br>

#3  
함수  
배열  
객체 
<br><br> 

**Q. 인자에 따라서 성인인지 아닌지를 말해주는 함수를 만들어 보세요**

```JavaScript
function Audlt(age) { 
    if ( typeof age !== 'number') { // age 가 넘버가 아니면
		console.log('인자는 숫자만 가능합니다')
		return; // return 아래 코드는 실행되지 않는다
	}
    if ( age >= 18 ){
        console.log("성인 입니다.");
    } else if ("성인이 아닙니다.");
}

//함수 호출
Audlt(15) // 성인이 아닙니다
Audlt(20) // 성인입니다 20: 인자(argument), 함수에 실제 전달하는 값

Audlt('hello') // 이것을 넣고 싶으면 예외처리 추가 또 필요.
```
<br><br>

**배열 (Array)**  
한개 이상의 값을 갖는 데이터 타입

1. 배열에 접근하기
2. 배열 메서드
3. 배열과 반복문


 ```JavaScript   
1 배열에 접근하기

var arr = ['foo', 'bar', 'baz']; // 문자열 배열

console.log(arr[0]) // foo 첫번째 아이템의 index는 0이다
console.log(arr[1]) // bar
console.log(arr[2]) // baz
console.log(arr.length) // item의 갯수: 3


아이템 업데이트하기
arr[2] = 'Baz';
console.log(arr) // 결과 : ['foo', 'bar', 'Baz']


아이템 추가하기
arr[3] = 'duck'
console.log(arr); // ['foo', 'bar', 'Baz', 'duck']

arr[4] = 'duck'
console.log(arr) // ['foo', 'bar', 'Baz', 'duck', 'duck']

// ['foo', 'bar', 'Baz', empty, 'duck'] 를 찍으면?
console.log(arr[3]) // 값이 없으니까 undefined
```
<br><br>

**배열 메서드**  
1. Array.push()  
2. Array.pop()  
3. Array.concat()  
4. Array.sort()  
<br>

Array.push(newItem1, newItem2, ...);
```JavaScript
var arr = ['foo', 'bar'];

arr.push('baz'); // 새로운 아이템을 추가한다

console.log(arr); // foo, bar, baz
```

Array.pop()
```JavaScript
var arr = ['foo', 'bar', 'baz'];

arr.pop(); // 가장 마지막 아이템을 제거한다

console.log(arr);
```

Array1.concat(Array2)  
Array1 뒤에 Array2를 합친다

```JavaScript
var arr1 = ['foo', 'bar'];
var arr2 = ['baz'];

var result = arr1.concat(arr2); // concatenate 

console.log(result) // ['foo', 'bar', 'baz']
```

Array.sort();
```JavaScript
var arr = ['foo', 'bar', 'baz'];

arr.sort(); // 정렬 메서드
// 문자열의 기본값은 알파벳순으로 정렬한다

console.log(arr); // bar, baz, foo
```
join(), toString(), shift(), splice(), slice() ... 등등 다양한 메소드 존재함.
<br><br>

**반복문과 배열**  
	배열에 특정한 작업을 수행할 수 있다


 ```JavaScript
var arr = ['foo', 'bar', 'baz'];

for (var i=0; i<arr.length; i++) {
	console.log(arr[i].toUpperCase()) // 대문자로 변환
}
```
 
필터링 작업
```JavaScript
var arr = ['foo', 'bar', 'baz'];

for (var i=0; i<arr.length; i++) {
	if (arr[i][0] === 'b') { // b로 시작하는 아이템
		console.log(arr[i]) // bar , baz
	}
}

console.log('    foo     ') // 뒷 여백 제거?
console.log('    foo     '.trim()) // 여백 제거
console.log('foo, bar, baz'.split(',')) // [foo, bar, baz]
// split , 를 기준으로 하여 배열로 나눔
```
<br>

**Q. beers 배열에 미국 맥주를 추가해보시오**
```JavaScript
var beers = ['기네스', '하이네켄']
var americanBeer = '버드와이저'

// beers[2] = '버드와이저' 이것도 됨. ( 변수 없이 추가 )
beers.push(americanBeer);
console.log(beers) //  ['기네스', '하이네켄', '버드와이저']

or 

beers[2] = americanBeer;
console.log(beers) //  ['기네스', '하이네켄', '버드와이저']
```
<br>

**Q. 성인의 나이만 출력하는 코드를 작성해보시오, 반복문 사용**
```JavaScript
var ages = [12, 19, 23, 30];
for (var i=0; i<ages.length; i++){
    if (ages[i]>=18){
        console.log(ages[i]);
    }
}
```
<br><br>

**객체 (Object)**  
	데이터와 함수의 집합


 ```JavaScript   
var cat = {
	// 객체의 속성 (property)
	name: '치즈',
	home: null,
	sound: function() { // 메서드 (method)
		return '야옹'
	}
}

console.log(cat) // {name: '치즈', home: null, sound: ƒ}
console.log(cat.name) // name 속성에 접근 , 치즈
console.log(cat['name']) // name 속성에 접근, 치즈
console.log(cat.color); // 존재하지 않는 속성에 접근: undefined
console.log(cat.sound()) // 메서드 호출

// 새로운 속성 추가 시엔 값은 할당 하면 됨.
cat.age = 2; // age 속성 추가

console.log(cat) // {name: '치즈', home: null, age: 2, sound: ƒ}

// 속성 업데이트
cat.home = '삼산동' // home 속성 업데이트
console.log(cat); // {name: '치즈', home: '삼산동', age: 2, sound: ƒ}

// 속성 삭제
delete cat.home; // home 속성 삭제
console.log(cat) // {name: '치즈', age: 2, sound: ƒ}
```
<br>

Q. 네덜란드 맥주의 이름에 접근해보세요
```JavaScript
var beers = [
	{ name: '기네스', origin: '아일랜드' },
	{ name: '하이네켄', origin: '네덜란드' },
	{ name: '버드와이저', origin: '미국' },
]
console.log(beers[1].name); // 하이네켄
```
<br>

<h6>3/17 수업 , 3/27 정리 복습</h6>