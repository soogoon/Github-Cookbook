# Git의 다양한 협업 워크플로우

Git 그 자체를 놓고 보면, 유연성에 초첨이 맞춰져 있다. 따라서, Git을 어떻게 사용하는지에 대해서는 표준화 된 것이 없다.

그래서 우리는 Git 으로 협업을 할 때, 일관되고 생산적인 방식으로 작업을 하기 위하여 몇가지 권장되는 워크플로우 방식을 따를 수 있다.

이러한 워크플로우는 구체적인 규칙보다는 지침 정도로만 설계되어 있고, 우리는 프로젝트의 다양한 측면에서 필요에 맞게 선택할 수 있다.





# Feature Branch Workflow

- Feature Branch Workflow의 핵심 아이디어는 모든 기능 구현을 전용 브랜치에서 작업하는 것이다. 
- 다수의 팀 구성원이 메인 코드 베이스(master)를 중심으로 해서 안전하게 새로운 기능을 개발할 수 있다.
- Feature Branch Workflow와 풀 리퀘스트(Pull Request)를 결합하면 팀 구성원간에 변경 내용에 대한 소통을 촉진해서 코드 품질을 높일 수 있다.

- 소규모 인원의 프로젝트에서 사용하는 워크플로우이다.
- 여러 워크플로우들이 Feature Branch Workflow를 기본 모델로 한다.



### 원격(remote) 저장소와, 로컬(local) 저장소

우선 Feature Branch Workflow는 중앙 원격 저장소(remote) 레포지토리(Repository)를 기준으로 한다.

중앙 원격 저장소를 기준으로 각자의 로컬(local) 저장소에 클론을 하여 작업을 수행한다.

```bash
# 터미널에서 자신의 원하는 디렉터리 이동한 후 아래의 명령어를 입력
# 해당 디렉터리
#    --하위--> remote repository와 동일한 이름의 디렉터리 생성
$ git clone [중앙 remote repository URL]
```

- git clone 명령은 아래의 명령들을 포함한 작업이다.

```bash
# 해당 디렉터리를 빈 Git 저장소로 만드는 작업
$ git init
# 현재 작업 중인 Git 저장소에 팀의 중앙 원격 저장소를 추가한다. 이름을 origin으로 짓고 긴 서버 주소(URL) 대신 사용한다.
$ git remote add origin [중앙 remote repository URL]
# 중앙 원격 저장소(origin)의 master 브랜치 데이터를 로컬에 가져오기만 하는 작업
$ git fetch origin master
```

### 기능 브랜치(feature branch) 생성

![new-feature](https://wac-cdn.atlassian.com/dam/jcr:223f5106-2191-4450-8916-e5c80d7d907a/02.svg?cdnVersion=912)

같은 프로젝트의 팀원들은 각자의 맡은 기능 구현에 대해 마스터 브랜치에서 작업하지 않고, 마스터 브랜치를 기준으로 한 브랜치를 만든다. 이를 Feature Branch라고 한다. 

```bash
$ git checkout -b new-feature master

# 위의 명령어는 아래의 두 명령어를 합한 것
$ git branch [branch name]
$ git checkout [branch name]
```

### 기능 구현, 커밋, 원격 저장소에 푸시(push)하기

프로젝트 요구사항에 따라 각자 정해진 기능을 해당 기능 브랜치에서 구현하고, 현재 작업 진행에 따라 커밋을 한다.

```bash
$ git status
$ git add <some-file>
$ git add .
$ git commit -m "new feature"

# 위의 과정을 아래에 명령어로 통합할 수 있다.
$ git commit -a -m "new feature"
```

<img src="https://wac-cdn.atlassian.com/dam/jcr:e2c88c1b-fb28-46a3-93be-c1c45f86bd1c/03%20(1).svg?cdnVersion=912" alt="push-origin" style="zoom: 25%;" />

기능 구현이 완료 되었다면 현재까지 진행된 모든 변경사항을 원격 저장소에 올려야한다.

다른 팀원과 협업할 때 백업 역할을 하며, 새 기능의 커밋을 볼 수 있는 접근 권한을 부여할 수 있다.

마스터 브랜치와 별개로 업데이트 되는 것이므로, 얼마든지 기능 브랜치를 올릴 수 있다.

```bash
$ git push -u origin new-feature
# -u 플래그는 해당 브랜치를 원격 추적 브랜치로 만든다.
# 이 플래그를 사용하면 해당 작업 이후부터 브랜치 이름을 명시하지 않아도 된다.
$ git push
```

### 풀 리퀘스트(Pull Request) 생성

![pull-request](https://wac-cdn.atlassian.com/dam/jcr:2119c2a3-7dff-43ad-bf98-77672d93242f/05%20(1).svg?cdnVersion=912)

자신이 새로 구현한 기능에 대해 풀 리퀘스트를 생성한다. 풀 리퀘스트를 활용하면 다른 팀원에게 자신의 구현한 기능에 대한 코멘트를 받을 수 있다. 이 과정은 협업 과정에서 아주 중요한 역할을 할 수 있다. 다른 팀원을 명시하여 풀 리퀘스트를 생성하고 해당 기능에 대해 리뷰를 요청할 수 있다. 풀 리퀘스트에 대한 자세한 고찰은 나중에 다룰 것이다.

풀 리퀘스트는 Github, Bitbucket 등의 원격 저장소 서비스를 활용해야 한다.

### 풀 리퀘스트 병합(merge)

새로운 기능 브랜치가 이상이 없다면 풀 리퀘스트를 병합한다.

- 이 때 만약 병합 충돌(merge conflict)이 생겨 자동 병합이 안된다면 해당 충돌을 반드시 해결해야 한다.

![merge](https://wac-cdn.atlassian.com/dam/jcr:09308632-38a3-4637-bba2-af2110629d56/07.svg?cdnVersion=912)

문제 없이 병합이 완료 되었다면 마스터 브랜치에 해당 기능이 반영 완료된 것이다.

이제 원격 저장소의 마스터에 생긴 변경 사항을 로컬에도 최신화해야 한다.

```bash
$ git checkout master
$ git pull origin master
```

만약 다른 팀원의 기능 브랜치에 기여를 하고 싶다면 로컬로 가져와 작업을 할 수 있다.

```bash
$ git pull origin new-feature
```

해당 작업은 여럿 충돌을 야기할 수 있기 때문에, 고려하여 작업해야 한다.






# Gitflow Workflow





# Forking Workflow

