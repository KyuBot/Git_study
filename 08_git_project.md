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