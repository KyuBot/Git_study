# Git add

1. git add 파일명
2. staging area로 변경
3. git status
4. 커밋에 반영될 변경사항과 커밋에 반영되지 않는 변경 사항을 보여줌
5. git add . : 모든 파일을 staging area에 놓는다



> git 은 2가지 상태를 가진다
>
> - untracked : 한번도 git add 하지 않은 상태
>
>  - tracked : git에 의해 변동사항이 추적되고 있는 상태
>    	- staged : staging area에 올라와 있는 상태
>       	- unmodified : 최신 커밋 모습과 비고했을 때 전혀 바뀐게 없는 상태 ( 커밋하고난 직전 모습 )
>    	- modifeid : 최근 커밋 모습과 비교했을 때 조금이라도 바뀐 내용이 있는 상태



### git add 취소

- git reset 파일명
- staging area에서 삭제 됌



### git help

> git help 알고 싶은 커맨드 이름
>
> man git-커맨드 : git help 와 같음