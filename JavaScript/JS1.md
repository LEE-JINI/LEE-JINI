
<br> 
<h1>JavaScript</h1>
<br>

#1
데이터 타입
연산자
 
<br><br>

데이터 타입  
1. String (문자열)
2. Number
3. Boolean
4. null
5. undefined
6. BigInt

<br><br>

**String (문자열)**  
연속된 문자 '', "" 안에 값을 작성한다
```JavaScript
 var foo = 'bar'

console.log(foo) // bar
console.log(typeof foo) // string

console.log(foo[0]); // b
console.log(foo[1]) // a
console.log(foo[2]) // r

console.log(foo.length) // 3
```
<br><br>


**Number**  
-(2^1024-1) 에서 2^1024-1 사이의 숫자를 나타낸다  
값의 종류: 정수, 소수, NaN(Not a Number), +Infinity, -Infinity

<br>

 
정수
```JavaScript   
var year = 2023;
console.log(year); // 2023
console.log(typeof year); // number
```
소수
```JavaScript 
var pi = 3.14
console.log(pi); // 3.14
```
 
NaN(Not a Number)
```JavaScript
var nan = 2 - 'foo';
console.log(nan);
```

Number타입의 최대 값, Number타입의 최소 값
```JavaScript 
var max_value = Number.MAX_VALUE;
console.log(max_value);

var negative_max_value = -Number.MAX_VALUE;
console.log(negative_max_value);
```

양의 무한대, 음의 무한대
```JavaScript 
var infinity = Number.MAX_VALUE * 1.1;
console.log(infinity); // Infinity

var negative_infinity = -Number.MAX_VALUE * 1.1;
console.log(negative_infinity); // -Infinity
```

Boolean 참 또는 거짓 (true or false)의 값을 갖는다
```JavaScript 
var bool = true;

console.log(bool);
console.log(typeof bool); // boolean
```

비교연산이나 논리연산은 boolean값을 리턴한다
```JavaScript 
console.log(1 > 0) // true
console.log(1 == 2) // false
```
Null   
'무효' 또는 '없는'의 상태를 나타낸다
```JavaScript 
var foo = null;
console.log(foo); // null
console.log(typeof foo) // object
```
undefined  
정의되지 않은 변수를 나타낸다
```JavaScript 
var x;

console.log(x);
console.log(typeof x)
```

BigInt
```
안전한 정수(safe integer) 밖의 정수를 나타낸다
Number 타입 값의 뒤에 n을 붙여 선언한다
* 안전한 정수: -(2^53 - 1) 에서 2^53 - 1 사이의 정수
````

안전한 정수 (최대), 안전한 정수 최소

```JavaScript 
var max_safe_integer = Number.MAX_SAFE_INTEGER;
console.log(max_safe_integer);

var min_safe_integer = Number.MIN_SAFE_INTEGER;
console.log(min_safe_integer);
```

Number타입은 안전한 정수 밖의 정수를 정확하게 저장할 수 없다
```JavaScript 
var not_safe_integer = 9999999999999999;
console.log(not_safe_integer); // 10000000000000000

var bigint = 9999999999999999n;
console.log(bigint); // 99999999999999999n

console.log(typeof bigint) // bigint
```
<br><br>

**연산자**
1. 수리연산자
2. 할당연산자
3. 비교 연산자
4. 논리 연산자
5. 타입 연산자

<br>

- 수리연산자
    - 4칙연산 + - * /
    - 증가 연산자 ++
    - 감소 연산자 --
    - 제곱 연산자 **
    - 계수 연산자 %

    

4칙 연산
```JavaScript 
var add = 1 + 1
var subtract = 2 - 1
var divide = 1 / 2
var multiply = 1 * 1

console.log('덧셈:', add)
```

증가연산자
```JavaScript 
var i = 1;
i++
console.log(i)
```
제곱 연산자 (지수)
```JavaScript 
var exp = 2 ** 7
console.log(exp) // 128
```
계수 연산자 
```JavaScript 
var mod = 5 % 2;
console.log(mod) // 1
```

<br>


- 할당연산자
    - 변수할당연산자 =
    - 덧셈할당연산자 +=
    - 빼기할당연산자 -=
    - 곱하기할당연산자 *=
    - 나누기할당연산자 /=
    - 지수할당연산자 **=
    - 계수할당연산자 %=

<br>
    
변수할당연산자
```JavaScript
var foo = 'bar'
console.log(foo);
```

덧셈할당연산자
```JavaScript
var longVariablesName = 1;

longVariablesName = longVariablesName + 1 와 같다
longVariablesName += 1;

console.log(longVariablesName); // 2
```

<br>

- 비교 연산자
    - 동등연산자 ==
    - 비동등연산자 !=
    - 엄격동등연산자 ===
    - 엄격비동등연산자 !==
    - greater than 연산자 >
    - greater than or equal 연산자 >=
    - less than 연산자 <
    - less than or equal 연산자 <=

    

동등연산
```JavaScript
console.log('동등:', 2023 == 2023) // true
console.log('동등', 2023 == '2023') // true
console.log('동등:', null == undefined); // true
```
비동등연산
```JavaScript
console.log('비동등', 2023 != 2023) // false
console.log('비동등', 2023 != '2023') // false
console.log('비동등', null != undefined) // false
```

엄격동등연산
```JavaScript
console.log('엄격동등', 2023 === 2023); // true
console.log('엄격동등', 2023 === '2023') // false
console.log('엄격동등', null === undefined) // false
```
엄격비동등연산
```JavaScript
console.log('엄격비동등', 2023 !== 2023) // false
console.log('엄격비동등', 2023 !== '2023') // true
console.log('엄격비동등', null !== undefined) // true
```

greater than 
```JavaScript
console.log(1 > 0)
```
<br>

- 논리연산자
    - AND (그리고) expr 1 && expr 2
    - OR (또는) expr 1 || expr2
    - ! (NOT) !expr


    
AND 
```JavaScript
console.log(1 > 0 && 1 < 2) // true
```
OR
```JavaScript
console.log(1 > 0 || 1 > 2) // true
```
NOT (부정)
```JavaScript
console.log(!(1>0)) // false
console.log(!true) // false
```

boolean타입이 아닌 다른 데이터 타입을 부정할 경우

```JavaScript
console.log('Not null:', !null) // true
console.log('Not undefined', !undefined) // true
console.log('Not zero:', !0) // true
console.log('Not 빈문자열', !""); // true
```
<br>

<h6>3/13 수업 , 3/27 정리 복습</h6>