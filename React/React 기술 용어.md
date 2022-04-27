# React.js

[velopert](https://velopert.com/3612)

## React 기술 용어 모음

### SPA : 싱글 페이지 애플리케이션

> 하나의 HTML 페이지와 애플리케이션 실행에 필요한 JS, CSS 같은 모든 자산을 로드하는 애플리케이션
> 

### 컴파일러(compiler)

> JS 코드를 변환하고 다른 형식으로 JS 코드를 반환
ex) Babel, React
> 

### 번들러(bundler)

> 분리된 JS와 CSS 모듈 코드를 브라우저에 최적화된 여러 개의 파일로 결합
ex) Webpack, Browserify
> 

### 패키지 관리자

> 프로젝트의 종속성을 관리할 수 있는 도구
ex) npm, Yarn
> 

### CDN(Content Delivery Network)

> 전 세계의 서버 네트워크에 캐시된 정적 콘텐츠를 제공
> 

### JSX

> JS의 확장 문법
> 
- JSX는 React.createElement()의 호출을 통해 일반 JS 객체인 ‘React 엘리먼트(React element)’로 컴파일
- React DOM은 캐멀케이스(camelCase)를 네이밍 컨벤션으로 이용
    
    ex) tabindex → tabIndex
    

### 엘리먼트(React Element)

> 화면에 보이는 것들을 기술, React 엘리먼트는 변경되지 x
> 
- 직접 사용되지 않고 컴포넌트로부터 반환됨

### 컴포넌트(component)

> React 컴포넌트는 페이지에 렌더링할 React 엘리먼트를 반환하는 작고 재사용 가능한 코드 조각
> 
- 컴포넌트 이름은 항상 대문자로 시작
    
    ex) `<wrapper/>` x → `<Wrapper/>`
    

### props

> 컴포넌트의 입력값. 부모 컴포넌트로부터 자식 컴포넌트로 전달된 데이터
> 

❗️props는 읽기 전용. 어떤 방식으로든 수정 절대 금지❗️

- **state** : 사용자의 입력 or 네트워크 응답에 반응하여 어떤 값을 수정하려면 state 사용

### props.children

> 모든 컴포넌트에 사용 가능
여는 태그와 닫는 태그 사이의 내용을 포함
> 

```jsx
<Welcome>Hello world!</Welcome>
//Hello world! 문자열은 Welcome 컴포넌트의 props.children으로 사용 가능

function Welcome(props) {
	return <p>{props.children}</p>;
}
```

### state

> 컴포넌트와 관련된 일부 데이터가 시간에 따라 변경될 경우
> 
- Checkbox 컴포넌트는 `isChecked` state가 필요할 수 있음
- **props vs state**
    - props - 부모 컴포넌트로부터 전달 받음
    - state - 컴포넌트에서 관리됨
    - 컴포넌트가 props는 변경 불가, state 변경 가능
- 해당 상태(state)를 ‘소유’하는 컴포넌트는 하나만 존재해야 함

### 생명주기 메서드

> 컴포넌트의 각각의 단계에서 실행되는 커스텀 기능
> 
- 컴포넌트가 **1)업데이트, 2)DOM에서 마운트 해제, 3)제거** 될 때 사용할 수 있는 기능 제공

### 제어 컴포넌트 vs 비제어 컴포넌트

> 2가지 방식으로 form 입력을 처리
> 
- **제어 컴포넌트(controlled component)**
    - ***대부분 이걸 사용***
    - react에 의해 입력값이 제어되는 엘리먼트
    - 데이터를 입력 → 변경 이벤트 핸들러 호출 → 입력 유효 여부 결정
- **비제어 컴포넌트(uncontrolled component)**
    - form 엘리먼트가 react 외부에서 작동하는 것처럼 작동
    - 사용자가 form 필드에 데이터를 입력하면 react가 별도 처리 필요 없이 엘리먼트에 반영
    

### key

> 엘리먼트 배열을 만들 때 포함해야 하는 특별한 문자열
> 
- 어떤 항목을 변경, 추가, 삭제할지 식별하는 것을 도움
- 같은 배열의 다른 요소 사이에서만 고윳값을 가지면 됨
    
    → 전체 애플리케이션 or 단일 컴포넌트 전체에서 고윳값 가질 필요x
    
- Math.random() 같은 값을 key로 사용하면 안됨
    
    → ‘안정적으로 식별 가능’해야 함 (ex) post.id)
    

### Ref

> 컴포넌트에 접근할 수 있응 특수한 attribute
> 
- React.createRef()함수, 콜백 함수, 문자열로 생성 가능
- ref attribute가 콜백 함수인 경우, 함수는 DOM 엘리먼트나 class 인스턴스를 인자로 받음
    
    → 컴포넌트 인스턴스나 DOM 엘리먼트에 직접 접근 가능
    
- 가능한 적게 사용할 것

### 재조정

> state나 prop가 변경되었을 때, react가 DOM을 업데이트 하는 것
