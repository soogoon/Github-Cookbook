# About Project Boards

Github에서 제공하는 project탭에 대해 차근차근 알아보는 시간을 가지도록 합시다!

처음 project 탭에 들어가게 되면 Project에 대한 설명이 간단하게 되어있는데요. 

<img src="https://user-images.githubusercontent.com/22820675/79424029-83529380-7ffa-11ea-9972-7a1215da484a.png" width="600">

1. 작업 정리 : 우리들의 Project Board에 issue와 pull request들을 더하고, 우선 순위대로 노트카드 안에 idea와 업무 리스트를 정리 합니다.
2. 프로젝트 계획 : "To Do" , "In Progress", "Done"와 같은 기준을 정해 작업을 상태를 정렬합니다. 
3. Workflow의 자동화 : 트리거를 설정해 프로젝트 관리 시간을 절약할 수 있습니다,
4. 진행 상황 추적 : 프로젝트에서 일어나는 모든 일을 추적할 수 있고, 마지막으로 본 이후에 어떤 일이 생겼는지 확인이 가능합니다. 
5. 상태 공유 : 카드마다 각각 고유한 URL이 있기 때문에 팀과 개별 작업을 공유하고 논의가 가능해집니다. 
6. 프로젝트 마무리 : 프로젝트를 닫고 마무리합니다.

와 같은 기능을 하는 Project에 대해 하나하나 알아가보도록 하겠습니다.

----

## Project

### project

프로젝트 보드를 만들수 있는 공간은 3군데가 있습니다.

1. User

    <img src="https://user-images.githubusercontent.com/22820675/79424027-82b9fd00-7ffa-11ea-9ebe-c6e7921567c8.png" width="600">

   사용자의 repo를 이용해 프로젝트를 생성할 수 있습니다.

2. organization

    <img src="https://user-images.githubusercontent.com/22820675/79424023-8188d000-7ffa-11ea-8cc6-a36fa2bc2784.png" width="600">

   해당 조직에 속한 repo만을 이용해 프로젝트를 생성할 수 있습니다.

3. repo

    <img src="https://user-images.githubusercontent.com/22820675/79424024-82216680-7ffa-11ea-9089-582bd453be87.png" width="600">

   repo하나로 범위가 한정되고 단일 repo에 속한 요청만을 끌어옵니다.

또한, user와 organization의 프로젝트 보드는 최대 25개의 저장소만을 연결할수가 있습니다.

---

### Board 만들기

프로젝트를 만드는 것은 생각보다 간단합니다!

이름, 설명(optional), 프로젝트의 템플릿만을 설정 하면되는데요!

템플릿에는 None, Basic kanban, Automated kanban, Automated kanban with reviews, Bug triage 5가지가 있습니다.

1. None : 말 그대로 프로젝트만 생성이 됩니다

   <img src="https://user-images.githubusercontent.com/22820675/79424016-8057a300-7ffa-11ea-926e-0ffe7b28d745.png" width="600">

   

2. Basic kanban : To Do, In Progress, Done 컬럼이 같이 생성됩니다.

   <img src="https://user-images.githubusercontent.com/22820675/79424003-7d5cb280-7ffa-11ea-8679-269cdecaa2ec.png" width="600">

3. Automated kanban : To Do, In Progress, Done 컬럼이 같이 생성됩니다. 

   <img src="https://user-images.githubusercontent.com/22820675/79423998-7c2b8580-7ffa-11ea-98b5-9b89ee143539.png" width="600">

   

4. Automated kanban with reviews : To Do, In Progress, Review In Progress, Reviewer Approved, Done 컬럼이 같이 생성됩니다.

   <img src="https://user-images.githubusercontent.com/22820675/79424032-83529380-7ffa-11ea-9fa6-fbd856de8c6d.png" width="600">

5. Bug triage : Needs triage, High priority, Low priority, Close 컬럼이 같이 생성이 됩니다.

   <img src="https://user-images.githubusercontent.com/22820675/79424005-7df54900-7ffa-11ea-877c-17d4b2d277dd.png" width="600">

기본적인 kanban에 대한 기본적인 구성은 비슷하고 자동화가 적용이 되어 있나, 리뷰를 진행하는 프로젝트의 progress에서 포함이 되어있는지에 대한 차이점이 있을 뿐입니다.  

---

### 컬럼 안에 넣기

컬럼안에 넣을수 있는 항목들은 노트, 이슈, 풀 리퀘스트 3가지 입니다. 

노트의 경우에는 

<img src="https://user-images.githubusercontent.com/22820675/79424017-80f03980-7ffa-11ea-97fe-a28eae2da1f1.png" width="300">

와 같은 방법으로 컬럼의 add 버튼을 누르고 만들면 됩니다. 

<img src="https://user-images.githubusercontent.com/22820675/79424020-8188d000-7ffa-11ea-8882-1016b7e0579d.png" width="300">

와 같은 방법으로 노트를 만들고 issue로 변환 시키는 방법도 있습니다.

<img src="https://user-images.githubusercontent.com/22820675/79424019-80f03980-7ffa-11ea-9eea-012bb931ee4c.png" width="300">

하지만 이슈에 대해서 지정해 줄수있는 것은 name과 body뿐이기 때문에 이슈를 만들때는 이슈탭에서 만드는것을 추천합니다.

<img src="https://user-images.githubusercontent.com/22820675/79424015-8057a300-7ffa-11ea-8cbd-e4fa177baaff.png" width="500">

이슈와 풀 리퀘스트의 경우에는 표시된 부분에서 원하는 프로젝트에 할당시킬 수있습니다. 그리고 할당시키는 경우에는 프로젝트에 할당되어있는 자동화 설정에 따라서 자동으로 할당이 됩니다.

---

### 자동화

자동화란 깃헙 프로젝트에서 기본적으로 제공하는 To Do, In Progress, Done 에 맞춰서 이슈, 풀 리퀘스트가 생성되거나 닫힐 경우 프로젝트 내에서 알아서 이동을 해주는 것을 의미합니다.

물론 이름을 해당하는 프리셋에 맞춰서 설정할 필요는 없고, 프리셋 하나만 할당 한 뒤에 원하는 자동화 옵션을 선택해주시면 됩니다.

<img src="![img](https://user-images.githubusercontent.com/22820675/79424033-83eb2a00-7ffa-11ea-8dab-1ba42c9af257.png)" width="500">

To do

1. Issue
   - Newly added : 새로운 이슈를 생성하고 해당 프로젝트에 설정할 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
   - Reopened : 닫혀 있던 이슈를 다시 오픈시키는 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
2. Pull request
   - Newly added : 새로운 풀 리퀘스트를 생성하고 해당 프로젝트에 설정할 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
   - Reopened : 닫혀 있던 풀 리퀘스트를 다시 오픈시키는 경우 해당 옵션을 선택한 컬럼에 할당됩니다.

<img src="https://user-images.githubusercontent.com/22820675/79424012-7fbf0c80-7ffa-11ea-971e-0db1a1f66fff.png" width="500">

1. Issue
   - Reopened : 닫혀 있던 이슈를 다시 오픈시키는 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
2. Pull request
   - Newly added : 새로운 풀 리퀘스트를 생성하고 해당 프로젝트에 설정할 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
   - Reopened : 닫혀 있던 풀 리퀘스트를 다시 오픈시키는 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
   - Approved by reviewer : 리뷰어들의 최소 승인 검토 횟수를 충족한 경우 해당 옵션을 선택한 컬럼으로 할당됩니다.
   - Pending approval by reviewer : 리뷰어들이 코드 변경을 요청하거나 최소 승인 검토 횟수를 충족하지 못한 경우 해당 옵션을 선택한 컬럼으로 할당됩니다.

<img src="https://user-images.githubusercontent.com/22820675/79424011-7f267600-7ffa-11ea-9297-6bc7ca5362e3.png" width="500">

1. Issue
   - Closed : 이슈가 닫히는 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
2. Pull request
   - Merged : 풀 리퀘스트가 머지 된 경우 해당 옵션을 선택한 컬럼에 할당됩니다.
   - Closed with unmerged commits :  경우 해당 옵션을 선택한 컬럼에 할당됩니다.
   - Approved by reviewer : 리뷰어들의 최소 승인 검토 횟수를 충족한 경우 해당 옵션을 선택한 컬럼으로 할당됩니다.
   - Pending approval by reviewer : 리뷰어들이 코드 변경을 요청하거나 최소 승인 검토 횟수를 충족하지 못한 경우 해당 옵션을 선택한 컬럼으로 할당됩니다.

해당하는 자동화 옵션들을 상황에 맞게 설정해놓으면 좀 더 편하게 사용할수있겠죠??

---

### URL 공유

프로젝트에 속한 컬럼, 카드를 URL로 공유할 수 있습니다.

<img src="https://user-images.githubusercontent.com/22820675/79424008-7e8ddf80-7ffa-11ea-8a5a-4e99f7b9e180.png" width="300"><img src="https://user-images.githubusercontent.com/22820675/79424010-7e8ddf80-7ffa-11ea-9474-bec08d4192fc.png" width="300">





----

## 참고

- [Git reference](https://help.github.com/en/github/managing-your-work-on-github/managing-project-boards)
- 오픈소스 라이브러리 [YPImagePicker](https://github.com/Yummypets/YPImagePicker/projects/2) 에서 사용하고 있는 프로젝트 사용 예시

