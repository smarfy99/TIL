# jQuery

### jQuery

> js를 사용하기 쉽게 해주는 라이브러리
> 

**장점**

1. 간결한 문법
2. 편리한 API
3. 크로스 브라우징 - 모든 브라우저에서 동일한 기능 제공

- **jQuery 사용법**
    
    html상에 아래 태그를 넣어주면 됨
    
    <script src="[https://code.jquery.com/jquery-3.6.0.min.js](https://code.jquery.com/jquery-3.6.0.min.js)" integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>
    

### jQuery 문법

---

```jsx
$(선택자).행위;

//js
var content = document.getElementById('jasoseol').value;

//jQuery
<script>
//해당 id의 value값을 가져옴
	$('#id값').val()
</script>
```

- **jQuery 이벤트**
    
    ```jsx
    //js
    <button id='click' onclick='hello()'>클릭</button>
    
    //jQuery
    <button id='click'>클릭</button>
    $('#click').click(hello);
    ```
    

- **익명 함수**
    
    : 함수를 한 번만 사용한다면) 
    
      함수를 정의하는 과정없이 바로 사용할 수 있게 하는 함수
    
    ```jsx
    $('#click').click(function(){
    	console.log('hello');
    })
    ```
    

.animate(css properties, [duration], [easing], [complete])

: 특정 CSS  속성을 서서히 변화시켜 주기 위한 함수

→ **callback함수** : complete를 적으면 이 함수가 끝난 후에 다음 함수를 실행하는 함수

⇒ 비동기 처리의 결과물