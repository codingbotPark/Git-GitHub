> **패스트캠퍼스 Git & GitHub - 진유림 강사** 를 참고

# Git & GitHub

현대 팀 프로젝트에서 **버전관리**와 **클라우드 저장소**는 필수적인 기술이다  

<a href = "https://ko.wikipedia.org/wiki/%EA%B9%83_(%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4)" target = "_blank" title = "참고자료">Git</a> 으로 버전관리를 할 수 있다  
<a href = "https://namu.wiki/w/GitHub" target = "_blank" title = "참고자료">GitHub</a> 는 클라우드 저장소이다  


<br>

# ch1. Git 과 버전관리

## 버전관리
원하는 지점마다 깃발을 꽂고(버전을 만들고) 이것들을 자유롭게 사용할 수 있다   
동료가 만든 버전으로 이동할 수 있고 버전들을 비교해서 최신본으로 업데이트를 할 수 있다  

<br>

## Git을 쓰려면 필요한 것
저장할 공간만 있다면 어디서나 사용이 가능하다
* 개인 컴퓨터
* USB
* 회사서버
* 클라우드 (GitHub, BitBucket, GitLab 등)

<br>

## Git을 사용하는 두 가지 방법
* CLI(Command Line Interface)
커맨드 창에 명령어를 친다
* GUI(Graphic User Interface)
버튼을 눌러 우리가 원하는 명령을 수행한다

CLI에 명령어를 쳐서 작동하는게 일반적이다  
이 것을 조금더 편하고 가시적으로 하기 위해 GUI가 

CLI는 Git이 제공하는 모든 기능을 사용할 수 있다 

<br>

## GitHub에 코드를 올리는 과정
1. 프로젝트 폴더에 이곳에 Git을 사용할 것을 명령 (git init)
1. 코딩
1. 내가 변경한파일 중 올리길 원하는 것만 선택 (git add)
1. 선택한 파일들을 한 덩이로 만들고 설명 적어주기 (git commit -m "설명")
1. GitHub 사이트에서 프로젝트 저장소 만들기 
1. 내 컴퓨터 프로젝트 폴더에 GitHub 저장소 주소 알려주기 (git remote add)
1. 내 컴퓨터에 만들었던 덩어리 GitHub에 올리기 (git push)

<br>

## Git & GitHub 환경 설정
### Git 설치
1. 명령 프롬프트에 `git` 을입력해서 내 컴퓨터에 Git이 설치되어 있는지 확인
1. 명령어에 대한 안내가 나오지 않으면  <a href = "https://git-scm.com/downloads" target = "_blank" title = "참고자료">Git 설치</a>
(설치할 때 Git Bash는 꼭 설치한다)

### Visual Studio Code 설치
Microsoft에서 제작한 무료 코드 에디터이다  
문법 강조, 코드 자동 완성, Git 연동 등 유용한 기능도 많고 오픈소스이다  

<a href = "https://code.visualstudio.com/download" target = "_blank" title = "참고자료">Visual Studio Code 설치</a>

### GitHub 가입
Git으로 버전 관리한 코드를 올릴 수 있는 클라우드 서버

<a href = "https://github.com/" target = "_blank" title = "참고자료">GitHub 가입</a>

Git 호스팅 사이트 | 모기업 | 특징 | 가격
:---:|:---:|---|---
GitHub|GitHub Inc(Microsoft에서 인수)|최대 규모의 Git 호스팅 사이트 | 공개 저장소 생성 무료, 비공개 저장소는 작업자 3인 이하인 경우에 무료, 설치형 버전인 Enterprise는 월 21달러
GitLab | GitLab inc | NASA, Sony 등 많은 조직이 사용, GitLab 자체가 오픈소스인 특징 | 공개, 비공개 저장소 생성 무료
BitBucket | Atlassian | 사용자 600만명, 지라(Jira)와 연동이 쉽다 | 5명 이하 팀이면 공개 및 비공개 저장소 생성 무료

<br> 

# ch2. Git & GitHub 시작하기 feat.GLI

GitHub에 코드를 올리는 과정

<br>

## 프로젝트 폴더에 Git을 쓴다는 명령
git init 을 한다  
git init 을 하면 .git의 폴더(숨김처리), 로컬 저장소가 나오게 된다  
이 로컬 저장소에서 버전관리 작업을 할 수 있다  
로컬 저장소를 직접적으로 만지는 경우는 없고 명령어를 통해 사용한다

프로젝트 폴더에서 Git 명령을 쓰는 관정

1. 원하는 폴더에서 Git 초기화를 한다
1. Git 초기화를 하면 .git 이라는 숨겨진 폴더(로컬 저장소)가 만들어진다
1. 로컬 저장소에 내가 만든 버전 정보, 원격 저장소 주소 등이 저장된다
1. 원격 저장소에서 내 컴퓨터로 코드를 받아오면 로컬 저장소가 자동으로 생긴다

**한 폴더에 하나의 로컬 저장소만 유지해야한다**  
.git을 만들고 원격 저장소에서 코드를 받아오면 또 .git이 생기기 때문에 충돌이 발생한다

### 로컬 저장소 생성 실습
1. 컴퓨터에 폴더 생성
1. Git Bash 로 만든 폴더에 들어가기     
1. git init 으로 로컬 저장소 생성

>순서대로 진행
git bash에 `pwd` 를 입력하면 현재 폴더를 알 수 있다  

`ls` 를 입력하면 현재 파일에 어떤 폴더와 어떤 파일이 있는지 알 수 있다  

다른 폴더를 선택하려면 `cd "들어갈폴더이름"` (change directory) 를 입력한다  

이 `pwd` , `ls` , `cd` 를 활용해 원하는 폴더에 접근한다  
생성한 빈 폴더에 접근하면 `ls` 를 입력했을 때 아무것도 출력되지 않는다

`git init` 을 입력한다
initialized impty Git repository in ~~ 가 출력된다  
빈 깃 레포지토리(로컬저장소)를 만들었다는 뜻이다  
`git init` 을 한 후에는 `(master)` 라는 단어가 추가되어있다

`ls -al` 을 출력하면 `.git` 파일이 보이다  
`.git`파일이은 레퍼지토리가 만들어 졌다는 뜻이다  
즉 숨겨진, 보이지않는 폴더를 볼 수 있게 해준다  

<br>

## 첫번째 버전 만들기

### 커밋(commit) = 하나의 버전  

페이지 1, 2, 3 작성 = commit,  
페이지 2 수정 = commit  
이런 버전들을 오갈 수 있다

### add = 커밋으로 만들길 원하는 파일만 선택
페이지 1, 2, 3 작성 = add,  
페이지 1, 2 선택 = commit  
결과적으로 커밋은 1, 2가 된다  

### 버전 생성 실습
1. VS Code에서 선택한 폴더에 README.md, index.html 파일 생성
1. 원하는 파일만 선택하기  
`git add README.md`
1. 메시지를 달아 커밋으로 만들기  
`git commit -m "프로젝트 설명 파일 추가"`
1. 생성한 커밋 보기  
`git log`

* git add . 을 하면 폴더에 있는 전체 파일을 추가할 수 있다

### 커밋특징
* 커밋은 '의미 있는 변동사항' 을 묶어서 만든다
* 만약 하나의 기능을 고치는데 5가지 파일을 수정했다면 그 5가지를 묶어서 하나의 커밋으로 만든다
* 개발자들이 어떤 파일을 수정했는지 손쉽게 파악할 수 있다
* 커밋 메시지를 적는게 관리하기 편하다

<br>

## 만든 버전 GitHub에 올리기 
GitHub에 만든 버전을 올려서 다른 사람들과 함께 버전 관리를 할 수 있다  

> 만든버전을 github에 올리려면 아래의 과정을 거쳐야 한다

GitHub 사이트에서 프로젝트 저장소 만들기  
내 컴퓨터 프로젝트 폴더에 GitHub 저장소 주소 알려주기 = `git remote add`  
내 컴퓨터에 만들었던 덩어리 GitHub에 올리기 = `git push`

### 원격 저장소 GitHub에서 만들고 커밋 푸쉬하기 실습
1. GitHub에 로그인해서 레퍼지토리 생성
1. 내 컴퓨터 로컬저장소폴더에 GitHub 저장소 주소 알려주기    
`git remote add origin https://github.com/아이디/이름.git`  
remote add = 원격저장소를 추가한다는 말이다  
origin = 원격저장소를 'origin' 이라는 이름 으로 추가한다는 말이다 (origin이 아닌 다른 이름도 된다)
1. 만든 커밋 푸쉬하기  
`git push origin master`  
'origin' 이라는 이름으로 리모트를 추가했기 때문에 'origin' 이다  
'master' = 브렌치라고 하는 개념이다 (기본 브렌티가 'master' 다)  
즉 'origin' 리모트에 'master' 브렌치에 커밋들이 올라가게 된다  
1. GitHub 사이트에서 올라간 커밋 확인  

<a href = "https://myhappyman.tistory.com/54" target = "_blank" title = "참고자료">원격저장소 주소 삭제하기</a>  
`git remote rm 저장소이름`  
즉 `git remote rm origin`

github의 우측상단에서 레퍼지토리를 생성할 수 있다  
* New repository = 새로운 저장소
* Import repository = 저장소 가져오기  
* New gist = 코드 조각을 올릴 때 사용  
저장소는 큰 단위의 폴더, 여러가지 코드가 모여있다
* New organization = 팀프로젝트 등을 할 때 팀이름으로 만들 수 있다  

README.md는 깃허브 저장소에 들어왔을 때 이 소스코드가 무엇을 하는지, 어떤 정보를 봤으면 좋겠는지 등을 요약하는 안내하는 역할을 한다

<br>

## 다른 사람이 만든 저장소 받아오기
원격 저장소를 내 컴퓨터에 받아는 것을 **클론 (clobe)** 이라 한다  
원격 저장소의 데이터를 가져오는 것을 **풀 (pull)** 이라 한다

<br>

# ch3. Git & GitHub 다지기 feat.GUI






<br>