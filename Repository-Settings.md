# 📌 Previous Contents
* 👀[Marketplace & Explore 탭 살펴보기](Github-Marketplace-Explore.md)
----
* 👄[Repository 환경 제대로 알고 설정하기](#Repository-Setting-살펴보기)

Repository 에 들어가보면 Code 부터 Pull requests, Actions, Projects, Wiki, Security, Insights, 그리고 Settings 까지

8가지의 메뉴 중에서 **Settings 에서 할 수 있는 것들**에 대해 얼마나 알고 있는지 스스로 자문해봅시다.

저는 주로 Repository 의 이름을 변경하거나, 위치를 이동하거나, 삭제할 때 이외에는 잘 사용하지 않았던 것 같습니다.

이번에는 우리가 주로 사용하는 Options Settings 이외의 탭 메뉴에 대해서도 살펴보려고 합니다.

<h4 align="center">Repository Setting</h4>
<p align="center"> 
<img width="720" alt="스크린샷 2020-03-27 오전 12 18 36" src="https://user-images.githubusercontent.com/44978839/77663631-9c9a8e00-6fc0-11ea-849c-165abb9a5f50.png">
</p>

<h4 align="center">Setting menu</h4>

<p align="center"> 
<img width="180" alt="스크린샷 2020-03-27 오후 9 57 43" src="https://user-images.githubusercontent.com/44978839/77758280-03c64a00-7076-11ea-8b22-8045d72555bb.png">
</p>

# Repository Setting 살펴보기

## Options
### Template repository 
### Social preview
누군가가 Repository 에 링크를 걸 때 소셜 미디어 플랫폼에 표시되는 이미지를 설정할 수 있습니다.  
이미지를 추가하지 않으면 저장소 및 소유자 아바타에 대한 기본 정보가 표시됩니다. 

### Features
* Wikis 
* Issues 
* Get organized with issue templates
* Sponsorships 
  * 오픈소스 프로젝트의 가시성을 높이기 위한 스폰서 버튼 활성화
* Projects 
### Data services
### Merge button
* Allow merge commits 
* Allow squash merging 
* Allow rebase merging 
* Automatically delete head branches 

### GitHub Pages
* Source
* Theme Chooser

### Danger Zone
* 비공개 & 공개 설정
* repository 소유권 넘기거나 위치 이동
* Archive this repository : 아카이빙 목적, read-only 로 사용하기
* Deleting a repository : 그러나 삭제된 repository 되돌리기는 User settings > Repositories 에서 가능합니다.

## Manage access  
team 이나 person 을 검색 & 초대할 수 있고 권한을 수정하거나 삭제할 수 있다.

## Branches
### Branch protection rules
* Pull requests 가 Merge 전에 일련의 확인을 통과하도록 요구할 수 있습니다. 
예를 들어 상태 확인을 통과하지 못한 Pull requests 을 차단하거나 특정 수의 승인 검토가 있어야 병합할 수 있습니다.

* **Add rules** 버튼을 눌러 다음과 같은 규칙을 부여할 수 있습니다.

  * Require pull request reviews before merging
  
  * Require status checks to pass before merging
  
  * Require signed commits
  
  * Require linear history
    * to block all merge commits from a protected branch.
    
  * Include administrators
  
  * Allow force pushes
  
  * Allow deletions

## Webhooks
## Notifications
## Integrations & services
## Deploy keys
## Secrets
## Actions
## Interaction limits (Moderation)

> 참고 | [GitHub Help](https://help.github.com/en/github/administering-a-repository/managing-repository-settings)
