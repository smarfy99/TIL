# ES6+문법
### 변수

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

변수 네이밍

1. **변수** 카멜케이스 - ex) listOver
2. 변수 이름 시작 - `_ / $ / 문자` 로만 시작
3. **상수** 스네이크케이스 - ex) MAX_LEVEL

### Spread syntax

---

: **배열, 객체**를 동일하게 copy 해올 수 있음

- object값을 복사해오는 것이 아니라 object의 주소값을 가져오는 것이기 때문에
    - array, arrayCopy 모두 동일한 obj1,obj2를 가리키고 있음
    - 즉, obj1, obj2를 변경하면 arrayCopy 또한 값이 변경됨

```jsx
const obj1 = {key:'key1'};
const obj2 = {key:'key2'};
const array = [obj1, obj2];

//array copy : [...]스프레드
const arrayCopy = [...array];
console.log(array, arrayCopy);

=> 둘 다 동일하게
	 {key:'Key1'}
	 {key:'Key2'}

//array에 추가하고 싶다면
const arrayCopy2 = [...array, {key:'Key3'}];
```

- 배열과 객체 모두 병합 가능
- 동일한 키를 가지고 있는 객체의 경우, 뒤의 객체가 앞의 객체를 덮어씌움

```jsx
//array concatenation
const fruits1 = ['a','b'];
const fruits2 = ['c','d'];
const fruits = [...fruits1, ...fruits2];
console.log(fruits);

=>['a','b','c','d']

//object merge
const dog1 = {dog:'a'};
const dog2 = {dog:'b'};
const dog = {...dog1, ...dog2};
console.log(dog);

=>{dog:'b'}
```

### Default parameters

---

### Template Literals

---

- 원래 문자열 + 변수를 반환할 때

```jsx
console.log('Today '+ weather + ' good');

```

- template literals

```jsx
console.log('Today ${weather} good');
```

false : false, ‘’, 0, null, undefined