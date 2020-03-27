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
<img width="500" alt="스크린샷 2020-03-27 오전 12 16 46" src="https://user-images.githubusercontent.com/44978839/77663626-9a383400-6fc0-11ea-9bce-473462a97b3e.png">
</p>
<h4 align="center">Repository Setting</h4>
<p align="center"> 
<img width="720" alt="스크린샷 2020-03-27 오전 12 18 36" src="https://user-images.githubusercontent.com/44978839/77663631-9c9a8e00-6fc0-11ea-849c-165abb9a5f50.png">
</p>


# 👀 Marketplace 살펴보기

* GitHub Marketplace 영상 [시청하기](https://youtu.be/_HjToekoEMk)
* GitHub Marketplace 란? [공식 문서 보기](https://developer.github.com/marketplace/)

> 깃헙 공식 문서는 다음과 같이 Marketplace 를 설명합니다.

>> GitHub Marketplace 는 GitHub 워크 플로우를 확장하고 개선하려는 개발자에게 연결합니다.  
개발자가 GitHub Marketplace 에서 사용할 무료 및 유료 도구를 나열 할 수 있습니다.  
GitHub Marketplace 는 개발자에게 GitHub 액션 및 앱이라는 두 가지 유형의 도구를 제공하며 각 도구는 GitHub Marketplace에 도구를 추가하기 위해 서로 다른 단계를 필요로합니다.

* 쉽게 말해서,  
GitHub 와 연동해서 사용할 수 있도록 개발된 써드파티의 앱이나 액션을 구매할 수 있는 서비스입니다.  
Marketplace 에서는 GitHub 기능을 확장하는 App 과 GitHub 액션에서 사용할 수 있는 Action 을 구매할 수 있습니다.

## Apps
* **Verified Apps** : 녹색 배지가 있습니다.

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
### 설치 방법
먼저 설치 방법은 굉장히 쉬웠습니다.
  1.  자신이 적용하고자 하는 projects 의 성격에 따라 **Open souce, Individual, Professional 플랜**을 선택하고 **적용할 Organization** 을 선택합니다.
  
  2. **Buy with Github** 버튼을 눌러 청구 내용을 확인한 다음 플랜에 따라 알맞은 가격을 지불하고 주문을 완료합니다.
  
  3. 이제 설치가 시작되는데, 이때 **Organization 의 모든 Repository 에 적용**할 것인지 **특정 Repository 를 선택하여 적용**할 것인지 설정합니다.
  
  4. 설치할 앱이 계정에 **접근할 수 있는 권한을 허용**한다면 설치가 완료됩니다.

### 삭제 방법
설치한 앱 확인 및 삭제하는 방법은 다음과 같습니다.
  1. 자신의 **account profile** 을 선택하고 **Settings** 로 들어갑니다.
  
  2. Personal Settings 의 많은 메뉴 중 **Applications** 를 클릭합니다.
  
  3. 해당 메뉴에서 **설치한 Github App** 과 **권한을 부여한 App** 을 확인할 수 있을 뿐만 아니라 Github 계정으로 접근했던 Applications 의 목록을 확인할 수 있습니다.

## Reviews
GitHub Marketplace 에서 사용해본 앱 중 제일 괜찮았던 앱을 추천해보겠습니다.

### [Imgbot](https://github.com/marketplace/imgbot)
<img height="100" src="https://user-images.githubusercontent.com/44978839/77730803-e2009f00-7044-11ea-9fa1-5dd230bc93a7.png"> <img height="100" src="https://user-images.githubusercontent.com/44978839/77730892-1d02d280-7045-11ea-937a-dfd8c6284c5d.png">  
* Repository( Xcode project 는 보통 Assets ) 에 있는 이미지의 품질은 유지하면서 파일 크기를 줄여 무손실 압축을 시켜주는 앱
> Imgbot 은 본인들의 툴을 사용해야하는 이유에 대해 이미지가 최적화 되어있을수록 더 빨리 로드되고, 페이지가 빠를수록 전환율이 높아지기 때문에 이탈률이 낮아지고 사용자가 더 행복해질 것이라고 어필하면서 자신들의 앱이 이 모든 것을 몇 번의 클릭만으로 가능할 수 있게 한다고 설명합니다.

> 사용 예시 : https://github.com/GoldenTicketGroup/GoldenTicket-iOS/pull/1

### [Assignee to reviewer](https://github.com/marketplace/actions/github-action-for-assignee-to-reviewer)
<img height="100" alt="스크린샷 2020-03-27 오후 5 13 01" src="https://user-images.githubusercontent.com/44978839/77735631-42480e80-704e-11ea-91ad-ff42a63fbaa6.png">  

* 유저가 assigned 되었든 unassigned 되었든 간에 Pull requests 에 대해 assigned / unassigned 이벤트를 알려주는 액션

> 팀에서 Pull requests 담당자가 있지만 Review requests 시스템으로 바꾸고 싶을 때, 모든 사람이 워크 플로우를 변경하는 건 어려울 수 있습니다. 이 GitHub Action 은 담당자를 기반으로 Review requests 을 자동으로 작성하고 삭제하여 전환을 용이하게합니다. Review requests 에 의존하는 [Pull Reminders](https://pullreminders.com/) 와 같은 타사 앱을 사용할 때 특히 유용합니다.

# 👃 Explore 살펴보기


# 👄 Repository Setting 살펴보기
