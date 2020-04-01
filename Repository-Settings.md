# 📌 Previous Contents
* 👀[Marketplace & Explore 탭 살펴보기](Github-Marketplace-Explore.md)
----
* 👄[Repository 환경 제대로 알고 설정하기](#Repository-Setting-살펴보기)

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
> 사용 예시 : https://github.com/ttub-nii/test-template-repo
> 적용 사례 : https://github.com/ttub-nii/Study-Node-Server

**Fork 와 무엇이 다른가?**
Fork 와 유사하지만 매우 중요한 다른 점이 있습니다.

* fork 를 받은 repository 에는 상위 저장소의 전체 commit history 가 포함됩니다. 그러나 template 에서 작성된 repository 는 싱글 commit 로 시작합니다.

* fork 로 commit 한 내용은 contributions 그래프에 나타나지 않습니다. 그러나 template 에서 생성된 repository 에 대한 commit 은 contributions 그래프에 나타납니다.

* fork 는 기존 프로젝트에 코드를 기여하기 위한 임시적인 방법일 수 있지만 template 에서 repository 를 만들면 새 프로젝트를 빠르게 시작할 수 있습니다.

##
### Social preview
누군가가 Repository 에 링크를 걸 때 소셜 미디어 플랫폼에 표시되는 이미지를 설정할 수 있습니다.  
이미지를 추가하지 않으면 저장소 및 소유자 아바타에 대한 기본 정보가 표시됩니다. 

**Social preview 적용 전 / 후 비교**

<img width="350" src="https://user-images.githubusercontent.com/44978839/77940171-3d57b900-72f3-11ea-8f82-f509072e4d76.png">  <img width="350" src="https://user-images.githubusercontent.com/44978839/77940175-4052a980-72f3-11ea-8d80-2bc23d207a32.png">

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
  
  > 참고
  >> Github Sponsor 계정으로 등록하고 은행, 세금 정보를 제출하고 GitHub 계정에서 2 단계 인증을 활성화하면 스폰서 개발자가 될 수 있습니다.
  
* Projects

  * 작업을 조직화, 구성하거나 우선 순위를 매길 때 유용하게 사용할 수 있는 게시판입니다.  
  
  * 특정 기능의 작업이나 포괄적인 로드맵이나, 출시 체크 리스트 등에 관한 프로젝트를 만들 수 있습니다.

   <img width="550" alt="스크린샷 2020-03-31 오전 2 07 15" src="https://user-images.githubusercontent.com/44978839/77941038-7e040200-72f4-11ea-8126-7bf0f95b93d8.png">

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
GitHub 의 특정 이벤트를 구독하는 GitHub Apps 또는 OAuth Apps 와 같은 integrations 을 설정할 수 있습니다.
이벤트가 발생하면 Webhooks 의 URL에 HTTP POST 페이로드를 보냅니다. 웹 후크를 사용하여 외부 이슈 트래커를 업데이트하거나, CI 빌드를 트리거하거나 백업 미러를 업데이트하거나 프로덕션 서버에 배포할 수 있습니다.

## Notifications
push 이벤트가 발생했을 때 설정한 이메일 주소로 알림을 받을 수 있습니다.

* Approved header

  * GitHub가 보내는 각 이메일 알림에는 헤더 정보가 포함되어 있습니다. 모든 이메일의 헤더 정보는 일관성이 있으므로 모든 GitHub 알림 또는 특정 유형의 GitHub 알림을 필터링하거나 전달할 수 있습니다.

## Integrations & services
## Deploy keys
## Secrets
## Actions
## Interaction limits (Moderation)

> 참고 | [GitHub Help](https://help.github.com/en/github/administering-a-repository/managing-repository-settings)
