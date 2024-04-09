Branch 보호 규칙  
  
branch pull request기능을 아무나 사용하지 못하게 만드는 기능  
특정 branch에 push가 가능한 permission을 부여함으로써 branch를 안전하게 관리할 수 있다.  
  
git flow  
  
Branch를 관리하기 위한 전략.  
Branch의 종류: main(master), develop  
feature, release, hotfix  
  
main branch  
프로젝트 생성시 기본으로 생성되는 브랜치  
프로젝트의 본체, 병합될 때마다 새로운 버젼으로 업데이트됨.  

develop branch  
두 번째 branch  
feature branch의 기반이 됨.  
우리가 개발하는 내용을 이 곳에 저장?  
  
feature branch  
develop branch의 가지, 실질적으로 기능을 개발하는 장소  
main, master, develop, release, hotfix를 제외한 이름으로 사용할 것.  

release branch  
배포 전에 버그수정을 위한 branch  
버그수정 및 qa작업을 위한 branch이다.  
베타테스트정도로 생각하면 될 듯.  

hotfix  
배포 완료된 상황에 급하게 수정이 필요할 경우 사용한다.  
수정 및 바로 적용이 필요하기 때문에 main branch에서 분기하고,  
main develop branch에 모두 병합시킨다.  
develop가 정비고라면 hotfix는 현장 출동a/s  
  
github flow  
  
배포가 수시로 이루어지는 현재의 웹앱과는 부적합.  
main과 feature만 사용.  
항상 배포가능한 상태로 유지를 하기 때문에 main에 병합 전 충분히 test를 할 필요가 있다.  
main에서 분기하여 main으로 병합  
달리 개발전용 branch 분기점이 없기 때문에 branch에 그 이름을 잘 적어야 한다.  
바로 real time환경에 적용시키기 때문에 코드리뷰를 확실하게 해야한다.  
  

개발자로서의 Attitude  
  
convention 만들어 사용하기.  
convention이란 무엇이냐? "표준"  
SI단위계, 미터법과 같은 표준을 사용하면 정리하기가 훨씬 좋다.  
  
구글링을 꼼꼼히 하고, 스스로 정리한 포트폴리오를 만들면 좋다.  
  
public repository의 코드는 곧 내 얼굴  
돌아가기만 하는 코드보다는 꼼꼼하게 잘 설계된 코드를 만들 수 있도록 노력하자.  
  
질문의 기회가 있다면 그 기회를 잘 활용하자.