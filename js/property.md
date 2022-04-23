# Property (js)

> ***해당 object의 특징, 속성***. 데이터 구조와 연관된 속성을 나타냄
> 

### property의 종류

- 인스턴스 프로퍼티 (Instance property)
    
    : 특정 object 인스턴스의 특정한 데이터를 가지고 있음
    
- 정적 프로퍼티 (Static property)
    
    : 모든 object 인스턴스들에게 공유되는 데이터를 가지고 있음
    

### About property

- 구성
    - 이름 (string, symbol)
    - 값 (원시함수(primitive), 메서드(method), 객체 참조(object reference))
- 주의할 점❗️
    - ‘property가 object를 가지고 있다’ → ‘property가 object reference’를 가지고 있다는 뜻
    - 즉, property의 값을 변경할 때, 기존에 참조된 object는 그대로 남아있음 → 이걸 구분하는게 중요
    - property에 object를 담을 수 있음
        
        → object를 담는게 아니라 object의 reference를 담고 있는 것(메모리 번지 주소)
        

### property와 method

- property는 object를 위해서 데이터를 저장
- method는 object가 요청 받을 수 있는 액션