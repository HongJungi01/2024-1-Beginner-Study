3주차 요약  
ㄴcommit 관리, 수정, 삭제하기  
  
git log
지금까지의 commit을 최신순으로 확인, 가장 위에있는 commit이 가장 최근 commit  
--oneline 명령어를 추가하면 각 commit을 한줄로 요약해준다.  

commit id란?  
각 commit을 식별하기 위한 고유의 번호, 40자 길이의 16진수를 사용한다.  
강의록에는 중복확률이 1/2^80이라고 적혀있는데, 16^40=2^160 아닌가?  
SHA-1해쉬함수를 사용  
  
HEAD는 현재 작업중인 branch  
현재 작업중인 브랜치의 가장 최근 commit을 보여준다.  
즉 다음 commit의 기반이 되는 commit을 보여준다고 할 수 있다.  
  
내 가장 최근 commit이 docs/1-readme에서 이루어지고, checkout을 통해 현재 main 브랜치에 있을 때  
git log가 보여주는 commit은 main에서 가장 마지막에 이루어진 commit을 보여준다.  
새 commit이 생기면 HEAD도 변경된다.  

git status  
세가지 상태에 따라 파일을 분류, untracked(빨간색), not staged(빨간색), committed(초록색)  

commit --amend  
마지막 commit의 내용을 수정한다. commit id도 변경됨.  
사실상 마지막 commit을 삭제하고 새로 commit한다고 볼 수 있다.  
--no-edit 명령어를 사용하면 메시지 수정 없이 commit만 수정, 즉 commit id만 바뀐다고 할 수 있다.  
다른 사람이 작업 기반으로 사용하고 있는 commit은 --amend하지 말 것.  
  
reset  
commit을 제거하는데에 사용됨  
3가지 옵션 soft, mixed(default), hard  
soft reset  
커밋만 취소하고 변경사항은 staging area로 돌아감.  
mixed reset  
커밋을 취소하고, working directory로 돌아감.  
hard reset  
변경사항을 모두 제거, 이전 커밋으로 돌아감.  
  
revert  
commit을 제거하는 일 없이 되돌린다.  
되돌리기 위한 commit이 새로 생성된다.  
--amend와 마찬가지로 --no-edit옵션을 이용할 수 있다.  
--no-commit 옵션을 사용해 직접 commit하지 않고 staging area에 되돌릴 수 있다.  
reset과 amend를 동시의 사용한것이라고 이해해도 되나?
