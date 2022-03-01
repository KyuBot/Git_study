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

