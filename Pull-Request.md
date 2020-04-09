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

일반적으로

### 브랜치에서 생성하기

![브랜치선택](https://user-images.githubusercontent.com/19575791/78851187-24b67400-7a54-11ea-8496-524cdb68c298.png)

풀 리퀘스트 생성 화면에서 위의 사진처럼 compare 할 브랜치를 선택할 수 있다. 원하는 브랜치를 선택하여 진행하면 된다.

![풀리퀘스트제안](https://user-images.githubusercontent.com/19575791/78851672-5aa82800-7a55-11ea-9178-e7739077ecde.png)

만약, 어떤 브랜치에서 새로운 변경사항을 푸시 했다면 깃헙은 이렇게 새롭게 생성할 풀 리퀘스트를 제안해준다. 이는 포크된 레포지토리에서 한 작업이라도 똑같이 제안된다. (다만, 포크된 원본의 레포지토리로 병합하기 위한 풀리퀘스트가 제안된다는 점이 다르다.)



새로운 풀 리퀘스트 작성을 하거나 생성을 하고나서도 오른쪽 탭을 보면 여러가지 옵션이 있는데 Reviewers, Assignees, Labels, Projects, Milestone, Linked Issues 등이 있다.

![옵션](https://user-images.githubusercontent.com/19575791/78856852-d197ed80-7a62-11ea-933d-daffd1556d93.png)

#### Reviewers

