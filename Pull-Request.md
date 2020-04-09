> Github help 문서에 있는 [Proposing changes to your work with pull requests](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests), [Reviewing changes in pull requests](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/reviewing-changes-in-pull-requests) 의 내용을 참고하여 작성하였습니다.



## 풀 리퀘스트란?

풀 리퀘스트는 깃헙으로 협업을 할 때, 레포지토리의 변경사항을 같이 작업하는 다른 사람에게 알리는 수단이다.

풀 리퀘스트가 생성되면 협업하는 사람들과 새롭게 반영할 수 있는 변경사항을 논의하고 검토할 수 있으며 변경 사항이 기본 브랜치로 병합되기 전에 수정을 거친 커밋을 추가할 수 있다.

> **Note**: 풀 리퀘스트로 작업할 때의 유의점
> - 공유 저장소 모델(여러명과 협업할 때)에서 작업하는 경우, 어떠한 주제(새로운 기능)에 맞는 브랜치를 사용하여 풀 리퀘스트를 생성하는 것이 좋다. 모든 브랜치나 커밋에서 풀 리퀘스트를 생성할 수 있지만, 제안된 변경 사항을 업데이트 해야 할 경우 브랜치를 사용하여 후속 작업을 푸시할 수 있다.
> - 풀 리퀘스트에 대한 푸시 커밋을 할 때, 강제로 푸시하면 안된다. 풀 리퀘스트가 손상 될 수도 있다.

---

### 풀 리퀘스트를 생성하자

풀 리퀘스트를 생성하여 레포지토리에 대한 변경사항을 제안하고 공동으로 작업하자. 이러한 변경은 새로운 브랜치에 적용되며 마스터 브랜치에는 완료된 작업과 승인된 작업만 포함되도록 한다. 

레포지토리에 대한 읽기 권한이 있는 모든 사용자는 풀 리퀘스트를 생성할 수 있지만 브랜치를 생성하려면 쓰기 권한이 있어야 한다. 풀 리퀘스트에 대한 새로운 브랜치를 만들고 레포지토리의 쓰기 권한이 없는 경우 레포지토리를 포크하면 된다.

기본적으로 풀 리퀘스트는 상위 레포지토리(포크한 저장소)의 마스터 브랜치를 베이스로 한다.

![브랜치선택](https://user-images.githubusercontent.com/19575791/78851187-24b67400-7a54-11ea-8496-524cdb68c298.png)

풀 리퀘스트 생성 화면에서 위의 사진처럼 compare 할 브랜치를 선택할 수 있다. 원하는 브랜치를 선택하여 진행하면 된다.

![풀리퀘스트제안](https://user-images.githubusercontent.com/19575791/78851672-5aa82800-7a55-11ea-9178-e7739077ecde.png)

만약, 어떤 브랜치에서 새로운 변경사항을 푸시 했다면 깃헙은 이렇게 새롭게 생성할 풀 리퀘스트를 제안해준다.

이는 포크된 레포지토리에서 한 작업이라도 똑같이 제안된다. (다만, 포크한 원본의 레포지토리로 병합하기 위한 풀리퀘스트가 제안된다는 점이 다르다.)

새로운 풀 리퀘스트 작성을 하거나 생성을 하고나서도 오른쪽 탭을 보면 여러가지 옵션이 있는데

Reviewers, Assignees, Labels, Projects, Milestone, Linked Issues 가 있다.

#### Reviewers 

![reviewers](https://user-images.githubusercontent.com/19575791/78857621-d8bffb00-7a64-11ea-91af-c32b671eccba.png)

리뷰어는 말그대로 이 풀 리퀘스트의 리뷰를 요청받은 사람을 의미한다. Reviewers의 톱니바퀴를 눌러보면 현재 레포지토리의 소유자, 공동작업자 또는 팀의 인원이 목록에 나타나고 리뷰를 요청할 수 있다. 뒤에서 더 자세히 다뤄보자.

- 참고 : [Requesting a pull request review](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review)

#### Assignees

![assignee](https://user-images.githubusercontent.com/19575791/78859312-ed52c200-7a69-11ea-9d90-e037f02f7187.png)

Assignee 는 담당자를 의미한다. 해당 작업을 담당하는 사람인데 이슈 또는 풀 리퀘스트에 누가 작업하고 있는지 명확하게 하는 역할이다.

- 참고 : [Assigning issues and pull requests to other GitHub users](https://help.github.com/en/github/managing-your-work-on-github/assigning-issues-and-pull-requests-to-other-github-users)

> Assignee에 대해서는 꽤나 갑론을박이 있는 것 같다.(작성자 주관적 의견) 링크된 [stackoverflow 질문](https://stackoverflow.com/questions/41087206/on-github-whats-the-difference-between-reviewer-and-assignee)에서 확인해보자.

#### Labels

![label](https://user-images.githubusercontent.com/19575791/78862938-6c002d00-7a73-11ea-8bf9-a397232a29a3.png)

label을 선택하면 특정 풀 리퀘스트가 어떠한 작업인지 명시할 수 있다. 어떤 종류의 작업인지 필터링하게 되어 직관적으로 사용할 수 있다.

- 참고 : [About labels](https://help.github.com/en/github/managing-your-work-on-github/about-labels)

#### Projects

![project](https://user-images.githubusercontent.com/19575791/78864690-1a59a180-7a77-11ea-84e9-e6a027cc54d2.png)

레포지토리에 Project가 생성되어있다면 해당 풀 리퀘스트를 특정 Project에서의 작업이란 것을 명시할 수 있다.

Project에 대한 자세한 내용은 다음 챕터에서 확인해보자.

- 참고 : [About project boards](https://help.github.com/en/github/managing-your-work-on-github/about-project-boards)

#### Milestone

![milestone](https://user-images.githubusercontent.com/19575791/78863303-360f7880-7a74-11ea-85ec-1ae0c8ab38b2.png)

마일스톤은 말 그대로 마일스톤이다(...). 마일스톤은 기한을 설정할 수 있고, 이슈와 풀 리퀘스트를 그룹화 할 수 있는데 마일스톤에 연동된 모든 이슈와 풀 리퀘스트가 성공적으로 마무리되면 마일스톤도 완료된다.

- 참고 : [About milestones](https://help.github.com/en/github/managing-your-work-on-github/about-milestones)

#### Linked issues

현재 오픈되어있는 이슈와 풀리퀘스트를 연동시키는 것이다. 해당 풀리퀘스트가 성공적으로 병합된다면 연동되어있는 이슈가 close된다. 자세한 내용은 다음 챕터에서 확인해보자.

- 참고 : [Linking a pull request to an issue](https://help.github.com/en/enterprise/2.20/user/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue)

---

위의 여러 옵션들을 설정하고 나면 커밋 메세지처럼 풀 리퀘스트의 제목과 간단한 본문을 작성할 수 있다.

![title](https://user-images.githubusercontent.com/19575791/78865057-e468ed00-7a77-11ea-94bd-bc633f529091.png)

제목은 풀 리퀘스트를 생성하려는 브랜치의 이름이나 마지막 커밋메세지로 자동 생성된다. 원하는 제목으로 바꾸면 된다.

---

### 풀 리퀘스트의 4가지 탭

이제 풀 리퀘스트가 생성되었다.

풀 리퀘스트를 생성하고 나면 총 4가지 탭이 있다.

- Conversation
- Commits
- Checks
- Files changed

#### Conversation

![conversation](https://user-images.githubusercontent.com/19575791/78868487-fb124280-7a7d-11ea-8b78-b259a2af4829.png)

풀 리퀘스트의 모든 작업들이 이 Conversation에 표기된다. 위에서 살펴본 Labels, Assignees, Projects, Milestone, Linked issues 를 설정한 경우, 새로운 커밋을 푸시한 경우, 새로운 코멘트를 작성한 경우, 풀 리퀘스트에서 가장 중요한 리뷰와 리뷰 코멘트 등 모든 내용이 시간 순서에 따라 나열된다.

#### Commits

![commits](https://user-images.githubusercontent.com/19575791/78868944-ba66f900-7a7e-11ea-86fa-fd1f5e46073f.png)

해당 풀 리퀘스트에서 해당하는 브랜치의 모든 커밋이 표기되는 곳이다. 해당 커밋을 선택하여 그 커밋에서 어떠한 코드 수정이 있었는지 확인하고 코멘트할 수 있다.

#### Checks

Checks 탭은 현재 레포지토리에 설정된 [Github Actions](https://help.github.com/en/actions)으로 할 수 있는 작업 중 하나 같은데... 여기서는 다루지 않겠다. (단호)

#### Files Changed

![files changed](https://user-images.githubusercontent.com/19575791/78869500-a66fc700-7a7f-11ea-8148-b3558bb681ee.png)

현재 풀 리퀘스트의 모든 파일의 변경사항이 한번에 나열 되는 곳이다. 이곳에서 풀 리퀘스트의 꽃이라 할 수 있는 코드 리뷰를 진행할 수 있다.

### 풀 리퀘스트에 대한 리뷰 요청하기

풀 리퀘스트 생성이 끝났다면 특정 사용자(공동 작업자 또는 원본 소스코드 관리자)에게 변경 사항에 대해 리뷰를 요청할 수 있다.

또한, 레포지토리의 소유자 또는 공동작업자는 읽기 권한을 부여받은 모든 사용자에게 풀 리퀘스트 리뷰를 할당할 수도 있다.

- 참고 : [Requesting a pull request review](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review)

리뷰가 이루어지는 과정은 아래에서 더 자세히 다루어 보자.

---

## 풀 리퀘스트 리뷰란?

리뷰에서는 공동작업자가 풀 리퀘스트에서 제안된 변경사항에 대해 의견을 나누거나, 변경사항을 승인하거나, 풀 리퀘스트가 병합되기 전에 추가 작업을 요청할 수 있다.

리뷰어는 한번에 한 파일씩 풀 리퀘스트의 변경 사항을 리뷰할 수 있다. 특정한 변경사항에 대해서 개인 코멘트를 남길 수도 있고, 파일은 리뷰하고 나서 확인했다고 표시할 수 있다. 아래 과정에서 어떻게 이루어지는지 살펴보자.

### 리뷰하기

1. 풀 리퀘스트의 **Files changed** 탭으로 들어간다.

   ![files changed tab](https://help.github.com/assets/images/help/pull_requests/pull-request-tabs-changed-files.png)

2. 코멘트를 추가할 코드 줄 위에 마우스를 놓고 파란색 + 아이콘을 누르거나, 여러 줄에 대한 코멘트를 남기고 싶다면 해당 영역을 드래그하여 추가할 수 있다.
	![add comment](https://help.github.com/assets/images/help/commits/hover-comment-icon.gif)
	
3. 코멘트를 추가한다.

  ![add commect field](https://help.github.com/assets/images/help/pull_requests/comment-field.png)

4. 만약 해당 라인의 코드를 제안하고 싶다면 `+` 버튼이나 아래 사진처럼 할 수 있다.

   ![suggestion](https://help.github.com/assets/images/help/pull_requests/suggestion-block.png)

5. 코멘트 작성을 완료하였다면, `Start a review`를 누른다.

   ![start a review](https://help.github.com/assets/images/help/pull_requests/start-a-review-button.png)
   
6. 리뷰를 제출하기 전까지는 해당 코멘트는 해당 사용자에게만 표시된다. 리뷰를 제출하기 전까지는 언제든지 보류 중인 코멘트를 편집할 수 있다.

### 해당 파일을 확인했다는 `Viewed` 누르기

파일 리뷰가 끝나고 파일을 본 것으로 표시하면 파일이 축소된다. 만약 해당 파일에 다시 변경 사항이 생긴다면 `Viewed`가 취소 된다.

![viewed](https://help.github.com/assets/images/help/pull_requests/viewed-checkbox.png)

### 리뷰 제출하기

모든 파일에 대해 리뷰가 끝났다면, 최종 리뷰를 제출하여야 한다.

1. 모든 리뷰, 피드백에 대한 요약을 입력한다.

   ![review changes](https://help.github.com/assets/images/help/pull_requests/review-summary-comment-window.png)

2. 리뷰 결과는 총 세가지 타입이 존재한다.

   ![review type](https://help.github.com/assets/images/help/pull_requests/pull-request-review-statuses.png)

   - **Comment**: 명시적으로 변경을 승인하거나 추가 변경을 요청하지 않는 일반 피드백
   - **Approve** : 피드백을 제출하고 풀 리퀘스트의 제안된 변경사항을 병합하는 경우

   - **Request changes** : 병합되기 전에 반드시 개선되어야하는 변경 사항을 새롭게 요청하는 경우

3. 리뷰를 제출한다.

### 나는 리뷰 말고 코멘트 남길래

방금 전까지 각 코드에 대한 리뷰를 남기는 과정을 확인해 보았다. 만약, 그 코드에 대한 단순 코멘트만 남기고 싶다면

![single comment](https://help.github.com/assets/images/help/commits/inline-comment.png)

이렇게 `Add single comment` 를 선택하면 된다.

**single comment** 에서는 해당 코드에 대해 다른 사용자들과 여러 의견을 나눌 수 있으며 그 의견이 해결되었다면

![resolve conversation](https://help.github.com/assets/images/help/pull_requests/conversation-with-resolve-button.png)

`Resolve conversation` 을 클릭하면 된다.

### 나는 풀 리퀘스트에 대해 코멘트 남길래

만약 해당 풀 리퀘스트에 대해 코멘트를 남기고 싶다면 **Conversation** 탭에서 남길 수 있다.

![conversation comment](https://help.github.com/assets/images/help/pull_requests/conversation.png)

이렇게 작성 한 코멘트가 시간 순으로 표기된다.

### 리뷰에 제안된 피드백이 포함되었다면?

리뷰어들은 풀 리퀘스트에 대해서 구체적인 피드백을 제시할 수 있고, 레포지토리에 대해 쓰기 권한이 있는 경우엔 직접 적용하는 것까지 가능하다. 포크에서 풀 리퀘스트가 생성되고 작성자가 관리자의 편집을 허용한 경우, 업스트림에 대한 쓰기 권한이 있는 경우 제안된 변경 사항을 적용할 수도 있다. (영어 그대로 해석했는데 말이 되게 어렵게 써져있네요...)

제안된 피드백들을 적용한 것들은 모두 단일 커밋에 통합된다. 각 변경 사항을 제안한 리뷰어는 커밋의 공동 저자가 된다. 제안된 변경 사항을 적용하는 사람은 공동 저자와 커밋의 커밋자(?)가 된다.

1. 변경 내용을 커밋에 적용하려면 `Commit suggestion` 을 누른다.

   ![commit suggestion](https://help.github.com/assets/images/help/pull_requests/commit-suggestion-button.png)

2. 제안된 변경사항에 새로운 제안을 추가하려면 `Add suggestion to batch` 를 누르고, 변경사항을 추가한다.

   ![Add suggestion](https://help.github.com/assets/images/help/pull_requests/add-suggestion-to-batch.png)

3. 제안된 변경사항을 커밋할 때, 커밋 메세지를 입력하듯이 제목과 내용을 입력할 수 있다.

   ![commit message](https://help.github.com/assets/images/help/pull_requests/suggested-change-commit-message-field.png)

4.  커밋을 한다.

   ![commit changes](https://help.github.com/assets/images/help/pull_requests/commit-changes-button.png)



## 풀 리퀘스트 마무리

기본적으로 통합하려는 HEAD 브랜치와 마스터 브랜치가 충돌하지 않는 한, 풀 리퀘스트는 언제든지 병합할 수 있다.

만약 병합 충돌이 있거나 병합하기 전에 변경 사항을 테스트하려는 경우에는 로컬에서 풀 리퀘스트를 체크아웃하고 커맨드라인을 사용하여 병합을 진행할 수 있다.

또한, 풀 리퀘스트가 병합된 후에 HEAD 브랜치를 자동으로 삭제하도록 할 수 있다.

병합하지 않으려면 풀 리퀘스트를 닫을 수도 있다.

### 풀 리퀘스트 병합하기

1. `Merge pull request` 를 눌러 병합을 진행 한다. 만약 `Merge pull request` 옵션이 표시되지 않으면 드롭다운 메뉴를 클릭하여 `Create a merge commit` 를 클릭한다.

   ![merge pull request](https://help.github.com/assets/images/help/pull_requests/pullrequest-mergebutton.png)

2. 스쿼시하여 커밋을 하나의 커밋으로 압축하려면 `Squash and merge`을 클릭한다.

   ![squash and merge](https://help.github.com/assets/images/help/pull_requests/select-squash-and-merge-from-drop-down-menu.png)

3. 커밋을 리베이스하고 병합하고 싶다면 `Rebase and merge` 를 클릭한다.

   ![Rebase and merge](https://help.github.com/assets/images/help/pull_requests/select-rebase-and-merge-from-drop-down-menu.png)

   > **Note** : 리베이스 및 병합은 항상 커밋자 정보를 업데이트하고 새로운 커밋을 생성한다.

4. 커밋 메세지 입력창이 나타나면 메세지를 입력한다.

   ![confirm merge](https://help.github.com/assets/images/help/pull_requests/merge_box/pullrequest-commitmessage.png)

### 풀 리퀘스트 닫기

풀 리퀘스트를 병합하지 않으려면 닫을 수 있다. 

> **Tips** : 만약 풀 리퀘스트의 베이스 브랜치를 잘못 선택하였다면, 풀 리퀘스트를 닫고 새로 생성하는 것이 아니라 베이스 분기를 변경할 수 있다. 참고 : [Changing the base branch of a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/changing-the-base-branch-of-a-pull-request)

풀 리퀘스트 하단의 `Close pull request` 를 클릭하여 풀 리퀘스트를 닫을 수 있다.

![closw pull request](https://help.github.com/assets/images/help/pull_requests/pullrequest-closebutton.png)

### 풀 리퀘스트 Revert 하기

풀 리퀘스트를 병합하고 나서 되돌리는 작업을 하고 싶다면 이 과정이 포함된 새로운 풀 리퀘스트가 생성된다.

> **Note** : 다음과 같은 경우 [ Git을 사용하여 수동으로 커밋을 되돌릴 수 있다](https://git-scm.com/docs/git-revert.html).
>
> - 풀 리퀘스트를 되돌리면 병합 충돌이 발생하는 경우
> - 풀 리퀘스트가 Github에서 병합되지 않고 Git 명령으로 병합된 경우

풀 리퀘스트의 맨 아래쪽의 `Revert` 를 클릭하면 된다.

![revert](https://help.github.com/assets/images/help/pull_requests/revert-pull-request-link.png)





