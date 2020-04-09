> Github help 문서에 있는 [Proposing changes to your work with pull requests](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests), [Reviewing changes in pull requests](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/reviewing-changes-in-pull-requests) 의 내용을 참고하여 작성하였습니다.



## 풀 리퀘스트란?

풀 리퀘스트는 깃헙으로 협업을 할 때, 레포지토리의 변경사항을 같이 작업하는 다른 사람에게 알리는 수단이다.

풀 리퀘스트가 생성되면 협업하는 사람들과 새롭게 반영할 수 있는 변경사항을 논의하고 검토할 수 있으며 변경 사항이 기본 브랜치로 병합되기 전에 수정을 거친 커밋을 추가할 수 있다.

---

**Note**: 풀 리퀘스트로 작업할때의 유의점

- 공유 저장소 모델(여러명과 협업할 때)에서 작업하는 경우, 어떠한 주제(새로운 기능)에 맞는 브랜치를 사용하여 풀 리퀘스트를 생성하는 것이 좋다. 모든 브랜치나 커밋에서 풀 리퀘스트를 생성할 수 있지만, 제안된 변경 사항을 업데이트 해야 할 경우 브랜치를 사용하여 후속 작업을 푸시할 수 있다.
- 풀 리퀘스트에 대한 푸시 커밋을 할 때, 강제로 푸시하면 안된다. 풀 리퀘스트가 손상 될 수도 있다.

---

## 풀 리퀘스트를 생성하자

풀 리퀘스트를 생성하여 레포지토리에 대한 변경사항을 제안하고 공동으로 작업하자. 이러한 변경은 새로운 브랜치에 적용되며 마스터 브랜치에는 완료된 작업과 승인된 작업만 포함되도록 한다. 

레포지토리에 대한 읽기 권한이 있는 모든 사용자는 풀 리퀘스트를 생성할 수 있지만 브랜치를 생성하려면 쓰기 권한이 있어야 한다. 풀 리퀘스트에 대한 새로운 브랜치를 만들고 레포지토리의 쓰기 권한이 없는 경우 레포지토리를 포크하면 된다.

기본적으로 풀 리퀘스트는 상위 레포지토리(포크한 저장소)의 마스터 브랜치를 베이스로 한다.

![브랜치선택](https://user-images.githubusercontent.com/19575791/78851187-24b67400-7a54-11ea-8496-524cdb68c298.png)

풀 리퀘스트 생성 화면에서 위의 사진처럼 compare 할 브랜치를 선택할 수 있다. 원하는 브랜치를 선택하여 진행하면 된다.

![풀리퀘스트제안](https://user-images.githubusercontent.com/19575791/78851672-5aa82800-7a55-11ea-9178-e7739077ecde.png)

만약, 어떤 브랜치에서 새로운 변경사항을 푸시 했다면 깃헙은 이렇게 새롭게 생성할 풀 리퀘스트를 제안해준다.

이는 포크된 레포지토리에서 한 작업이라도 똑같이 제안된다. (다만, 포크한 원본의 레포지토리로 병합하기 위한 풀리퀘스트가 제안된다는 점이 다르다.)

새로운 풀 리퀘스트 작성을 하거나 생성을 하고나서도 오른쪽 탭을 보면 여러가지 옵션이 있는데

Reviewers, Assignees, Labels, Projects, Milestone, Linked Issues 등이 있다.

#### Reviewers 

<img src="https://user-images.githubusercontent.com/19575791/78857621-d8bffb00-7a64-11ea-91af-c32b671eccba.png" width="300" align=left>

리뷰어는 말그대로 이 풀 리퀘스트의 리뷰를 요청받은 사람을 의미한다. Reviewers의 톱니바퀴를 눌러보면 현재 레포지토리의 소유자, 공동작업자 또는 팀의 인원이 목록에 나타나고 리뷰를 요청할 수 있다. 뒤에서 더 자세히 다뤄보자.

- 참고 : [Requesting a pull request review](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review)

#### Assignees

<img src="https://user-images.githubusercontent.com/19575791/78859312-ed52c200-7a69-11ea-9d90-e037f02f7187.png" width="300" align=left>

Assignee 는 담당자를 의미한다. 해당 작업을 담당하는 사람인데 이슈 또는 풀 리퀘스트에 누가 작업하고 있는지 명확하게 하는 역할이다.

- 참고 : [Assigning issues and pull requests to other GitHub users](https://help.github.com/en/github/managing-your-work-on-github/assigning-issues-and-pull-requests-to-other-github-users)

Assignee에 대해서는 꽤나 갑론을박이 있는 것 같다.(작성자 주관적 의견) 링크된 [stackoverflow 질문](https://stackoverflow.com/questions/41087206/on-github-whats-the-difference-between-reviewer-and-assignee)에서 확인해보자.

#### Labels

<img src="https://user-images.githubusercontent.com/19575791/78862938-6c002d00-7a73-11ea-8bf9-a397232a29a3.png" width="300" align=left>

label을 선택하면 특정 풀 리퀘스트가 어떠한 작업인지 명시할 수 있다. 어떤 종류의 작업인지 필터링하게 되어 직관적으로 사용할 수 있다.

- 참고 : [About labels](https://help.github.com/en/github/managing-your-work-on-github/about-labels)

#### Projects

<img src="https://user-images.githubusercontent.com/19575791/78864690-1a59a180-7a77-11ea-84e9-e6a027cc54d2.png" width="300" align=left>

레포지토리에 Project가 생성되어있다면 해당 풀 리퀘스트를 특정 Project에서의 작업이란 것을 명시할 수 있다.

#### Milestone

<img src="https://user-images.githubusercontent.com/19575791/78863303-360f7880-7a74-11ea-85ec-1ae0c8ab38b2.png" width="300" align=left>

마일스톤은 말 그대로 마일스톤이다 (...)

#### Linked issues

현재 오픈되어있는 이슈와 풀리퀘스트를 연동시키는 것이다. 해당 풀리퀘스트가 성공적으로 병합된다면 연동되어있는 이슈가 close된다. 자세한 내용은 다음 챕터에서 확인해보자.

- 참고 : [Linking a pull request to an issue](https://help.github.com/en/enterprise/2.20/user/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue)



위의 여러 옵션들을 설정하고 나면 커밋 메세지처럼 풀 리퀘스트의 제목과 간단한 본문을 작성할 수 있다.

<img src="https://user-images.githubusercontent.com/19575791/78865057-e468ed00-7a77-11ea-94bd-bc633f529091.png" align=left>

제목은 풀 리퀘스트를 생성하려는 브랜치의 마지막 커밋메세지로 자동 생성된다. 원하는 제목으로 바꾸면 된다.

<img src="https://user-images.githubusercontent.com/19575791/78865277-40337600-7a78-11ea-9717-0a36bab3bc01.png" align=left>

Create pull request 버튼의 화살표를 누르게 되면 두가지 옵션이 뜨는데 하나는 그대로 풀 리퀘스트를 생성하는 것이다.

Create draft pull request 

#### Conversation



#### Commits



#### Checks



#### Files Changed





