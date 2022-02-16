# js 코테 노트


- 리스트 안 중복 엘리먼트 제거
    1. `const 변수 = Array.from(new Set(해당list))` → 잘 안씀
    2. `const 변수 = [...new Set(해당list)]` 
        
        → Set로 list에서 중복 엘리멘트 제거하고, spread 연산자로 펼쳐준 다음, []배열로 마무리
        
- min, max함수
    - 배열 아닐 때
        - Math.max(1,2,3) ⇒ 3
        - Math.min(1,2,3) ⇒ 1
    - 배열일 때
        - Math.min(...해당list)
        - Math.max(...해당list)
        
- 배열 오름차순 정렬
    - 배열.sort((a,b) ⇒ a-b);

- 배열 합치는 3가지 방법
    1. concat() 함수
    2. ... spread(전개연산자)
    3. push()함수 & spread