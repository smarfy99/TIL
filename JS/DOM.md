## DOM (Document Object Model)

> 웹 페이지에 대한 인터페이스
> 
- 여러 프로그램들이 페이지의 콘텐츠 및 구조, 스타일을 읽고 조작할 수 있도록 API 제공

## 웹 페이지가 만들어지는 원리

---

![image](https://user-images.githubusercontent.com/82459123/152915043-dabb52e2-d768-45cc-8399-0b3a17be3991.png)


### **Critical Rendering Path**

: 웹 브라우저가 원본 HTML 문서를 읽은 후, 스타일을 입히고 대화형 페이지로 만들어 viewport에 표시하는 과정

과정1️⃣

: 브라우저가 문서를 읽고 파싱하여 최종적으로 어떤 내용을 페이지에 렌더링할지 결정

→ **Render Tree** 생성

: HTML 요소 + 스타일 요소

<aside>
💡 Render Tree 생성 위해서 DOM & CSSOM 이 두 모델이 필요

</aside>

- DOM (Document Object Model) - HTML 요소들의 구조화된 표현
- CSSOM (Cascading Style Sheets Object Model) - 요소들과 관련된 스타일 정보의 구조화된 표현

과정2️⃣

: 브라우저가 렌더링 수행

## DOM은 어떻게 생성되고 보여질까?

---

- DOM은 HTML 문서의 객체 기반 표현 방식
- 단순 텍스트로 구성된 HTML 문서의 내용과 구조가 객체 모델로 변환되어 다양한 프로그램에서 사용 가능
- DOM의 개체구조는 ‘**노드 트리**’로 표현

![image](https://user-images.githubusercontent.com/82459123/152915137-1852af06-5a73-463a-a9d0-d29231b7970d.png)


### DOM이 아닌 것

---

1. **DOM은 HTML이 아니다**
    
    : DOM은 HTML 문서로부터 생성 but, DOM이 HTML과 다를 수 있는 2가지 케이스
    
    - 작성된 HTML 문서가 유효하지 않을 때
        
        →HTML 규칙에 안 맞아도 DOM 트리에는 올바르게 생성됨
        
    - JS에 의해 DOM이 수정될 때
        
        →JS를 통해 HTML을 변경하지 않고 DOM에 새로운 노드 추가 가능
        
2. **DOM은 브라우저에서 보이는 것이 아니다**
    - viewport에 보이는 것 : 렌더 트리(DOM + CSSOM)
    - 렌더 트리는 렌더링 되는 요소만 있기 때문에 시각적으로 보이지 않는 요소 제외
        
        ex) DOM 트리에는 존재하는 <p>How?</p>가 css에 display : none;일 때는 viewport에 보이지 x
        
3. **DOM은 개발도구에서 보이는 것이 아니다**
    - DOM은 HTML로부터 빌드되고, 요소에 적용되는 스타일은 포함x
    - 개발도구 요소 검사기는 DOM과 가장 가까운 근사치를 제공하지만 DOM에 없는 추가적인 정보를 제공
    
    ex) CSS 가상 요소
    
    `::before` `::after` 선택자를 사용한 CSSOM과 렌더 트리의 일부를 구성
    
    → not DOM
    

### DOM vs HTML 요약정리

---

- 항상 유효한 HTML 형식
- JS에 수정될 수 있는 동적 모델이어야 함
- 가상 요소 포함x
- 보이지 않는 요소 포함

참조 :  [https://wit.nts-corp.com/2019/02/14/5522](https://wit.nts-corp.com/2019/02/14/5522)
