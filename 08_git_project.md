# Git 협업하기

- git push 시 충돌 나는 상황

  - 로컬에서 git commit

  - 리모트 레포지토리 git commit

  - 이때 git push : reject 된다

  - 로컬 레포지토리 수정을 하고 리모트 레포지토리에서 이미 변화가 있다면

    1. 우선 git pull을 한다
2. confilct 발생!
    3. conflict가 발생한 곳에서 소스 수정
4. git commit
    5. git push





### git fetch

- merge는 하지않고 가져오기만 하는 명령어
- git pull => 자동으로 머지가 됌
- 리모트 레포지토리에 있는 브랜치의 내용을 살펴본 후 머지를 할때 사용
- git diff : 브랜치간의 차이도 볼 수 있음

