# 커밋

- 커밋 히스토리 : git log
- git log를 쳤을때 commit 뒤에는 커밋아이디 (커밋해시)
- 커밋 히스토리 깔끔하게 보기 : git log --pretty=oneline
- git show 커밋아이디 : 해당 커밋 이전모습과 해당 커밋 모습을 비교해서 보여줌
- git commit : 커밋 메세지를 입력하는 창으로 전환 (vim으로 전환) : 복잡하고 긴 커밋 메시지를 쉽게 남길 수 있다.



### 최신 커밋 수정하기

- git commit --amend : 최신 커밋을 수정해서 다시 새로운 커밋으로 만들기
- 커밋 규칙 
  - 커밋 메세지의 제목과 상세 설명 사이에는 한줄 비우기
  - 커밋 메세지의 제목 뒤에 온점을 붙이지 말기
  - 커밋 메세지의 제목의 첫번째는 알파벳은 대문자
  - 커밋 메세지의 제목은 명령조로
  - 커밋의 상세 내용은 
    - 왜 커밋했는지
    - 어떤 문제가 있었는지
    - 적용한 해결책이 어떤 효과를 가지는지
  - 자신의 코드를 바로 이해할 수 있다고 가정하지 말고 최대한 친절하게 작성
  - 하나의 커밋에는 하나의 수정사항, 하나의 이슈를 해결한 내용만 남기기
  - 에러가 발생하지 않는 상태인 경우에만 커밋을 하기



### Alias

> git config alias.histroy 'log --pretty=online'
>
> = git histroy = git log --pretty=online



### diff

> git diff 커밋A 커밋B
>
>  = 두 커밋간의 차이가 보임
>
> = git show와 비슷하게 나옴



### HEAD

> 어떤 커밋 하나를 가리킴
>
> : 보통 가장 최근에 한 커밋을 가리킴
>
> 매번 더 새로운 커밋을 가리킴
>
> => HEAD가 가리키는 것에 따라서 working directory가 바뀐다

- git reset --hard 커밋 아이디
- 해당 커밋에 따라 working directory가 바뀐다!
- 이전 커밋으로 돌아갈때 사용



### git reset

- git add 를 할 때 마다 staging area에 있던 것들은 커밋을 하더라도 그것과 상관없이 계속 남아있는다
- --hard : working directory, staging area, repository 모두 바뀜 : 바뀐 커밋 이후 다 사라짐
- --soft :  working directory, staging area 안바뀜, repository 바뀜
- --mixed : working directory 안바뀜, staging area, repository 바뀜



