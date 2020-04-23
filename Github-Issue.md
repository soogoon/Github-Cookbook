# Issue Traking

### Issue가 무엇인가요?

프로젝트를 진행하면서 발생하는 모든 이슈를 뜻합니다.
(버그 발생, 개발, 풀 리퀘스트 등등..)



* GitHub 공식문서 [About issues](https://help.github.com/en/github/managing-your-work-on-github/about-issues)

> Use issues to track ideas, enhancements, tasks, or bugs for work on GitHub.
>
> You can collect user feedback, report software bugs, and organize tasks you'd like to accomplish with issues in a repository.
>
> You can link a pull request to an issue to show that a fix is in progress and to automatically close the issue when someone merges the pull request.



✔️깃헙에서는 issue 기능을 통해 프로젝트에서 발생하는 모든 문제를 관리할 수 있도록 돕는다. 



### Issue 생성하기

* 이슈는 유저의 이슈 사용이 허용된 깃헙 레포지토리에서 생성할 수 있다. (이슈를 사용 안하도록 설정할 수도 있다.)
  ![레포이슈생성](/Github-Issues-Imgs/레포이슈생성.png)
  [Disabling Issues](https://help.github.com/en/github/managing-your-work-on-github/disabling-issues)

* 이슈는 현재 존재하는 풀 리퀘스트의 코드로도 생성할 수 있다.
  풀리퀘를 하고있는 파일을 View File을 한 후 코드를 선택해서 이슈를 생성할 수 있다.

  ![코드이슈생성](./Github-Issues-Imgs/코드이슈생성.png)
  [Opening an issue from code](https://help.github.com/en/github/managing-your-work-on-github/opening-an-issue-from-code)

* 또한, 하나의 이슈 또는 풀 리퀘스트의 리뷰에 있는 코멘트로부터도 바로 이슈를 생성할 수 있다.

  ![코드이슈생성](./Github-Issues-Imgs/코멘트이슈생성.png)
  [Opening an issue from a comment](https://help.github.com/en/github/managing-your-work-on-github/opening-an-issue-from-a-comment)

* 만약 업무의 우선순위와 추적을 위해 프로젝트를 사용하고 있다면, 프로젝트 보드 노트를 이슈로 바꿀 수도 있다.

  [5anniversary의 project  스터디 자료 참고](https://github.com/soogoon/Github-Cookbook/blob/master/About-Git-Project.md)
  [Adding notes to a project board](https://help.github.com/en/github/managing-your-work-on-github/adding-notes-to-a-project-board#converting-a-note-to-an-issue)



아래는 기본적인 이슈 생성 방법이다.

![기본이슈생성](./Github-Issues-Imgs/기본이슈생성.png)

이슈를 만들 Repository에서 Issue탭의 New Issue를 클릭한다.
이슈는 제목과 이슈에 대한 설명을 적을 수 있다.



![이슈리스트](./Github-Issues-Imgs/이슈리스트.png)

생성된 이슈는 리스트 형태로 관리하기 힘들어 보인다. 
이슈가 엄청 많다면? ~~특정 이슈를 찾기 힘들어질 것이다.~~



### Label 기능

✔️이러한 문제점을 개선하기 위해 우리는 **Label 기능을 사용**한다. 

**각 이슈에 대한 Labeling을 통해 이슈를 검색할 수 있고, 이슈별 주제를 구분할 수 있다.**

![라벨1](./Github-Issues-Imgs/라벨1.png)

Labels 버튼에서 새로운 라벨을 만들 수 있고, 기본으로 있는 라벨을 사용할 수도 있다. (컬러 지정도 가능)



![라벨생성](./Github-Issues-Imgs/라벨생성.png)

라벨을 커스텀하여 생성할 수 있다.



![이슈상세페이지_라벨지정](./Github-Issues-Imgs/이슈상세페이지_라벨지정.png)

![이슈상세페이지_라벨지정결과](./Github-Issues-Imgs/이슈상세페이지_라벨지정결과.png)

이슈 상세페이지에서 이슈를 생성한 라벨로 지정할 수 있다.

==라벨을 나누는 기준?==

라벨은 이슈의 우선순위, 카테고리, 다른 유용한 정보들을 나누는 기준으로 만들어야한다.
(작은 단위일수록 좋다. )



### Assignees 부여

✔️또한, 해당 이슈에 대해 Assignees(책임자)를 부여할 수 있다.

![이슈상세페이지_책임자지정](./Github-Issues-Imgs/이슈상세페이지_책임자지정.png)

![이슈상세페이지_책임자지정결과](./Github-Issues-Imgs/이슈상세페이지_책임자지정결과.png)



![이슈리스트_후](./Github-Issues-Imgs/이슈리스트_후.png)

라벨과 책임자를 부여한 후 이슈 리스트를 보면 깔끔하게 정리되어있는 것을 확인할 수 있다.
지정한 label과 assignee를 통해 Filters 란에서 필터링하여 이슈를 검색할 수 있다.



하지만, Label과 Assignee를 부여해도 <u>각 기능별 서로 유사한 이슈들이 존재</u>하며, 이와 관련된 이슈를 찾거나 해당 기능들이 얼마나 구현되어 있는지 파악하기 위해서는 <u>일일히 추적해야한다</u>.



### Milestone 설정

✔️이러한 문제점을 해결하는 기능이 **Milestone**이다. 

마일스톤은 말 그대로 이정표 역할을 하며, **이슈들을 그룹화**한다.

![마일스톤생성](./Github-Issues-Imgs/마일스톤생성.png)

![마일스톤리스트](./Github-Issues-Imgs/마일스톤리스트.png)

이슈 탭의 Milestones에서 마일스톤을 생성할 수 있다.



![이슈상세페이지_마일스톤지정](./Github-Issues-Imgs/이슈상세페이지_마일스톤지정.png)

![이슈상세페이지_마일스톤지정결과](./Github-Issues-Imgs/이슈상세페이지_마일스톤지정결과.png)

이슈 상세페이지에서 마일스톤을 지정할 수 있다.



![이슈상세페이지_클로즈](./Github-Issues-Imgs/이슈상세페이지_클로즈.png)

![이슈상세페이지_클로즈후](./Github-Issues-Imgs/이슈상세페이지_클로즈후.png)

이슈는 이슈 상세페이지에서 close와 reopen을 할 수 있고, 마일스톤으로 최대 3개의 이슈까지 묶을 수 있다.



![이슈완료후마일스톤](./Github-Issues-Imgs/이슈완료후마일스톤.png)

하나의 이슈가 완료(close)된다면 마일스톤 진행상황이 업데이트된다.

또한 이슈 페이지에서 @이름을 통해 다른 사용자를 언급할 수 있고, #num을 통해 커밋, 이슈를 참조하여 소통을 원활하게 할 수 있다.

이를 통해 연관된 이슈의 추적과 진행상황을 한 눈에 파악할 수 있다.



✔️또 다르게, 풀 리퀘스트에서 이슈를 지정할 수 있다.

![풀리퀘스트_이슈지정가능](./Github-Issues-Imgs/풀리퀘스트_이슈지정가능.png)



✔️이슈 발급부터 풀 리퀘스트까지 [참고 자료](https://www.popit.kr/github로-프로젝트-관리하기-part1-이슈-발급-부터-코드리뷰까/)
