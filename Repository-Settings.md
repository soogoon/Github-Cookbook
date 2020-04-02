# 📌 Previous Contents
* 👀[Marketplace & Explore 탭 살펴보기](Github-Marketplace-Explore.md)
---
# [Repository 환경 제대로 알고 설정하기](#Repository-Setting-살펴보기)

Repository 에 들어가보면 Code 부터 Pull requests, Actions, Projects, Wiki, Security, Insights, 그리고 **Settings** 까지

8가지의 메뉴 중에서 **Settings 에서 할 수 있는 것들**에 대해 얼마나 알고 있는지 스스로 자문해봅시다.

저는 주로 Repository 의 이름을 변경하거나, 위치를 이동하거나, 삭제할 때 이외에는 잘 사용하지 않았던 것 같습니다.

이번에는 우리가 주로 사용하는 **Options Settings 이외의 다른 탭 메뉴들**에 대해서도 살펴보려고 합니다.

<h4 align="center">Repository Setting</h4>
<p align="center"> 
<img width="720" alt="스크린샷 2020-03-27 오전 12 18 36" src="https://user-images.githubusercontent.com/44978839/77663631-9c9a8e00-6fc0-11ea-849c-165abb9a5f50.png">
</p>

<h4 align="center">Setting menu</h4>

<p align="center"> 
<img width="180" alt="스크린샷 2020-03-27 오후 9 57 43" src="https://user-images.githubusercontent.com/44978839/77758280-03c64a00-7076-11ea-8b22-8045d72555bb.png">
</p>

# Repository Setting 살펴보기

## Options
### Template repository 
2019년 6월 9일자로 새로 추가된 기능인 template repository는, 설정을 체크하면 모든 파일과 폴더가 포함된 새 repository 를 생성할 수 있습니다.  
튜토리얼을 작성하거나 기업용 *boilerplate* 를 만들거나 프레임워크를 배포하고 싶을 때 유용하게 사용할 수 있습니다. 

> 사용 예시 1 : https://github.com/ttub-nii/test-template-repo

> 사용 예시 2 : https://github.com/ttub-nii/Study-Node-Server

**Fork 와 무엇이 다른가?**
Fork 와 유사하지만 매우 중요한 다른 점이 있습니다.

* fork 를 받은 repository 에는 상위 저장소의 전체 commit history 가 포함됩니다. 그러나 template 에서 작성된 repository 는 싱글 commit 로 시작합니다.

* fork 로 commit 한 내용은 contributions 그래프에 나타나지 않습니다. 그러나 template 에서 생성된 repository 에 대한 commit 은 contributions 그래프에 나타납니다.

* fork 는 기존 프로젝트에 코드를 기여하기 위한 임시적인 방법일 수 있지만 template 에서 repository 를 만들면 새 프로젝트를 빠르게 시작할 수 있습니다.

<h4 align="center">Fork commit 이 Merge 되기 전 / 후 비교</h4>

<p align="center"> 
<img width="200" alt="스크린샷 2020-04-01 오후 11 46 29" src="https://user-images.githubusercontent.com/44978839/78213863-c7b83c80-74ee-11ea-8c0c-f944be047b86.png">　 　 <img width="200" alt="스크린샷 2020-04-02 오후 1 40 17" src="https://user-images.githubusercontent.com/44978839/78213865-c8e96980-74ee-11ea-941c-fd0e55a7d557.png">
</p>

##
### Social preview
누군가가 Repository 에 링크를 걸 때 소셜 미디어 플랫폼에 표시되는 이미지를 설정할 수 있습니다.  
이미지를 추가하지 않으면 저장소 및 소유자 아바타에 대한 기본 정보가 표시됩니다. 

<h4 align="center">Social preview 적용 전 / 후 비교</h4>

<p align="center"> 
<img width="300" src="https://user-images.githubusercontent.com/44978839/77940171-3d57b900-72f3-11ea-8f82-f509072e4d76.png">   　 <img width="300" src="https://user-images.githubusercontent.com/44978839/77940175-4052a980-72f3-11ea-8d80-2bc23d207a32.png">
</p>

##
### Features
* Wikis 

  * 자신의 Repository 에 대해 documents 를 작성해서 다른 이들이 프로젝트를 사용하거나 프로젝트에 기여할 수 있도록 합니다.
  
  * 선택을 해제하면 Wiki 탭을 비활성화할 수 있습니다. 또한 Wiki 를 collaborators 에게만 수정 권한을 부여할 수 있습니다.

* Issues 

  * 사용자의 피드백을 모으거나, sw 의 버그를 report 하거나, task 를 오거나이즈 하는 데에 사용할 수 있습니다.
  
  * Issues 탭을 비활성화할 수 있고, **Set up templates** 버튼을 눌러 새 Issue 를 작성할 때 양식을 커스텀할 수 있습니다.
  
  * template 의 타입을 **Bug report, Fearture request, Custom template** 중에 선택하여 생성합니다.
  
  * 이슈 제목을 자동으로 설정하거나, repository 에 읽기 권한이 있는 사용자에게 이슈를 할당하거나, title, labels, YAML frontmatter 형식의 커스텀 라벨을 지정할 수도 있습니다.
  
<p align="center"> 
<img width="600" alt="스크린샷 2020-03-28 오후 2 21 04" src="https://user-images.githubusercontent.com/44978839/77815564-67e12080-70ff-11ea-947e-51a380c02e4f.png">
</p> 

* Sponsorships 

  * 오픈 소스 프로젝트에 가치를 기여하고 해당 repository 에 대해 스폰서 십(경제적 지원)을 받을 것인지 설정하는 부분입니다.
  
  * **Set up sponsor button** 을 누르면 오픈소스 프로젝트의 가시성을 높이기 위한 스폰서 버튼 활성화 할 수 있습니다.
  
  > TIP
  >> Github Sponsor 계정으로 등록하고 은행, 세금 정보를 제출하고 GitHub 계정에서 2 단계 인증을 활성화하면 스폰서 개발자가 될 수 있습니다.
  
* Projects

   <img width="550" alt="스크린샷 2020-03-31 오전 2 07 15" src="https://user-images.githubusercontent.com/44978839/77941038-7e040200-72f4-11ea-8126-7bf0f95b93d8.png">
   
  * 작업을 조직화, 구성하거나 우선 순위를 매길 때 유용하게 사용할 수 있는 게시판입니다.  
  
  * 특정 기능의 작업이나 포괄적인 로드맵이나, 출시 체크 리스트 등에 관한 프로젝트를 만들 수 있습니다.

   > **Projects Template 종류**
   >>   * None
   >> * Basic kanban
   >> * Automated kanban
   >> * Automated kanban with reviews
   >> * Bug triage

##
### Data services
denpendency 에서 취약성이 발견되었을 때 알림을 주는 기능입니다.  
여기서 취약성은 프로젝트 또는 해당 코드를 사용하는 다른 프로젝트의 기밀성, 무결성, 가용성을 손상시키기 위해 악용될 수 있는 프로젝트 코드의 문제입니다.  

**Security Alerts 에는 다음과 같은 내용이 포함됩니다.**

* 심각도 수준

* 프로젝트의 영향을 받는 파일에 대한 링크

* 취약점을 해결하는 자동 보안 업데이트가 포함된 Pull requests 링크

##
### Merge button
Pull request 를 merge 할 때, commit / 스쿼시 / 리베이스 중에서 어떤 조합을 허용할 것인지 설정할 수 있습니다.  
만약 protected 브랜치에서 linear history 를 활성화 한 경우에는 스쿼시나 리베이스를 허용해야 합니다.  
다음과 같은 옵션 중에서 하나 이상의 옵션은 활성화 되어 있어야 합니다.  

* Allow merge commits 

* Allow squash merging 

* Allow rebase merging 

Pull request 가 merge 된 후 헤드 브랜치를 자동으로 삭제할 수 있습니다.

* Automatically delete head branches 

##
### GitHub Pages
GitHub 저장소에서 직접 개인, organization 또는 프로젝트에 대한 웹 사이트를 호스팅 할 수 있습니다.  
GitHub의 저장소에서 HTML, CSS 및 JavaScript 파일을 직접 가져 와서 웹 사이트를 게시하는 정적 사이트 호스팅 서비스입니다.

* Source

  * default source 를 사용하면 가장 최근에 빌드된 master branch 의 내용으로 사이트가 자동으로 게시됩니다. 
  
  * 다른 브랜치나 폴더에서 프로젝트 사이트를 게시하도록 선택할 수도 있습니다.
  
* Theme Chooser

  * GitHub 페이지 사이트에 테마를 추가하여 사이트의 모양과 느낌을 사용자 정의 할 수 있습니다.
  
  * 예시 : https://ttub-nii.github.io/Github-Cookbook/

##
### Danger Zone

* 비공개 & 공개 설정

* repository 의 Owner 를 변경하거나, 위치를 이동

* repository 를 아카이빙 목적, read-only 로 사용

* repository 를 삭제 
  * ~~그러나 삭제된 repository 되돌리기는 User settings > Repositories 에서 가능합니다.~~

##
## Manage access  
team 이나 person 을 검색 & 초대할 수 있고 권한을 수정하거나 삭제할 수 있다.

## Branches
### Branch protection rules
Pull requests 가 Merge 전에 일련의 확인을 통과하도록 요구할 수 있습니다.  
예를 들어 상태 확인을 통과하지 못한 Pull requests 을 차단하거나 특정 수의 승인 검토가 있어야 병합할 수 있습니다.

**Add rules** 버튼을 눌러 다음과 같은 규칙을 부여할 수 있습니다.

> 참고 | [오지는 컴퓨터 공부 - Git에 대해 알아보자 5. GitHub 추가 기능들](https://cupjoo.tistory.com/11)

  * **Require pull request reviews before merging**
  
    * 지정된 횟수 만큼의 승인이 완료되어야 Merge가 가능합니다. 
    
    * 이 조건을 선택할 경우, 요구 승인 수를 설정할 수 있으며 또 다른 추가 선택 사항들이 나타납니다.
  
  * **Require status checks to pass before merging**
    * CI 테스트를 통해 기존 브랜치와 충돌이 없을 시에만 Merge가 가능합니다.
    
    * A 브랜치가 최신인 상태를 기준으로 해당 검사를 실시하기에, B 브랜치에서 코드를 수정하던 중 C 브랜치에 의해 A 브랜치가 업데이트 됐을 시, 새로운 A 브랜치를 B 브랜치로 Merge 시켜야 합니다.
    
  * **Require signed commits**
    * GPG key가 있어야 Merge가 가능합니다.
    
  * **Require linear history**
    * to block all merge commits from a protected branch.
    
  * **Include administrators**
    * 관리자에게도 이 모든 제약 사항을 적용하도록 하는 옵션입니다.
  
강제로 푸시하는 것을 허용하거나, 브랜치를 삭제하는 것 역시 권한을 설정할 수 있습니다.

  * **Allow force pushes**
  
  * **Allow deletions**
> 사용 예시 : https://github.com/binarysound/web-lab/issues/4

## Webhooks  
앱이 다른 앱에 실시간 정보를 제공하는 방법입니다.  
GitHub 의 특정 이벤트를 구독하는 GitHub Apps 또는 OAuth Apps 와 같은 integrations 을 설정할 수 있습니다.  
이벤트가 발생하면 Webhooks 의 URL에 HTTP 요청을 다른 애플리케이션에 주로 POST 형태의 페이로드를 보낼 것입니다.  
간단하게 요약하자면, Webhook 기능을 사용해 특정 API를 호출하는 것이 가능합니다.

> 참고 | [44bits - 깃허브 웹훅을 활용해 슬랙에 이벤트 전달하기](https://www.44bits.io/ko/post/notifying-github-event-by-using-github-webhook) | [SendGrid Team - What’s a Webhook?](https://sendgrid.com/blog/whats-webhook/)

* 유일한 단점은 처음에 설정하기가 어렵다는 것인데 Webhook 은 API와는 반대 방향으로 작동합니다.  

* Webhook 은 API 스펙에 해당하기 때문에 Webhook 을 사용하기 위해서는 API를 설계해야 합니다.

* 예를 들어 보통 API를 호출하면 어떤 정보를 되돌려줍니다만, Webhook 에 등록하면 어떤 이벤트가 발생할 때 거꾸로 깃허브에서 등록한 URL을 호출합니다. 

## Notifications
push 이벤트가 발생했을 때 설정한 이메일 주소로 알림을 받을 수 있습니다.

* Approved header

  * GitHub가 보내는 각 이메일 알림에는 헤더 정보가 포함되어 있습니다. 
  
  * 모든 이메일의 헤더 정보는 일관성이 있으므로 모든 GitHub 알림 또는 특정 유형의 GitHub 알림을 필터링하거나 전달할 수 있습니다.
  
  * 'Approved' 헤더 값을 추가하면 읽기 전용 메일을 자동으로 승인합니다.

## Integrations
설치된 Github Apps 를 확인할 수 있습니다.

> 사용 예시

<p align="center"> 
<img width="801" alt="스크린샷 2020-04-01 오후 8 23 33" src="https://user-images.githubusercontent.com/44978839/78131843-adcb1b00-7456-11ea-8ef2-679bea0d18b6.png">
</p>

## Deploy keys
repository 의 SSH 키로, repository 에 접근하는 클라이언트에게 읽기 전용 (원하는 경우 r / w) 액세스 권한을 부여합니다.  
이름에서 알 수 있듯이, 주요 기능은 읽기 접근 권한이 필요한 배포 프로세스에서 사용됩니다.  
따라서 Deploy key 를 설정하면 서버 쪽이 망가졌을 경우에 대비하여 repository 를 공격으로부터 안전하게 유지할 수 있습니다.
> 사용 방법 : https://gist.github.com/zhujunsan/a0becf82ade50ed06115

## Secrets
암호화 되어 저장되는 환경 변수로 특정 선택한 작업에만 노출됩니다.  
Repository 에 공동 작업자 액세스 권한이 있는 사람은 누구나 이러한 비밀을 사용할 수 있습니다.  
액세스 토큰과 같은 민감한 정보를 저장할 수 있고, fork 로 부터 Pull requests 한 워크 프로우에는 Secret 이 전달되지 않습니다.  

Github 공식 문서에서는 Secret 이름은 공백을 포함할 수 없고, JSON 이나 인코딩 된 Git Blob 과 같은 structured data 를 secret 값으로 저장하는 걸 지양하라고 합니다.
> 출처
>> https://help.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets

## Actions

* **local 과 third party Action 모두 허용함**
  * Action 코드가 이 repository 에 있는지, organization 에 있는지, 제 3자가 소유한 repository 에 있는지 상관 없이 모든 Action 을 실행할 수 있습니다.

* **local Action 만 허용함**
  * 해당 repository 나 organization 에 속하기만 하면 어떤 Action 이든 실행되는 것을 허용합니다.

* **Action 사용 안함**
  * 해당 repository 에서 모든 Action 을 불허합니다.

## Security Alerts (organization 에 속한 repository)
보안 경고는 관리자가 권한을 부여한 사람과 팀만 볼 수 있습니다.  
권한을 부여받으면 dependencies 중 하나에서 새로운 취약점이 발견되면 알림을 주고, 자동 업데이트한 보안 내용의 추가 세부 정보들을 볼 수 있습니다.  
각 개인은 해당 탭에서 보안 알림을 받는 방법을 관리 할 수 있습니다.

> **Choose the people or teams you would like to grant access to security alerts**
>> 보안 경고에 접근할 수 있도록 하려는 개인이나 팀을 찾아 권한을 부여합니다.

---
# Moderation
## Interaction limits
24시간 동안 repository 나 organization 의 특정 사용자가 
1. comment 를 남기거나, 
2. issues 를 열거나, 
3. Pull requests 를 작성하는 것을 제한할 수 있습니다. 

예를 들어, Github 공식 문서는
```
This may be used to force a "cool-down" period during heated discussions.
```
너무 논쟁이 과열됐을 때 이 기능을 사용하여 진정 기간을 가질 수 있다고 설명합니다.

* **Limit to existing users**
  * Users that have recently created their account will be unable to interact with the repository.

  * 24시간 이내에 계정을 만든 사용자 중에 contributions 가 없고 공동 작업자도 아닌 사용자의 활동을 제한합니다.

* **Limit to prior contributors**
  * Users that have not previously committed to the repository’s master branch will be unable to interact with the repository.
  
  * 이전에 master 브랜치에 commit 하지 않았거나 공동 작업자가 아닌 사용자의 활동을 제한합니다.

* **Limit to repository collaborators**
  * 공동 작업자가 아닌 사용자의 활동을 제한합니다.

## Reported content (organization 에 속한 repository)
collaborators 나 contributors 는 욕설 또는 파괴적인 콘텐츠를 신고할 수 있습니다.  
**Accept** 한다면 repository 관리자에게 collaborators, contributors 가 콘텐츠를 신고할 수 있는 옵션이 보여집니다.

---
### 끝! 모두 수고 많으셨습니다 :)
