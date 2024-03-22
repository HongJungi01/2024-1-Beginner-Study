1주차 학습 내용\n
ㄴgit의 개념 및 필요성에 대해 학습하고, git을 이용한 파일 관리, github에    관리된 파일을 업로드하는 방법을 배웠음.\n

git이 왜 필요한가.\n
ㄴ개발 과정에서 수많은 테스트, 수정, 정리 및 마감단계가 있을텐데 이 모든 과정에서의 파일의 버젼이 존재해야 빠른 수정, RollBack이 가능.\n
ㄴ누가 언제 파일을 수정하였고, 어떤 부분이 수정되었는지 빠르게 파악하여 파일을 관리하는데에 유용함\n

github\n
온라인 저장소를 이용한 git, 협력개발에 유용함\n

내가 만든 파일을 git에 넣는 방법.\n
git init 현재의 폴더를 git으로 관리하도록 등록.\n
git add 폴더 속 파일을 git으로 관리하도록 등록.\n
ㄴgit add . 모든파일 등록\n
ㄴgit add <파일명> 해당 파일을 등록\n
ㄴgit rm --cached <file> 해당 파일의 등록을 해제\n
\n
commit\n
파일을 저장 후 로컬레포지토리로 이동시키는 단계\n
git commit -m "<내용>" 해당 파일에 주석을 달아주는건가? 몰르겠음...\n
\n
로컬 파일을 github에 업로드하기\n
자신의 github에 repository 생성.\n
ㄴ이 때 repository는 git의 폴더 이름과 같게 해주면 더욱 편리함\n
repository를 생성하면 고유 주소가 만들어진다.(https://github.com/<사용자명>/<repository이름>.git)\n
로컬 repository를 github에 업로드하기 위한 명령어\n
git remote add origin <주소>\n
git branch -M main\n
git push -u origin main\n
ㄴ궁금한 점: 여기서 origin과 main이라는 단어는 어떤 경로를 만드는 대명사같음... 관리하기 쉽게 하기 위해서 저런 단어를 쓰는건가...\n
\n
git add <파일명>\n
ㄴ파일을 git에 등록\n
git commit -m "<내용>"\n
ㄴ파일을 git에 commit하기\n
git push origin main\n
ㄴ파일을 github에 업로드\n