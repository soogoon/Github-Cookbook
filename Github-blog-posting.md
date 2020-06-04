**[깃허브에 개인 블로그 만들기]**

* GitHub Pages 알아보기

  - GitHub Pages : 저장소에 홈페이지 파일을 올린 뒤 저장소의 주소를 그래로 홈페이지 주소로 사용할 수 있는 기능

  - 장점 : 깃허브 저장소를 웹 서버처럼 활용 가능하기 때문에 무료로 깃허브의 저장소를 블로그나 홈페이지 공간으로 사용 가능
  - 정적인 페이지(ex) 포트폴리오 사이트, 기술 정보를 정리하는 블로그 등)를 제공할 때 사용하기 좋음!
  - .github.io 라는 이름이 붙음 -> 국내의 한 기업에서 GitHub Pages를 통해 운영하는 기술 블로그
  - 반응형 웹 디자인을 만드는 Bootstrap 오픈 소스의 사이트 (https://getbootstrap.com/) -> GitHub Pages를 사요해 만든 홈페이지
  - ![image-20200604162835232](https://user-images.githubusercontent.com/19575791/83743888-50da2400-a696-11ea-8066-48015cabd519.png)

* GitHub Pages를 사용하는 2가지 방법

  1. 홈페이지 파일이 있는 경우:

     HTML과 CSS, Javascript(또는 jQuery) 등 홈페이지 파일이 있는 경우 -> 직접 준비한 파일을 바로 깃허브 저장소에 올리고 GitHub Pages 기능을 사용해 홈페이지를 열면 됨

  2. 홈페이지 파일이 없는 경우:

     **깃허브에서 지원하는 지킬 테마(Jekyll theme)를 가져다가 사용하는 방법**

* 1. 홈페이지 파일이 있을 때 GitHub Pages 사용하기

     -> 추후 준비 예정!

* 2. 홈페이지 파일이 없을 때 GitHub Pages 사용하기	

     * 지킬 테마(Jekyll theme) : GitHub Pages로 블로그나 사이트를 열 때 쓸 수 있는 디자인과 스타일 모음

       https://jekyllrb-ko.github.io/

       (깃허브에 가입 되어 있다는 전제하에 진행!

       포스팅은 윈도우 기준!)

       1) http://jekyllthemes.org/ 에 들어가기 또는 깃허브에 직접 jekyll을 검색해서 사용해도 됨!

       ![image-20200604171142222](https://user-images.githubusercontent.com/19575791/83743986-6e0ef280-a696-11ea-834d-fad16af2913f.png)

       2) 원하는 테마 고르기-> Homepage 버튼 누르기

       ![image-20200604171442912](https://user-images.githubusercontent.com/19575791/83744030-7d8e3b80-a696-11ea-833d-49234c7bb147.png)

       3) Fork버튼을 누르고 추가하고 싶은 자신의 저장소로 포크![image-20200604171856927](https://user-images.githubusercontent.com/19575791/83744073-8aab2a80-a696-11ea-83a7-5cda1ba7759c.png)

       ![image-20200604172217750](https://user-images.githubusercontent.com/19575791/83744101-95fe5600-a696-11ea-918e-ffd432498ce5.png)

       4) Settings에 들어가서 다음과 같이 변경 ->

       계정을 Repository name에 똑같이 적은 뒤

       **계정.github.io** 이렇게 입력!(**중요! 도메인은 꼭 이렇게 해야함!** 원하는 도메인 명이 있다면 그 도메인을 사야함! )

       우측의 Rename버튼 누르기

       ![image-20200604173928415](https://user-images.githubusercontent.com/19575791/83744101-95fe5600-a696-11ea-918e-ffd432498ce5.png)

       5) Settings를 눌러서 나온 화면에서 스크롤을 내리면 GitHub Pages에서 초록색으로 경로가 나올 경우 블로그 개설이 완료됬다는 증거!

       6) 저장소에 있는 파일 목록 중에 ''_config.yml' 파일 선택하여 환경에 맞게 수정하기

       7) 각 항목마다 주석이 남겨져 있으니 이 내용을 참고 하여 자신과 맞게 수정하기

       항목들 중에서 name과 description, footer links의 url등 다양한 부분을 수정하기

       수정한 후에는 간단한 커밋 메시지와 함께 [Commit]을 눌러 커밋하기

       8) 완성

     * [준비중...]

       1. 새 저장소 (repository) 만들기

          -계정.github.io가 붙은 이름으로 짓기->도메인

          -프로젝트 별 페이지 만들기 : 계정.github.io/projectname의 url로 접속

       2. 마음에 드는 Jekyll 테마 찾기

       3. _config.yml 파일 가져오기 : Jekyll 사이트가 갖고 있는 설정 파일

          -자신의 레포지토리에 똑같이 _config.yml이라는 이름의 파일을 만들고 Raw를 눌러서 복사한 내용을 붙여넣기

          -한 줄 추가하고 두 줄 변경 :

          [한 줄 추가]

          ```
          remote_theme : mmistakes/minimal-mistakes
          ```

           :remote_theme을 지정하는 설정이며 GitHub의 `OWNER/REPOSITORY` 의 형식

          ->mmistakes라는 owner의 minimal-mistakes라는 저장소의 Jekyll 테마를 가져오겠다는 뜻

          [두 줄 변경]

          ```
          url                      : "https://yourname.github.io" # the base hostname & protocol for your site e.g. "https://mmistakes.github.io"
          baseurl                  : "" # the subpath of your site, e.g. "/blog"
          ```

          

        * 블로그에 포스트 작성하기

          *  블로그 포스트는 _posts디렉터리에 저장됨

          * _posts 디렉터리의 기본 포스트 파일은 '20xx-x-x-파일 이름.md' 형식을 사용

          * 포스트는 마크다운 문법을 사용해 작성

            1) 기본 포스트 파일 '20xx-x-x-Hello-World.md'를 누르기

            2) 포스트 형식

            	- ---부터 ---까지는 모든 포스트에 꼭 들어가야할 내용
            	- layout:post는 수정 X
            	- title부분은 포스트 제목->포스트 작성할 때마다 수정
            	- 새 포스트 사용하기 위해서는 ---부터 ---까지 선택한 후 복사

            3) _posts디렉터리에서 [Create new file]을 누르기

            파일 이름: '2020-06-04-first.md'처럼 오늘 날짜와 파일 이름, 확장자 .md를 입력

            복사했던 내용을 붙여 넣기

            title: 포스트 제목

            원하는 내용 입력하기 후 [commit new file]을 누른 후 커밋하기

            4) _posts 디렉터리에 방금 만든 포스트 파일이 나타남

        **https://dreamgonfly.github.io/2018/01/27/jekyll-remote-theme.html**

        

        

        

        

        



