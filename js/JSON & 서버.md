# JSON & 서버

## HTTP (Hypertext Transfer Protocal)

---

> 클라이언트와 서버가 어떻게 소통하는지에 대한 규약
어떻게 hypertext를 서로 주고받는지를 약속
> 
- Hypertext : 링크, 이미지, 문서 등

![Untitled](JSON%20&%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%A5%20b0aaa6d5e37d469ba2d70d840d2e7b90/Untitled.png)

## 1. AJAX (Asynchronous Javascript And XML)

---

> 웹페이지에 동적으로 데이터를 주고받을 수 있게 하는 기술
> 

![Untitled](JSON%20&%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%A5%20b0aaa6d5e37d469ba2d70d840d2e7b90/Untitled%201.png)

- **XHR (XML Http Request)**
    - 이 object는 브라우저에서 제공하는 object로 간단하게 서버에 요청하고 데이터를 받아올 수 있음
- **XML (eXtensible Markup Language)**
    - Markup 언어 중 하나 - 태그를 이용해 나타냄
    - 파일 용량이 너무 커질 뿐만 아니라 가독성도 좋지 않아 사용 안하는 추세 → JSON 사용
    

## 2. **JSON (Javascript Object Notation)**

---

![Untitled](JSON%20&%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%A5%20b0aaa6d5e37d469ba2d70d840d2e7b90/Untitled%202.png)

- 가장 간단하게 데이터를 전달할 수 있는 포맷
- 텍스트 기반
- 가독성 좋음
- key-value로 구성된 파일 포맷
- 데이터를 전송, 직렬화(serialization)할 때 사용
- **프로그래밍 언어나 플랫폼에 상관없이 사용 가능**

### Serialize, Deserialize

![Untitled](JSON%20&%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%A5%20b0aaa6d5e37d469ba2d70d840d2e7b90/Untitled%203.png)

![Untitled](JSON%20&%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%A5%20b0aaa6d5e37d469ba2d70d840d2e7b90/Untitled%204.png)

1. **Object to JSON**
    
    stringfy(obj)
    
    ```jsx
    let json 
    ```
    
2. **JSON to Object**