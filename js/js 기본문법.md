# js 기본문법


### 함수

---

`console.log()`

출력

`alert()`

알림창

`prompt()`

input

`typeof()`

자료형 알려줌

### 변수 선언과 초기화

---

**변수**

: 프로그램 실행 도중 임의의 값을 저장해 두고 읽을 수 있는 공간

- 선언 : 컴퓨터에게 변수 사용할 거라고 알려주는 역할
- 초기화 : 선언한 변수에 처음으로 값을 저장하는 과정

```jsx
var a;
var = 10;
```

### es6+ 변수

---

- `var` : 중복선언 가능 → 변수 선언

```jsx
var num = 10;
console.log(num);

var num = 20;
console.log(num);

=> 10
   20
```

- `let` : 중복선언 불가능 / 변수의 값 변경 **가능 → 변수** 선언
- `const` : 중복선언 불가능 / 변수의 값 변경 **불가능 → 상수** 선언

**변수 네이밍**

1. **변수** 카멜케이스 - ex) listOver
2. 변수 이름 시작 - `_ / $ / 문자` 로만 시작
3. **상수** 스네이크케이스 - ex) MAX_LEVEL

### 자료형

---

: 변수에 저장할 수 있는 값의 종류

- number type : 숫자

```jsx
var a=100, b=3.14;
```

- string type : 문자열

```jsx
var c="안녕하세요", d="a";
```

- boolean type : True/False

```jsx
var e=true, f=false;
```

**Number(숫자)**

: 정수, 실수 구분하지 않고 통일

`parseInt()` `parseFloat()`

→ 문자열을 숫자로 변환할 시 맨 앞 숫자부터 차례대로 처리

**String(문자열)**

- `“”` `‘’` 모두 가능 → 섞어서 사용할 순 x
- `“”` 문자열에는 `‘’` 사용가능 / `‘’` 문자열에는 `“”` 사용가능
- `\`(escape character)를 이용해 `‘’`, `“”` 모두 사용가능

```jsx
"이렇게 \'이렇게\' 사용하자"
```

- 역슬래쉬 쓰고 싶으면 `\\` 이렇게 2번 쓰기
- 줄바꿈 `\n` (newline character)

### 객체 (object)

---

: 속성(property)의 집합

```jsx
//객체 사용방법
{
	//객체 정의
}
ex)
var man = {name:"홍길동", age:20, height:190};

//객체 접근방법
man.name
man["name"]

//객체 속성변경방법
man.name = "정지원"
man["age"] = "정지원"
```

### undefined & null

---

undefined

- 어떤 변수나 속성이 정의되지 않은 경우
    - 선언만 하고 초기화 되지 않은 변수
    - 객체의 정의되지 않은 값

null

- 아무것도 없는 비어있는 상태를 나타낼 때
    - typeof 결과 : object이며 값은 null

### 연산자 (arithmetic operator : 산술연산자)

---

이항연산자

- +(더하기), -(빼기), *(곱하기), /(나누기), %(나머지)

단항연산자

- ++a; 는 a=a+1과 같음
- —a; 는 a=a-1과 같음

```jsx
var a;

a = 1;
console.log(++a);
console.log(a);
=> 2 2

a = 1;
console.log(a++);
console.log(a);
=> 1 2
```

Math

- `Math.pow(a,b)` : a의 b승
- `Math.sqrt(a)` : a의 제곱근
- `Math.random()` : 0~1 사이 임의의 난수 발생

### 함수

---

- 반복되는 코드 감소
- 코드의 개발 및 수정 용이

**함수 정의**

```jsx
function 함수이름(파라미터1, 파라미터2){
    /*
        실행될 코드
    */
    return 반환값;(생략 가능)
}
```

**함수 호출**

```jsx
var inp = prompt();
console.log("Hello World"); 
var randomValue = Math.random();
```

### 관계연산자 (relational operator)

---

- && and
- || or
- ! not (ex. !true)

**연산자 우선순위**

- ++, --
- !
- *, /, %
- +, -
- <, <=, >, >=
- ==, !=
- &&
- ||
- 괄호를 사용하여 우선순위 사용 가능

### string 이어붙이기

---

`.length`

문자열의 길이

ex) `“hello”.length` ⇒ 5

**문자열 붙이기**

1. `.concat`
    
    ```jsx
    var str = "hello"
    var str2 = "world"
    str.concat(str2); => "helloworld"
    
    var str3 = str.concat(str2).concat("!");
    => helloworld!" 
    ```
    
2. 더하기(+) 사용
    
    ```jsx
    1)
    "Hello" + " World";
    =>"Hello World"
    2)
    "Pi is" + 3.14;
    =>Pi is 3.14
    ```
    

### string 다루기

---

**특정 위치 문자열 알아내기**

- `.charAt` 함수 이용
    - 첫 문자 : `str.charAt(0)`
    - 마지막 문자 : `str.charAt(str.length-1)`
- 대괄호([]) 사용
    - 첫 문자 : `str[0]`
    - 마지막 문자 : `str[str.length-1]`
    

**부분문자열 구하기**

- `.substring(a,b)`
    
    : a에서 b-1까지의 문자열 반환
    
    - `.substring(a)`
        
        : a에서 문자열 끝까지 반환
        
- `.substr(a,length)`
    
    : a에서 length 길이 만큼 문자열 반환
    
    - `.substr(a)`
        
        : a에서 문자열 끝까지 반환
        
    - `.substr(-a)`
        
        : 끝에서 a만큼의 문자열에서부터 끝까지 반환
        
    - `.substr(-a, length)`
        
        : 끝에서 a만큼의 문자열~length만큼의 문자열 반환
        

**문자열 위치 알아내기**

- `.indexOf("bc");` ⇒ 2
    
    : 해당 문자열 중 가장 앞의 문자열 위치를 반환
    
- `.lastIndexOf(str);`
    
    : 해당 문자열 중 가장 뒤의 문자열 위치를 반환
    

### 배열(array)

---

: 값을 저장할 수 있는 엘리먼트(변수)의 연속된 공간.

주소(인덱스)를 통해 각 엘리먼트에 접근 가능

**배열의 정의**

- 빈 배열  :  var arr=[];
- 초기화된 배열 : var arr=[1,2,3];
- 엘리먼트에는 어떤 자료형이든 저장 가능
    - `var mixed_arr = [1, true, 3.14, “string”, {name:”object”}, [1,2,3]];`
    

**배열의 엘리먼트에 접근하기**

- arr[index]
- console.log(arr[arr.length-1]);

**배열 사용하기**

- `.push(2)` : 배열의 뒤에 엘리먼트 추가
- `.pop()` : 배열의 뒤에서 엘리먼트 삭제하고 리턴
- `.shift()` : 배열의 앞에서 엘리먼트 삭제하고 리턴
- `.unshift(2)` : 배열의 앞에 엘리먼트 추가
- `.sort()` : 배열 오름차순으로 정렬
- `.reverse()` : 배열 앞뒤 바꿔서 정렬

**split 함수**

: 문자열을 구분자로 나눠서 각각을 담은 배열로 반환

```jsx
var str="1,2,3,4,5";
arr = str.split(",");
=> arr = ["1","2","3","4","5"]
```

**slice()**

: 배열 일부분 잘라 새로운 배열로 리턴

`배열.slice(1,3)`

- 인덱스 1부터 3전까지, 즉 2까지

`배열.slice(-3,-1)`

- 인덱스 뒤에서 3부터 맨뒤 전까지

여기마 ㅓㄹ미ㅏㄹ먼이ㅏㄹ먼이ㅏㄹ

### 주석

---

- 한 줄 주석 : `//`
- 여러 줄 주석 : `/* */`

### if문 (조건문)

---

```jsx
if(조건식){
    /*참인경우 실행될 코드*/
}
else if(){
    /*if 문의 조건이 거짓이고, 위의 조건식이 참인경우 실행될 코드*/
}
/* 여러개의 else if... */
else if(){
   
}
else{
}
```

### switch문

---

: 조건에 따라 특정 코드가 실행되도록 함

```jsx
switch(비교할 값){
    case /*값1*/:
        /*비교할 값이 값1인 경우 실행될 코드*/
        break;
    case /*값2*/:
        /*비교할 값이 값2인 경우 실행될 코드*/
        break;

    /*
    ... 여러개의 case
    */

    default:
        /*비교할 값이 위의 모든 값과 다른 경우 실행될 코드*/
        break;
}
```

**break**

: break 만나면, switch-case {} 밖으로 빠져나옴

### while문 (반복문)

---

```jsx
while( 조건식){
    /* 반복 실행될 코드 */
}
```

- **continue** : 남은 반복실행될 코드 모두 skip
- **break** : 반복문에서 즉시 탈출

**do while문**

: 한 번은 코드가 실행되고, 이후에 반복될지 말지 결정

```jsx
do{
    /* 반복 실행될 코드 */
}while( /*조건식*/ );
```

**조건식이 거짓(false)일 때,**

- while : 한번도 실행되지 않음
- do, while : 한번은 실행되고 종료

### for문 (반복문)

---

- for문에서 continue, break 사용 가능
- **for문**에서 continue 만나면 코드 끝으로 이동 후update구문으로 이동
    
    update문 
    
    `for(var i = 0; i < array.length; i++)` 에서 i++ 한 번 하고 조건식 검사
    
- 반면 **while문**은 continue만나면 반복실행 코드 끝으로 이동 후, 조건식 검사

while문

```jsx
var sum = 0;
var i = 0; //초기 설정 코드
while( i < 5 /*조건식*/ ){
    sum = sum + i;
    i++; // 업데이트 코드
}
```

for문

```jsx
var sum = 0;
for( var i = 0 ; i < 5 ; i++ ){
    sum = sum + i;
}
```

**for in문**

- 객체의 key값을 가져오고 싶을 때 - `object.keys()`
    
    ```jsx
    var obj={
    	"속성1":1,
    	"속성2":2
    }
    object.keys(obj);
    ```
    

- 객체 안의 속성 값들에 대해 자동으로 순차적으로 값을 반환해줌
    
    
    for in문
    
    ```jsx
    
    var obj = {
    	name:"object",
    	age:10,
    	weight:5
    }
    var sum=0;
    for( var i in obj ){
    	if(typeof(obj[i]) = "number"){
    		sum = sum + obj[i];
    	}
    }
    ```
    
- 이 외에 in은 객체 안에 존재하는 지를 반환
    
    ⇒ true/false로
    

**for of문**

- 

### 변수의 scope

---

: 선언한 변수가 유효한 영역

**function scope**

→ 변수의 scope는 function의 scope를 따른다

→ 객체(변수)는 선언된 함수 안에서만 접근이 가능하다

### 변수의 shadowing

---

- 함수 안에서만 사용되어야 할 변수는 function 안에서 선언
- 포괄적으로 사용되어야 할 변수는 function 밖에서 선언

**shadowing**

- 함수 밖에서 선언되었던 같은 이름의 변수를 함수 안에서 사용하는 경우
    - 함수 밖 변수는 잠시 가려짐(shadowing)
    - 함수 안에서는 해당 함수에서의 변수 사용(함수 밖 변수 값은 변하지x)
    - 함수에서 빠져나오면 다시 함수 밖 변수에 접근 가능

### method, this

---

### closure(클로저)

---