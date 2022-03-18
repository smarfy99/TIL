# django 베이스

### 딕셔너리

: 데이터를 대응시켜주는 자료형

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled.png)

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%201.png)

### 예외처리

- 파이썬의 오류
    1. 문법 에러(파싱 에러)
        
        : 실행 자체에 영향을 주는 치명적인 오류
        
    2. 예외
        
        : 실행 중 감지되는 오류
        
          실행 자체에 영향을 주지는 않음
        
        **→ 프로그램을 멈추지 않고 실행시키기 위해**
        
    
    ![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%202.png)
    
    ![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%203.png)
    

### 객체지향

: 변수-상태 / 함수-동작

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%204.png)

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%205.png)

### 모듈, 패키지, 라이브러리

- 모듈 : 파이썬으로 정의된 파일
- 패키지 : 모듈의 집합, 모듈의 계층단위
- 라이브러리 : 쓸 만한 기능들을 모듈/패키지로 만들어 놓은 것

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%206.png)

### What is WEB?

- **WEB** : 정보의 그물망 (하이퍼링크)
- **URL** : 정보자원이 어디에 있는지
- **HTTP** : 정보자원으로 접근하고 통신하게 해주는 약속
    - HTTP 요청
        - **GET** : 갖다줘!
        - **POST** : 이 데이터를 처리해줘!
- **HTML**
    - 응답으로서의 정보 자원 자체
    - 다른 정보 자원과 연결 매개체

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%207.png)

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%208.png)

### 웹 프레임워크

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%209.png)

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%2010.png)

- 프레임워크 : 명확한 목적을 달성하기 위해 이미 설계까지 만들어진 구조/뼈대
- 라이브러리 : 도구의 모음

## Django 개념

---

### MVC, MTV 패턴

- 설계원칙 : **디자인 패턴**

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%2011.png)

- MVC
    - M : model (1번)
    - V : view (2번)
    - C : controller (3번)
- MTV
    - M : model (1번)
    - T : template (2번)
    - V : view (3번)

### 개발환경 세팅

- 가상환경 : 독립적인 개발이 가능하게끔 세팅

`django-admin startproject 이름`

새 프로젝트 만들기

`python -m venv myvenv(가상환경 이름)`

가상환경 만들고, 실행하기

`source myvenv/Scripts/activate`

가상환경 만들고, 실행하기

`deactivate`

가상환경 끄기

- 각 파일별 설명

| init.py | 패키지라는 것을 알려줌 |
| --- | --- |
| urls.py | url 등록, 관리 |
| manage.py | 1. 서버 켜기
2. application 만들기(장고의 단위)
3. database 초기화 및 변경사항 반영
4. 관리자 계정 만들기 |
| settings.py | DEBUG = True (개발자용) 
DEBUG = False (배포용 서버 켜기) |

### manage.py

`python manage.py runserver`

1. 서버 실행

`python manage.py startapp 이름`

1. application 만들기

**settings.py > application 추가하기**

![Untitled](django%20%E1%84%87%E1%85%A6%E1%84%8B%20fa8ac/Untitled%2012.png)

`python manage.py migrate`

1. database 초기화 및 변경

`python manage.py createsuperuser`

1. 관리자 계정 생성

### settings.py