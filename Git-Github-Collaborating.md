# Git의 다양한 협업 워크플로우

**Git 그 자체**를 놓고 보면, **유연성**에 초첨이 맞춰져 있다. 따라서, Git을 어떻게 사용하는지에 대해서는 **표준화 된 것이 없다**.

그래서 우리는 **Git 으로 협업을 할 때**, **일관되고 생산적인 방식**으로 작업을 하기 위하여 몇가지 **권장되는 워크플로우 방식**을 따를 수 있다.

이러한 워크플로우는 **구체적인 규칙보다는 지침 정도로만 설계**되어 있고, 우리는 프로젝트의 **다양한 측면에서 필요에 맞게 선택**할 수 있다.



# Feature Branch Workflow

- Feature Branch Workflow의 핵심 아이디어는 **모든 기능 구현을 기능(feature) 브랜치에서 작업**하는 것이다. 
- **다수의 팀 구성원**이 **메인 코드 베이스(master)를 중심**으로 해서 안전하게 **새로운 기능을 개발**할 수 있다.
- Feature Branch Workflow와 풀 리퀘스트(Pull Request)를 결합하면 팀 구성원 간에 **변경 내용에 대한 소통을 촉**진해서 **코드 품질을 높일 수 있다**.

- **소규모 인원의 프로젝트**에서 사용하는 워크플로우이다.
- 여러 워크플로우들이 Feature Branch Workflow를 기본 모델로 한다.



### 원격(remote) 저장소와, 로컬(local) 저장소

우선 Feature Branch Workflow는 중앙 원격(remote) 저장소(repository)를 기준으로 한다.

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

- 빈센트 드리센(Vincent Drissen)이 고안한 [Gitflow](https://nvie.com/posts/a-successful-git-branching-model) Workflow는 **더 큰 프로젝트를 관리하기 위해 설계**되었다.
- 프로젝트 **릴리스(release)를 중심으로 설계**된 엄격한 브랜치 모델을 정의하고 있다.
- Gitflow는 **릴리즈 사이클이 예정된 프로젝트에 이상적으로 적합**하다.
- Gitflow Workflow도 [Feature Branch Workflow](#feature-branch-workflow)와 같이 팀 구성원 간의 협업을 위해 중앙 원격 저장소를 사용한다. 즉, 로컬 브랜치에서 작업하고 중앙 원격 저장소에 푸시한다.

### git-flow 설치하기

Gitflow는 Git Workflow에 대한 추상적인 아이디어일 뿐이다. 이 개념을 툴로 만든 git의 확장 패키지인 **git-flow**가 있다. 

만약 macOS 환경이라면 `brew install git-flow` 을 통해 설치가 가능하다.(homebrew 사용 가정)

git-flow를 설치한 후에는 `git flow init`를 실행하여 프로젝트에서 사용할 수 있다. 이 명령은 `git init` 을 포함한 확장된 명령이고, 저장소에서 사용자를 위한 브랜치를 자동으로 생성해주는 것 외에는 다른 점은 없다.



### Master와 Develop 브랜치

Gitflow는 단일 마스터 브랜치 대신에 두 개의 브랜치를 사용한다.

- 마스터(master) 브랜치는 공식 릴리즈 이력을 저장한다. 즉, 실제 출시한 소프트웨어의 한 버전(version)을 의미한다.
- 개발(develop) 브랜치는 기능들의 통합 브랜치 역할을 한다. 이 브랜치를 기반으로 모든 구현이 이루어진다.

첫번째 단계는 마스터 브랜치로 부터 개발 브랜치를 생성하고 원격 저장소에 푸시하는 것에서 시작된다.

```bash
$ git branch develop
$ git push -u origin develop
```

다른 개발자들은 이제 중앙 저장소를 클론하여 로컬 저장소를 만들고 모든 브랜치를 체크아웃한다.

바로 직전에 우리는 `git-flow`에 대해 소개하였다. 방금 진행한 일련의 과정을 `git-flow` 가 도와준다.

```bash
$ git flow ini
No branches exist yet. Base branches must be created now.
Branch name for production releases: [master] 
Branch name for "next release" development: [develop] 

How to name your supporting branch prefixes?
Feature branches? [feature/] 
Release branches? [release/] 
Hotfix branches? [hotfix/] 
Support branches? [support/] 
Version tag prefix? [] 
$ git branch
* develop
 master
```



### Feature 브랜치

기능(Feature) 브랜치는  [Feature Branch Workflow](#feature-branch-workflow)와 마찬가지로 실질적인 기능 구현이 이루어진다.

가장 최신의 개발 브랜치로부터 생성되며 마스터 브랜치와는 절대로 상호작용해서는 안된다.

<img src="https://wac-cdn.atlassian.com/dam/jcr:b5259cce-6245-49f2-b89b-9871f9ee3fa4/03%20(2).svg?cdnVersion=913" alt="feature-branch" style="zoom:25%;" />

- `git-flow` 없이 생성

  ```bash
  $ git checkout develop
  $ git checkout -b feature_branch
  ```

- `git-flow` 를 이용하여 생성

  ```bash
  $ git flow feature start feature_branch
  ```

기능 구현이 완료되면 개발 브랜치로 병합한다.

- `git-flow` 없이 병합

  ```bash
  $ git checkout develop
  $ git merge feature_branch
  ```

- `git-flow` 를 이용하여 병합

  ```bash
  $ git flow feature finish feature_branch
  ```

만약, 구현이 완료된 기능 브랜치를 풀 리퀘스트를 통해 개발 브랜치에 병합하고 싶다면  [Feature Branch Workflow](#feature-branch-workflow)와 같은 방식으로 하면 된다.

### Release Branch

개발이 실제 출시를 위한 충분한 기능 구현이 완료되었다면, 개발 브랜치로 부터 릴리즈(release) 브랜치를 생성한다.

릴리즈 브랜치에서는 버그 수정, 문서 생성 및 기타 릴리즈 준비를 위한 작업들을 수행한다.

릴리즈(실제 소프트웨어의 출시)가 완료 되었다면,

- 릴리즈 브랜치는 마스터 브랜치로 병합되고 버전 번호를 태그로 부여한다.

- 또한, 개발 브랜치에도 병합이 이루어 진다.

![release](https://wac-cdn.atlassian.com/dam/jcr:a9cea7b7-23c3-41a7-a4e0-affa053d9ea7/04%20(1).svg?cdnVersion=913)

릴리즈 브랜치를 사용하면 한 팀이 현재 릴리즈 브랜치를 수정할 수 있고, 다른 팀은 다음 릴리즈의 기능을 계속 개발할 수 있다.



릴리즈 브랜치를 생성하는 작업은 간단하다. 기능 브랜치와 마찬가지로 개발 브랜치로 부터 생성하면 된다.

- `git-flow` 없이 생성

  ```bash
  $ git checkout develop
  $ git checkout -b release/0.1.0
  ```

- `git-flow` 를 이용하여 생성

  ```bash
  $ git flow release start 0.1.0
  새로 만든 'release/0.1.0' 브랜치로 전환합니다
  
  Summary of actions:
  - A new branch 'release/0.1.0' was created, based on 'develop'
  - You are now on branch 'release/0.1.0'
  
  Follow-up actions:
  - Bump the version number now!
  - Start committing last-minute fixes in preparing your release
  - When done, run:
  
       git flow release finish '0.1.0'
  ```

릴리즈가 완료 되었다면, 마스터와 개발 브랜치로 병합하고 해당 릴리즈 브랜치는 삭제된다.

릴리즈 과정에서 새롭게 수정된 사항들이 새로운 기능 구현에 필요할 수 있기때문에 다시 개발 브랜치로 병합되는 것은 중요하다.

만약, 우리의 팀이 코드 리뷰를 강조하고 있다면, 이 과정에서 풀 리퀘스트를 사용할 수 있다.

- `git-flow` 없이 릴리즈 완료

  ```bash
  $ git checkout master
  $ git merge release/0.1.0
  ```

- `git-flow` 를 이용하여 릴리즈 완료

  ```bash
  $ git flow release finish '0.1.0'
  ```

### Hotfix Branches

핫픽스(hotfix) 브랜치는 현재 릴리즈 완료되어있는 소프트웨어에서 결함이 발견되었을 시, 신속한 대응을 하기 위해 사용된다.

Gitflow 워크플로우에서 유일하게 마스터 브랜치를 기반으로 생성되는 브랜치이다.

결함 수정이 완료되었다면 즉시 개발, 마스터 브랜치로 병합되어야 하고, 마스터 브랜치는 새로운 버전 번호가 태그된다.

핫픽스 브랜치 라인을 갖추고 있는 소프트웨어는 나머지 워크플로우를 중단하거나 다음 릴리즈를 기다리지 않고 빠르게 결함을 수정할 수 있다.

![hotfix](https://wac-cdn.atlassian.com/dam/jcr:61ccc620-5249-4338-be66-94d563f2843c/05%20(2).svg?cdnVersion=913)

- `git-flow` 없이 생성

  ```bash
  $ git checkout master
  $ git checkout -b hotfix_branch
  ```

- `git-flow` 를 이용하여 생성

  ```bash
  $ git flow hotfix start hotfix_branch
  ```

릴리즈 브랜치와 마찬가지로, 핫픽스가 완료되고 나면 개발, 마스터 브랜치에 병합된다.

- `git-flow` 없이 핫픽스 완료

  ```bash
  $ git checkout master
  $ git merge hotfix_branch
  $ git checkout develop
  $ git merge hotfix_branch
  $ git branch -D hotfix_branch
  ```

- `git-flow` 를 이용하여 릴리즈 완료

  ```bash
  $ git flow hotfix finish hotfix_branch
  ```

### 요약

Gitflow의 전체 흐름을 요약하면 다음과 같다.

1. **마스터(master) 브랜치**로 부터 **개발(develop) 브랜치가 생성**된다.

2. **개발 브랜치**로 부터 **릴리즈(release) 브랜치가 생성**된다.
3. **개발 브랜치**로 부터 **기능(feature) 브랜치가 생성**된다.
4. **기능 구현이 완료**되면 **개발 브랜치로 병합**된다.

5. **릴리즈가 완료**되면 **개발, 마스터 브랜치로 병합**된다.
6. 만약 **마스터에서 결함이 발견**되면, 마스터 브랜치로 부터 **핫픽스(hotfix) 브랜치가 생성**된다.

7. **핫픽스가 완료**되면 **개발, 마스터 브랜치로 병합**된다.



# Forking Workflow

- Forking Workflow는 앞서 설명한 워크플로우와 근본적으로 다르다. 앞선 두개의 워크플로우는 중앙 원격 저장소는 하나 이고 자신의 로컬 저장소로 클론을 하여 협업을 하였다면, Forking Workflow는 **공식적으로 기준이 되는 원격 저장소와 더불어 모든 참여자가 개인 원격 저장소를 지닌다**.

- Forking Workflow의 장점은 **모든 참여자가 단일 중앙 저장소에 통합할 필요가 없다**는 것이다.
- 각각의 참여자는 **자신의 원격 저장소에 모든 변경사항을 푸시**하고, **해당 프로젝트의 관리자만이 기준 원격 저장소에 변경사항을 반영**할 수 있다.
- 이를 통해 관리자는 **공식 프로젝트 베이스에 대한 쓰기 권한을 부여하지 않고 참여자들의 변경사항을 제어**할 수 있다.
- 아주 **큰 규모의 분산된 팀(신뢰할 수 없는 제 3자를 포함)**에서도 안전하게 협업하기에 좋은 협업 방법이다.
- **오픈 소스 프로젝트에 이상적인 워크플로우**이다.

>  ### 포크(Fork) vs 클론(Clone)
>
> Forking Workflow에서 말하는 포크(fork)라는 개념은 특별한 것이 아니다. 원격 저장소를 포크한다는 것은 표준 `git clone` 명령어를 통해 이루어진다. 포크된 저장소는 일반적으로 Github, Bitbucket과 같은 서비스의 원격 저장소를 의미한다. fork된 레포지토리를 생성하기 위한 고유한 Git 명령어는 없다. 본질적으로, 클론(clone)은 저장소와 그 기록을 복사하는 것을 의미한다.
>
> ### Forking Workflow에서의 브랜치 나누기
>
> Forking Workflow에서 모든 개인 원격 저장소는 프로젝트의 다른 참여자들과 브랜치를 공유하는 편리한 방법일 뿐이다.  [Feature Branch Workflow](#feature-branch-workflow)와 [Gitflow Workflow](#gitflow-workflow) 처럼 모든 참여자가 브랜치를 사용하여 개별 기능을 분리해야 한다. 유일한 차이점은 그 브랜치들이 ''어떻게 공유되는지'' 이다.



### 중앙 원격 저장소로 부터 포크(fork)를 하여 개인 원격 저장소 생성

![fork](https://www.atlassian.com/dam/jcr:642c56e3-ddc6-43ff-ab86-c5cd845afd05/03.svg)

다른 Git Workflow와 마찬가지로, Forking Workflow도 기준이되는 원격 저장소에서 시작한다. Github이나 Bitbucket 같은 원격 저장소 호스팅 서비스에서 지원하는 포크기능으로 자신의 개인 원격 저장소를 생성한다.

### 개인의 원격 저장소를 로컬 저장소로 클론

각 참여자는 포크된 자신의 원격 저장소를 로컬저장소로 클론한다.

```bash
# Github 서비스 기준으로 한다.
$ git clone https://github.com/[유저닉네임]/Github-Cookbook.git
```

### 원격(remote) 추가

다른 워크플로우에서는 중앙 원격 저장소를 가리키는 단일 origin remote를 사용하는 반면, Forking Workflow에서는 공식 기준 원격 저장소와 참여자의 개인 원격 저장소, 각각 두 개의 remote가 필요하다.

두 개의 remote에서 최신 변경사항을 적용할 수 있지만, 일반적으로 포크된 개인 원격 저장소를 origin remote로 사용하고(이 것은 git clone을 수행할 때 자동으로 생성된다.), 공식 기준 원격 저장소를 upstream remote로 사용한다.

```bash
# 이 문서의 작성자의 원격 저장소를 기준 저장소로 한다.
$ git remote add upstream https://github.com/soogoon/Github-Cookbook.git
```



### 브랜치에서 기능 구현, 커밋, 개인 원격 저장소에 푸시하기

각 참여자의 로컬 저장소에서 다른 워크플로우와 마찬가지로 브랜치를 생성하고 코드를 편집하고 변경 사항을 커밋한다.

```bash
$ git checkout -b some-feature
# 기능 구현
$ git commit -a -m "Add first draft of some feature"
```

모든 변경 사항은 프로젝트의 기준 원격 저장소로 반영되기 전까지는 각 참여자에게만 적용되어 있을 뿐이다.

만약 다른 참여자의 기능 구현이 공식 프로젝트에 반영되었다면, 각 참여자는`git pull` 로 새로운 커밋을 적용할 수 있다.

```bash
$ git pull upstream master
```

각 참여자들은 개인 전용 기능 브랜치에서 작업을 하므로, 기능 구현의 단위는 작게, 변경사항을 병합하는 시간은 짧게 가져가는 것이 좋다.

### 풀 리퀘스트 생성

![make-pull-request](https://www.atlassian.com/dam/jcr:0de71551-5c08-4fc4-ab6d-dc8a51bfcc5a/05.svg)

한 참여자가 자신의 새로운 기능을 프로젝트에 반영하기 위해서는 두가지 작업이 필요하다.

첫번째로, 포크된 개인 원격 저장소에 변경 사항을 푸시한다. 다른 참여자들이 자신이 구현한 내용에 접근할 수 있어야 한다.

```bash
$ git push origin feature-branch
```

두번째로, 프로젝트 관리자에게 자신의 기능을 공식 코드베이스에 통합하고 싶다고 통지해야한다.

이 과정에서 Github, Bitbucket 같은 서비스는 풀 리퀘스트를 제안한다.

### 요약

Fork Workflow는 **일반적으로 오픈소스 프로젝트에 많이 사용**된다. 포크는 원격 저장소를 복사하는 `git clone` 작업이다.  Fork Workflow는 Github, Bitbucket과 같은 Git 호스팅 서비스와 함께 자주 사용된다. 

전체 흐름을 요약하면 다음과 같다.

1. https://github.com/userA/open-source-project 에서 **호스팅 되는 오픈소스 라이브러리에 컨트리뷰터로 참여**하려면,
2. **오픈소스를 포크**하여 https://github.com/yourName/open-source-project (개인 원격 저장소)를 만든다.
3. https://github.com/yourName/open-source-project에서 `git clone` 을 실행하여 로컬 저장소를 생성한다.
4. 로컬에서 새로운 기능 브랜치를 생성, 기능 구현, 커밋이 실행된다.
5. 그런 다음 **새로운 기능 브랜치를 포크된 원격 저장소에 푸시**한다.
6. Github를 사용하여 **원래의 저장소(기여하고자하는 오픈소스 라이브러리)로 새로운 브랜치에 대한 풀 리퀘스트를 생성**한다.



## 참고 문서

> - https://www.atlassian.com/git/tutorials/comparing-workflows
> - https://gmlwjd9405.github.io/2017/10/27/how-to-collaborate-on-GitHub-1.html
> - https://gmlwjd9405.github.io/2017/10/28/how-to-collaborate-on-GitHub-2.html
> - https://gmlwjd9405.github.io/2018/05/12/how-to-collaborate-on-GitHub-3.html