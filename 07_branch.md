# 브랜치

> 하나의 코드 관리 흐름

- git status : 어떠한 브랜치인지 보여준다
- git branch 브랜치명
- git checkout 브랜치명 : 브랜치로 이동



### 브랜치 명령어

- git branch : 브랜치 명을 조회 (현재 위치는 *표시가 되어있음)
- git branch 브랜치명 : 브랜치 생성
- git branch -d 브랜치명 : 브랜치 삭제
- git checkout -b 브랜치명 : 브랜치를 생성하면서 이동



### Merge

- git merge 브랜치명
- confilct 시 : 충돌 나는 두 부분 중 하나만 선택을 해야한다.
- 합치지 않고 취소하려면 : git merge --abort
- confilct 가 해결된 상태 : resolved
- 파일이 여러개일 경우 중간중간  git status를 통해서 수정된 사항을 살펴본다



### Origin

> 리모트 레포지토리로 관례적으로 origin을 씀. 다른 단어로 사용 가능

- git push -u origin master
- 이때 master 브랜치가 없을때 master 브랜치를 새로 생성하고 푸시
- -u : --set-upstream 
  - 로컬 레포지토리에 있는 master 브랜치가
  - origin에 있는 master 브랜치를 추적하는 것으로 설정
- 만약 처음 tracking 하지 않고 있다면
  - git push origin master:master 
  - origin : 리모트 레포지토리
  - 앞 master : 로컬 레포지토리
  - 뒤 master : 리모트 레포지토리의 master 브랜치



### HEAD 와 브랜치의 관계

- HEAD : 어떤 커밋 하나를 가리킴
- branch : 하나의 코드 관리 흐름 (포인터)
- HEAD -> branch -> commit 을 가리킴
- merge : 헤드가 가리키던 커밋에 다른 브랜치가 가리키던 커밋을 합쳐서 새로운 커밋을 만드는 작업
- git reset을 한다고 이후 커밋들이 삭제되는게 절대 아니다. 계속 남아있음
  - HEAD가 가리키는 위치만 달라질뿐
- git checkout 은 HEAD 가 커밋을 직접적으로 가리키게 할 수도 있고, 브랜치를 직접 가리키게 만들수도 있다
- git checkout 커밋아이디 : HEAD 가 직접 커밋을 가리킴 : Detached HEAD



### Merge commit

- 머지를 통해서 생겨난 커밋 : 머지 커밋
- 총 커밋수는 그대로 이고 단지 브랜치가 이동하게 되는 머지 : Fast-forward 머지
- 새로운 커밋이 생기는 머지 : 3-way merge
- 조상 브랜치 : base, 분기 branch 2개 => 3-way merge
- 3-way merge 에서는 기본 base에서 변화가 발생한 것을 우선 채택 (중요!!)
- 이때, 두 branch 에서 둘다 변화가 있으면 머지할시 confilct!!!