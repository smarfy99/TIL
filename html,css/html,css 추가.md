# HTML/CSS 추가

### HTML attribute(속성) vs CSS property(속성)

---

- attribute : 태그 안에서 명시되는 태그의 속성
- property : CSS 파일 내에 스타일 적용을 위해 사용하는 속성

### block vs inline

---

- `block`
    - <div, p, h, li>태그
    - 줄바꿈 - 가로 영역 모두 채움
    - width, height 속성 가짐
- `inline`
    - <span, b, i, a>태그
    - 줄바꿈 x
    - width, height 속성 x
- `inline-block`
    - block과 inline의 중간 형태
    - 줄바꿈 x
    - 크기 지정 가능

> 주의할 점
> 
- 인라인 요소는 `height`가 적용되지 않는다.
- 인라인 요소는 `width`가 적용되지 않는다.
- 블록 요소는 `vertical-align` 이 적용되지 않는다.
- 블록 요소는 `text-align`이 적용되지 않는다.

### display 속성

---

- `none` : 보이지 않음 (영역 차지x)
    - visibility : hidden 으로 하면 영역을 차지하면서 보이지 않음
- `block` : 블록 박스
- `inline` : 인라인 박스
- `inline-block` : block과 inline의 중간형태

### position 속성

---

: 태그를 어떻게 위치시킬지

- `static` : 기본값, 다른 태그와의 관계에 의해 자동 배치
- `absolute` : 절대 좌표와 위치 지정
- `relative` : 원래 있던 위치를 기준으로 좌표 지정
- `fixed` : 스크롤 상관x, 항상 문서 최 좌측상단 기준 좌표 고정
- `inherit` : 부모 태그 속성값 상속

> 부모 - positon : relative
자식 - position : absolute
부모 위에 자식 class 위치시킬 수 있음
> 

### css 속성

---

- `overflow:hidden`
    - 튀어나온 부분 숨김
- display:flex - justify-content:center
- display:block - text-align:center
    
    (inline요소도 display:blcok하면 block요소로 바뀜)
    

### hover 속성

---

: 마우스를 위에 올렸을 때 변할 속성

- `id-box:hover .bottom`
    - id-box를 hover했을 때 class bottom의 css
    

### ::after, ::before

---

: 가상 요소

- 부모 요소 앞, 뒤에 가상요소를 넣을 수 있음

```css
span.or-text:before {
    content: '';
    position: absolute;
    top: 5px;
    left: 12px;
    background-color: gray;
    opacity: 0.8;
    height: 1px;
    width: 43%;
}

span.or-text:after {
    content: ''; 
    position: absolute;
    top: 5px;
    right: 12px;
    background-color: gray;
    opacity: 0.8;
    height: 1px;
    width: 43%;
}
```

- content에는 ‘텍스트’, url(이미지 주소), 등을 넣을 수 있음

### 상속

---

1. nth-child