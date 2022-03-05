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
- git pull = git merge + git fetch



### git blame

- 어떤 파일의 특정 코드를 누가 작성했는지 찾아내기 위한 커맨드
- git blame 파일명
- 파일이 수정되었던 부분의 커밋 아이디가 나옴
- git show 커밋 아이디 



### git revert

- git revert 커밋 아이디
- git push 한 것을 취소하다
- git revert 후 git push를 해야한다
- git reset을 하고 push를 할 수 없기 때문에 이럴때는 사용 x (git pull을 사용하라고 뜬다)