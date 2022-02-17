# Git

### Git이란?

---

source 관리를 위한 분산 버전 관리 시스템

- **로컬 저장소(local) & 원격 저장소(remote)**
    - 자신의 컴퓨터 - local / 서버 - remote
        
        → local에서 작업한 것은 remote로 push해줘야 함
        

- add, commit, push
    - 자신이 작업한 내용을 remote 저장소에 반영하기 위해서는
    - add - 변경사항 추가
    - commit - local에 저장
    - push - remote에 업로드
    
- branch
    - 여러 개발자들이 공동으로 작업할 수 있게 main branch에서 새로운 가지를 만드는 과정

- pull
    - remote에 있는 내용을 local에 받는 과정
    

### Git 명령어

---

- `git init` git 생성하기
- `git clone git주소` clone 받아오기
- `git log` local저장소의 커밋 history보기

branch

- `git branch` 현재 branch 및 local branch 확인
- `git checkout 브랜치이름` 브랜치 옮기기
- `git checkout -b 브랜치이름` 브랜치 만들고 이동
- `git branch 브랜치이름` 브랜치 생성
- `git branch -d 브랜치이름` 브랜치 삭제
- `git branch -D 브랜치이름` 브랜치 강제 삭제
- `git branch -m 브랜치이름 바꿀이름` 브랜치 이름 변경

upload

- `git add .` 변경사항 추가
- `git commit -m “설명”` 커밋 내용 적기(local에 저장)
- `git push origin 브랜치이름` 해당 브랜치로 커밋 push(remote로 push)
- `git pull` git 서버에서 최신 코드 받아와 merge
- `git fetch` git 서버에서 최신 코드 받아오기
