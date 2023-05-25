
<br> 
<h1>JavaScript</h1>
<br>

#4  
<br><br>


클래스 (class)  
객체를 생성하기 위한 템플릿  
1. 클래스 인스턴스
2. static 속성과 static 메서드
3. 미리 정의된 클래스
4. 리터럴 표기법\
<br>


**1 클래스 인스턴스**  
```JavaScript
class Cat {

	// 생성자 함수 : 인스턴스 속성을 설정하기 위해 사용.
	constructor(name, age){
		this.name = name;
		this.age = age;
		// this(Cat 클래스의 속성) 인스턴스에서 매개변수로 받은 name 과 age 를 Cat 클래스 속성에 대입하겠다.
	}

	// 클래스 멤버 ( 속성 )
	home = null;

	// 클래스 멤버 ( 메소드 )
	sound() {
		return '야옹'
	}
}

// Cat 클래스의 인스턴스, 인스턴스 = 클래스의 생성된 객체
const cat = new Cat('치즈', 2);
console.log(cat);
console.log(cat instanceof Cat); // true

// 상속 (코드 재사용)
console.log(cat.home) // null

// 상속
console.log(cat.sound()) // 야옹
```
<br>


**2 static 속성과 static 메서드**  
클래스와 인스턴스와 관련된 유틸리티를 제공한다

```JavaScript
class Cat {

	// 생성자 함수 : 인스턴스 속성을 설정하기 위해 사용.
	constructor(name, age){
		this.name = name;
		this.age = age;
		// this(Cat 클래스의 속성) 인스턴스에서 매개변수로 받은 name 과 age 를 Cat 클래스 속성에 대입하겠다.
	}

	// 클래스 멤버 ( 속성 )
	home = null;

	// 클래스 멤버 ( 메소드 )
	sound() {
		return '야옹'
	}

	static family = '고양이과'

	static isAdult(age){
		if (age <1){
			return '아깽이'
		} else {
			return '고양이'
		}
	}
}

// static 속성과 메서드는 클래스 자체가 호출한다
console.log(Cat.family) // 고양이과
console.log(Cat.isAdult(2)) // 고양이

let c = new Cat('냥',2);
console.log(c); // Cat {home: null, name: '냥', age: 2}
console.log(c.family); // undefined


// JS가 제공하는 Math 클래스와 PI 속성 ( Math 클래스의 static 속성 )
var pi = Math.PI;
console.log(pi); // 3.141592653589793
```
<br>


**3 미리 정의된 클래스**
```
	문자처리: String
	숫자 및 날짜: Number, Math, Date
	인덱스가 있는 콜렉션: Array
	에러: SyntaxError, ReferenceError 기타 에러 등
	기타: Promise, JSON
```
<br>


**4 리터럴 표기법**
```JavaScript
String클래스의 인스턴스
var foo = new String('bar'); // 클래스를 이용
var foo = 'bar' // 리터럴 표기법 (값만 적는다)
console.log(foo.toUpperCase());


Number의 인스턴스
var year = new Number(2023); // 클래스
var year = 2023; // 리터럴 표기


Object의 인스턴스
var o = new Object({ prop1: 'foo', prop2: 'bar' }); // 클래스
var o = { prop1: 'foo', prop2: 'bar' }; // 리터럴 표기
```
<br>

**Q. 다음을 클래스로 정의해보시오.**  
	클래스 이름: Beer  
	인스턴스의 속성: name, origin(원산지)  
	클래스 속성 멤버  
	history: B.C 3000  
	클래스 메서드 멤버  
	recipe(제조법): 보리, 홉, 효모, 물 등  
	static 속성  
	caution(경고): 지나친 음주는 돈이 많이 듭니다  


```JavaScript

class Beer {
	constructor(name , age){
		this.name = name;
		this.age = age;
	}

	history = B.C 3000;// 속성 멤버

	recipe(){ // 메소드 멤버
		return '보리, 홉, 효모, 물 등 ...'
	}
	// static 멤버, 프로그램 실행 시 메모리에 올라가서 모든 인스턴스가 공유함.
	static caution = '지나친 음주는 돈이 많이 듭니다'
}

// Beer의 인스턴스
var irishBeer = new Beer('기네스', '아일랜드');
var dutchBeer = new Beer('하이네켄', '네덜란드');

console.log(irishBeer) // Beer {history: 'B.C 3000', name: '기네스', origin: '아일랜드'}
console.log(dutchBeer) // Beer {history: 'B.C 3000', name: '하이네켄', origin: '네덜란드'}

// 메서드
console.log(irishBeer.recipe()); // 밀, 홉, 효모, 물 등..

// static 속성
console.log(Beer.caution); // 지나친 음주는 돈이 많이 듭니다
```
<br><br>

**에러와 에러처리**  
1. 에러개념
2. 에러처리
3. 에러 종류
4. 커스텀 에러

<br>

**1 에러개념**  
에러는 프로그램의 실행을 중단시킨다  
에러는 처리가 되어야 한다  

```JavaScript
console.log(foo)
// ReferenceError: foo is not defined.

// ReferenceError: name
// foo is not defined: message
// at Object...: stack

// > app crashed (실행 중단)
```
<br>

**2 에러 처리**  
	try/catch
	
```JavaScript
try {
	// 코드...
	console.log(foo);

} catch (error) {
	// 에러 처리
	console.error(error);
}
```
<br>

**3 에러의 종류**
- ReferenceError (참조 에러)
- SyntaxError (문법 에러)
- TypeError(타입 에러)
- RangeError(범위 에러)
- URIError(URI 에러)

<br>

- ReferenceError  
존재하지 않는 변수를 참조할 때 발생한다
```JavaScript
console.log(x) // ReferenceError
```


- SyntaxError  
문법이 잘못되었을 때 발생한다  
컴파일 에러를 발생시킨다  
에러 처리를 할 수 없다  
```JavaScript
console.log(2023)) // SyntaxError: Unexpected token ')'
```


- TypeError
변수 또는 매개변수가 유효한 타입이 아닐 때 발생한다
```JavaScript
setInterval(callback, ms)
setInterval(null, 1000);
TypeError
The 'callback' argument must be of type function. Received null.
```


- RangeError
값이 지정된 범위를 벗어났을 때 발생한다
```JavaScript
var pi = Math.PI;
console.log(pi); // Number 
console.log(pi.toPrecision(200)); // 소수점 200자리까지 제한
// RangeError, toPrecision() argument must be between 1 and 100
```


- URIError  
encodeURI 또는 decodeURI 함수가 유효하지 않은 인자를 전달받았을 때 발생한다
```JavaScript
console.log(decodeURI('%'));
// URIError: URI malformed
```

<br><br>

**4 커스텀 에러**
```JavaScript
try {
	var age = 15;
	console.log('학생:', '아저씨 담배 하나 주세요')

	if ( age < 18) {
		throw '미성년자는 담배를 살 수 없습니다' // 에러 던지기, throw 커스텀 에러
	}

	// throw 아래 코드는 실행되지 않음.
	console.log('직원:','여기 있습니다')

} catch (error){
	console.error('실패:',error)
} finally {
	// 에러 발생 여부와 상관 없이 항상 실행됨.
	console.log('끝')
}

<br>
```
<h6>3/20 수업 , 3/30 정리 복습</h6>
