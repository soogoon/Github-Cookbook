# 📌 사전 준비 사항
upstream 으로부터 소스코드를 동기화하기 위해 clone 한 디렉토리로 이동하여 다음과 같은 절차를 행합니다.

**1.** 현재 **프로젝트에 등록된 원격 저장소**를 확인할 수 있는 명령어입니다.
```
$ git remote -v
```
**2.** 아래와 같이 origin 저장소와 **upstream 저장소**가 모두 잘 출력되는지 확인합니다.
```
origin	https://github.com/ttub-nii/Github-Cookbook.git (fetch)
origin	https://github.com/ttub-nii/Github-Cookbook.git (push)
upstream	https://github.com/soogoon/Github-Cookbook.git (fetch)
upstream	https://github.com/soogoon/Github-Cookbook.git (push)
```
**3.** 위와 같이 나타나지 않는다면 upstream 이름으로 **원본 소스코드의 위치를 추가**합니다.
```
$ git remote add upstream https://github.com/soogoon/Github-Cookbook.git
```
**4.** fetch 명령어로 원본 소스코드의 내용을 **로컬로 내려 받습니다.**
```
$ git fetch upstream
```
**5.** 내려받은 소스코드를 내 **repository 에 merge** 합니다.
```
$ git merge upstream/master
```
**동기화가 완료되었습니다. 이제 제가 준비한 2주차 내용을 보실 수 있습니다.**

# 📌 Contents

* 👀[Marketplace 는 무엇을 가능하게 하나?](#Marketplace-살펴보기)
* 👃🏻[Explore 탭 살펴보기](#Explore-살펴보기)
* 👄[Repository 환경 제대로 알고 설정하기](#Repository-Setting-살펴보기)
----

Github 페이지를 살펴보면 생각보다 우리가 매번 쓰는 기능만 이용하고 사용하지 않는 기능이 많다는 걸 확인할 수 있습니다.  

이번 주차에서는 그동안 놓치고 있었던 부분 중에서 평소에 궁금했던 **Marketplace 와 Explore 가 어떤 기능**을 제공하는지,  

그리고 **Repository 환경을 설정**하는 옵션들에 대해 살펴보려고 합니다.

<h4 align="center">Main page tab menu</h4>

<p align="center"> 
<img width="500" alt="스크린샷 2020-03-27 오전 12 16 46" src="https://user-images.githubusercontent.com/44978839/77663626-9a383400-6fc0-11ea-9bce-473462a97b3e.png">
</p>
<h4 align="center">Repository Setting</h4>
<p align="center"> 
<img width="720" alt="스크린샷 2020-03-27 오전 12 18 36" src="https://user-images.githubusercontent.com/44978839/77663631-9c9a8e00-6fc0-11ea-849c-165abb9a5f50.png">
</p>


# Marketplace 살펴보기

* GitHub Marketplace 영상 [시청하기](https://youtu.be/_HjToekoEMk)
* GitHub Marketplace 란? [공식 문서 보기](https://developer.github.com/marketplace/)

> 깃헙 공식 문서는 다음과 같이 Marketplace 를 설명합니다.
>> GitHub Marketplace 는 당신을 GitHub 워크 플로우를 확장하고 개선하려는 개발자에게 연결시켜줍니다.  
개발자들이 GitHub Marketplace 에서 사용할 수 있도록 무료 또는 유료 도구들을 게시 할 수 있습니다.  
GitHub Marketplace 는 개발자에게 GitHub 액션 및 앱이라는 두 가지 유형의 도구를 제공하며, 각 도구를 GitHub Marketplace에 추가하기 위해선 각각 다른 단계를 필요로합니다.

* 쉽게 말해서,  
GitHub 와 연동해서 사용할 수 있도록 개발된 써드파티의 앱이나 액션을 구매할 수 있는 서비스입니다.  
Marketplace 에서는 GitHub 기능을 확장하는 App 과 GitHub 액션에서 사용할 수 있는 Action 을 구매할 수 있습니다.

## Apps
* **Verified Apps** : 녹색 배지가 있습니다. 구독 등급 별로 제공하는 서비스가 다르고, 무료 또는 유료로 결제하여 사용할 수 있습니다.

* **Unverified Apps** : 확인 된 앱에 필요한 보안, 테스트 및 확인주기를 거치지 않습니다. 목록 옆에 회색 배지가 있으며 무료 앱으로만 사용할 수 있습니다.

<p align="center"> 
<img width="650" src="https://user-images.githubusercontent.com/44978839/77667494-9eb31b80-6fc5-11ea-9e7b-636504fc3fc4.png">
</p>

## Actions
서비스 약관을 충족하는 한 누구나 GitHub Marketplace 에 액션을 게시 할 수 있습니다.  

앱과 달리 GitHub Marketplace 에 올라와있는 GitHub Actions 는 GitHub 에서 검증하지 않습니다.  

<p align="center"> 
<img width="670" src="https://user-images.githubusercontent.com/44978839/77740778-2ac15380-7057-11ea-9f7f-8d85a65d47be.png">
</p>

---
### App 설치 방법
먼저 설치 방법은 굉장히 쉬웠습니다.
  1.  자신이 적용하고자 하는 projects 의 성격에 따라 **Open souce, Individual, Professional 플랜**을 선택하고 **적용할 Organization** 을 선택합니다.
  
  2. **Buy with Github** 버튼을 눌러 청구 내용을 확인한 다음 플랜에 따라 알맞은 가격을 지불하고 주문을 완료합니다.
  
  3. 이제 설치가 시작되는데, 이때 **Organization 의 모든 Repository 에 적용**할 것인지 **특정 Repository 를 선택하여 적용**할 것인지 설정합니다.
  
  4. 설치할 앱이 계정에 **접근할 수 있는 권한을 허용**한다면 설치가 완료됩니다.

### App 삭제 방법
설치한 앱 확인 및 삭제하는 방법은 다음과 같습니다.
  1. 자신의 **account profile** 을 선택하고 **Settings** 로 들어갑니다.
  
  2. Personal Settings 의 많은 메뉴 중 **Applications** 를 클릭합니다.
  
  3. 해당 메뉴에서 **설치한 Github App** 과 **권한을 부여한 App** 을 확인할 수 있을 뿐만 아니라 Github 계정으로 접근했던 Applications 의 목록을 확인할 수 있습니다.

## Reviews
GitHub Marketplace 에서 사용해본 앱 중 제일 괜찮았던 앱을 추천해보겠습니다.

>### Apps
### [Imgbot](https://github.com/marketplace/imgbot)
<img height="100" src="https://user-images.githubusercontent.com/44978839/77730803-e2009f00-7044-11ea-9fa1-5dd230bc93a7.png"> <img height="100" src="https://user-images.githubusercontent.com/44978839/77730892-1d02d280-7045-11ea-937a-dfd8c6284c5d.png">  
* Repository( Xcode project 는 보통 Assets ) 에 있는 이미지의 품질은 유지하면서 파일 크기를 줄여 무손실 압축을 시켜주는 앱
> Imgbot 은 본인들의 툴을 사용해야하는 이유에 대해 이미지가 최적화 되어있을수록 더 빨리 로드되고, 페이지가 빠를수록 전환율이 높아지기 때문에 이탈률이 낮아지고 사용자가 더 행복해질 것이라고 어필하면서 자신들의 앱이 이 모든 것을 몇 번의 클릭만으로 가능할 수 있게 한다고 설명합니다.
>> 사용 예시 : https://github.com/GoldenTicketGroup/GoldenTicket-iOS/pull/1

### [Codacy](https://github.com/marketplace/codacy)
<img height="100" src="https://user-images.githubusercontent.com/44978839/78118368-e280a780-7441-11ea-96fa-0122c4ae4055.png"> <img height="100" src="https://user-images.githubusercontent.com/44978839/78118476-06dc8400-7442-11ea-8a06-3c096640c1b3.png">

* Codacy 는 자동으로 코드를 분석하여 품질 관리를 해주는 도구로 개발자가 더 나은 소프트웨어를 더 빨리 제공할 수 있도록 도와주는 앱
> Codacy 를 사용하면 모든 commit 과 Pull requests 마다 static 분석, 순환 복잡도, duplication, 코드 unit 테스트 커버리지 변화를 확인할 수 있습니다. 코드 퀄리티를 향상시키고, 코드 리뷰 하는 데에 시간을 절약하고, 보안을 강화하고, 개발자들이 빠르게 온보딩할 수 있도록 합니다.
>> 사용 예시 : https://app.codacy.com/gh/GoldenTicketGroup/GoldenTicket-iOS/dashboard

---
>### Actions
### [Assignee to reviewer](https://github.com/marketplace/actions/github-action-for-assignee-to-reviewer)
<img height="100" alt="스크린샷 2020-03-27 오후 5 13 01" src="https://user-images.githubusercontent.com/44978839/77735631-42480e80-704e-11ea-91ad-ff42a63fbaa6.png">  

* 유저가 assigned 되었든 unassigned 되었든 간에 Pull requests 에 대해 assigned / unassigned 이벤트를 알려주는 액션

> 팀에서 Pull requests 담당자가 있지만 Review requests 시스템으로 바꾸고 싶을 때, 모든 사람이 워크 플로우를 변경하는 건 어려울 수 있습니다. 이 GitHub Action 은 담당자를 기반으로 Review requests 을 자동으로 작성하고 삭제하여 전환을 용이하게합니다. Review requests 에 의존하는 [Pull Reminders](https://pullreminders.com/) 와 같은 타사 앱을 사용할 때 특히 유용합니다.

# Explore 살펴보기
**Get email updates** 버튼을 누르면 이메일로 뉴스레터를 구독할 수 있습니다.
<h4 align="center">Explore 탭에 들어갔을 때 보이는 상세 메뉴</h4>
<p align="center"> 
<img width="600" alt="스크린샷 2020-03-27 오후 6 58 22" src="https://user-images.githubusercontent.com/44978839/77744422-f81a5980-705c-11ea-8c84-8d66d4a760d2.png">
</p>

### Explore 
* 들어가면 가장 먼저 보이는 Explore 페이지에는 사용자가 관심있어 할 만한 소식을 보여주는 뷰가 가장 크게 자리잡고 있습니다. 소식들을 보여주는 기준에는 다음과 같은 항목들이 있습니다.

  * **repositories you’ve viewed**

  * **people you follow**

  * **topics you've starred**

  * **recommended by GitHub** (App, Upcoming event, Collection)

* 가장 좌측에서는 사용자 프로필과 함께 사용자가 starred 한 topics 와 repositories 를 한번에 모아볼 수 있는 리스트가 있습니다.

* 가장 우측에서는 오늘 하루동안 가장 스타를 많이 받은 repositories 와 스타를 많이 받은 repository 를 소유하고 있는 핫한 개발자를 소개합니다. 이것은 Trending 탭과도 연결되며, 해당 탭에서 보다 자세한 필터링을 할 수 있습니다.

### Topics 
  * 프로그래밍 언어부터 테크닉, 개발 트랜드, 디자인 툴, 개발 환경, IDE, 라이브러리, 서비스까지 GitHub 에서 핫한 주제를 스타하여 소식을 받아볼 수 있습니다.

### Trending 
* 앞서 언급했던 Explore 메인 페이지 우측에 있는 탭과도 연결되는 부분으로 보다 상세한 필터링을 하여 관심 Repository 나 개발자를 팔로우할 수 있습니다.

* **Spoken Language, Language, Date range(오늘, 이번주, 이번달)** 와 같은 필터가 있습니다.

* 여기서 Spoken Language 는 사용자의 **Personal Setting** 에서 Profile 설정에 있는 **Trend setting** 과 연결되는 부분으로, 필터를 변경하고 싶다면 프로필 설정에서 변경하여 적용할 수 있습니다. 
 
 <h4 align="center">Profile 클릭 > Settings > Personal Settings > Profile > Trending settings</h4>
<p align="center"> 
 <img width="650" alt="스크린샷 2020-03-27 오후 7 18 13" src="https://user-images.githubusercontent.com/44978839/77746175-df5f7300-705f-11ea-9de0-ad4ca8452e10.png">
</p>

### Collections 
* 급성장하는 산업, 주제 및 커뮤니티 목록과 인사이트를 선별하여 보여줍니다.

* 해시태그로 분류된 카테고리에 들어가면 해당 콜렉션과 관련된 Repository 및 라이브러리를 볼 수 있습니다.

* 사용자가 직접 자신이 관심있는 주제에 대해 새로운 콜렉션을 생성할 수도 있습니다.

  * **새 콜렉션을 만들 시 유의 사항**
  
    * GitHub 커뮤니티에 콘텐츠를 제안할 때는 특정 사례를 제공하는 대신 다른 사람에게도 광범위하게 적용될 수 있는 주제이거나 현재 중요한 정보가 부족한 주제와 같이 가치있는 주제를 고려해야합니다.
    
    * 새로운 주제 또는 컬렉션을 제안하려면 추가 사항을 Pull requests 합니다. API 문서 및 스타일 가이드는 포함해야하는 정보와 양식에 대한 가이드라인을 제공합니다.
    
    * 이 저장소에는 추가 context 가 없는 가장 많이 사용되는 GitHub 주제 목록이 포함되어 있습니다. 풀 요청이 이러한 주제 중 하나를 추가하는 경우 주제가 선택 (완료 표시)되도록 주제 -todo.md를 업데이트하십시오.
    
    * 풀 요청 템플릿을 완전히 작성하십시오. 템플릿을 작성하지 않으면 풀 요청이 종료됩니다.
    
    * 모든 제안은 GitHub의 커뮤니티 지침 및 서비스 약관을 준수해야합니다. 당사의 서비스 약관에 따라 귀하는 귀하가 제공 한 컨텐츠에 대한 책임이 있으며 이를 사용할 권리가 있습니다.


### Events
* GitHub community 와 함께 전 세계에서 열리는 컨퍼런스, 밋업, 그리고 해커톤에 참가할 수 있습니다.
* 2020년 3월 5일 00시 01분부터 31일 23시 59분까지, 4주간 original GitHub Actions 을 구현하는 해커톤이 열렸었습니다.
* 보너스로 선착순 1,000 개의 유효한 제출물은 무료 GitHub 사용권을 받습니다!
<p align="center"> 
<img width="800" alt="스크린샷 2020-03-27 오전 1 35 26" src="https://user-images.githubusercontent.com/44978839/77756339-50a82180-7072-11ea-8794-d9e67f072fa2.png">  
  <img width="800" alt="스크린샷 2020-03-27 오후 9 36 28" src="https://user-images.githubusercontent.com/44978839/77756703-0c695100-7073-11ea-9e24-127402b4505a.png">

</p>

### GitHub Sponsors
오픈소스를 개발하여 GitbHub 에 공여한 contributors 를 계속해서 Refresh 하여 찾아볼 수 있습니다.

# Repository Setting 살펴보기
앞의 내용과 구분하기 위해 따로 작성하여 업로드 하겠습니다. [다음 목차로 이동]()하고 싶다면
