# Resume

[![HitCount](http://hits.dwyl.com/eehwan/Resume.svg)](http://hits.dwyl.com/eehwan/Resume)
![GitHub last commit](https://img.shields.io/github/last-commit/eehwan/Resume.svg)
![status](https://img.shields.io/badge/working-brightgreen.svg)

<br>

## 신 이 환

생년월일 : &nbsp;**1995년 2월 15일**  
전화번호 : &nbsp;**010-5006-0874**  
&nbsp;&nbsp;E-mail &nbsp;&nbsp; : &nbsp;**eehwan.shin@gmail.com**  
&nbsp;&nbsp;Github &nbsp;&nbsp;: &nbsp;**<https://github.com/eehwan>**

<br>

*********************************************
<br>

## < Education >

- 고려대학교 : _2014.03 ~ 2022.02_ (졸업예정)

<br>

*********************************************

<br>

## 풀스택을 지향하는 예비 개발자입니다

<br>

*********************************************

<br>

## 나의 강점  

<br>

- 한 번 정한 목표는 포기하지 않고 될 때 까지 노력한다.
- 사소하고 세심한 것을 캐치 잘 하며, 적당한 마무리보다 완벽한 마무리를 선호한다.

<br>

*********************************************

<br>

## < Skills >

- Front-end: Html5, Css, Scss, Javascript, webpack, React
- Back-end: NodeJS, express, RESTful api, Aws s3
- Database: SQLite, mongoDB
- Etc: socketIO, git  

<br>

*********************************************

<br>

## < 개인 프로젝트 >

### 동영상 공유 플랫폼 (Wetube) [코드 링크](https://github.com/eehwan/Wetube)

- **Stacks**: node, express, RESTful api, OAuth, Aws-S3, mongoDB, ...  
- **Features**: 회원가입, 업로드, 삭제, 댓글 등등  

### 실시간 Drawing & Chatting app (Catch-Mind) [코드 링크](https://github.com/eehwan/Catch-Mind)

- **Stacks**: node, socketIO  
- **Features**: SPA, socketIO를 통한 html Canvas 라이브 공유, 라이브 채팅  

### React framework를 이용한 영화 소개 web (movieApp) [코드 링크](https://github.com/eehwan/https://github.com/eehwan/movie_app)

- **Stacks**: React, JSX, Html, Css  
- **Features**: React를 이용한 프론트엔드 작업물  

### 그림판 (Painting Board) [코드 링크](https://github.com/eehwan/PaintingBoard)

- **Stacks**: Html, Css, Html Canvas  
- **Features**: 사진 불러오기 저장하기 등이 가능한 그림판  

### Notes for ToDo list (todoWEB) [코드 링크](https://github.com/eehwan/todoWEB)

- **Stacks**: Html, Css, Local-Storage, openweatherMap api 
- **Features**: 간단한 메모 작성, 위치기반 날씨 제공


<br>

Etc . . .

<br>

*********************************************

<br>

## 개인프로젝트를 진행하며 생긴 일화 및 고찰

<br>

### - 파이썬으로 게시판 만들기 中

#### 인코딩 오류
  
> 가장 처음 만들었던 웹페이지로 기본적인 게시판을 구현하여 아파치 서버로 가동하여 테스트했었다. 내 컴퓨터에 있는 파이썬 인터프리터로 돌아갔었는데 내 파이썬에서는 비슷한 오류가 난 적이 없었는데 자꾸 한글의 경우만 글자가 깨지는 오류가 났었다.

>그래서 서치를 하던 중 이것이 인코딩 문제라는 것을 알게 되었다.
그 후, 웹페이지의 meta태그의 charset 설정을 cp949, unicode 등으로 변경해보았고 파이썬 인터프리터에서 defaultcoding도 변경해보았지만,
문제가 해결되지 않았다.

>결국 혼자 해결 할 수가 없었다. 하지만 그 당시에는 관련 검색어나 물어볼만한 커뮤니티를 알지 못했고 개발 관련 오픈 카톡방까지 여기저기 돌아다니며 해결책을 찾았고 그 결과

```python
import sys
reload(sys)
sys.setdefaultcoding("utf-8") 
```

>위의 코드를 index.py 맨 앞줄에 넣어 실행될 때 다시 한번 defaltcoding을 세팅해주니 해결되었다. 대단한 오류도 아니었지만 초심자 시절 마주한 오류라 기억에 남는다.  

------------------------------------------

<br>

### - 그림판 (Painting board) 中

<br>

#### 그림그리는 중간중간 조금이라도 마우스가 canvas 바깥으로 나가면 선이 바로 끊기는 현상 해결

> 가장자리에 선을 채우거나 하는 작업을 할 때 종종 마우스 커서가 canvas영역 바깥으로 나갔다가 들어오는 경우가 많다. 하지만 기존에 방식으로는 나갈때마다 선이 끊겨서 해당 과정에서 상당한 불편함을 발생시켰다.

>그래서 해결책으로 canvas에 영역은 유지한 채 마우스이벤트 감지하는 영역을 넓혔다. 그렇게 하여 마우스가 canvas바깥으로 나갔다가 다시들어와도 선의 연결이 끊기지 않게 되었다.

------------------------------------------

<br>

### - Youtube를 오마주한 동영상 공유 플렛폼 (Wetube) 中  

<br>

#### 동기처리와 비동기처리에 대한 이해 부족

> 해당 내용에 대해 서치와 강의나 영상등을 시청하며 지식을 쌓고 테스트코드를 통한 연습을 하였고 하나씩 코드에 적용시켜가며 개발을 진행하였다.

#### 배포 서버가 linux기반이여 window기반 script가 동작하지 않음

>문제 원인을 찾지 못하고 헤매이다가 os가 달라 생기는 문제라는 것을 알게 되고 linux script명령어를 따로 숙지해서 dev버전은 그대로 window기반으로 나둔 채  
production버전 명령어는 linux명령어로 바꾸었다.
그 이후 다른 개인 프로젝트에서는 이런 경험을 바탕으로 os가 달라도 문제가 되지않게 gulp를 이용하여 dev모드 실행과 prduction모드 build가 될 수 있도록 설정하여 미리 해결하였다.

#### git 명령어를 잘 알지 못하여 되돌리지 못함

> 위의 배포과정에서 문제가 발생된 뒤, 사실 바로 해결된 것이 아니다. 그때 당시가 학교 시험기간이었고 바쁘고 정신없던 시간이라 일단 프로젝트는 미루어두고 학업에 집중하기로 결정햇었다.

> 그리고 시험기간이 끝난 후, 문제를 해결하고자 할때 오랜만에 코드를 보자 어디서부터 수정해야할지 막막해져서 일단 문제가 발생하기 이전으로 돌리고자 하였다. 하지만 git에 익숙하지 않아 해당 과정에 애를 먹엇고, 다시금 git을 공부하여 문제를 해결하였다. 그리고 이 문제를 언제든 다시 마주할 거 같아서 언제든 찾기 쉽게 개인 velog에 정리해두었다.

#### 고찰

> 처음으로 서버와 db, Aws-s3 Storage를 이용하여 작업하게된 프로젝트라 진행하는 과정에서 정말 머리가 하얘지는 경우도 많았고 답답한 경우도 많았다. 그만큼 완성하고 나서의 성취감과 만족감도 높았다.

> 배포나 db연결 등에 보다 익숙해지게 되었으며 RESTful api를 사용하는데에도 능숙해져서 보람이 컸다.

------------------------------------------

<br>

### -  상대방이 그린 그림 맞추기 게임 (Catch-Mind) 中    
  
<br>

#### 팝업되는 알림창을 차례로 쌓이고 위에서부터 차례로 없어지게 만드는 과정

> 기존에는 알림창을 opacity:0 으로 해두고 변경사항이 있는 경우 1. innerText를 수정 2.opacity:1 3.setTimeout으로 일정 시간이 지난 후 다시 opacity:0 으로 해두었다.  

> 하지만 팝업이 연속해서 생성되면 이전의 팝업은 확인하기 어려운 문제가 있었고, 팝업이 생성되는 순서대로 차례로 쌓이고 위에서 부터 차례로 자연스럽게 없어지는 모양을 만들고 싶었다.

> 일단 팝업을 감싸는 상위 태그를 하나 더 만들어서 display:flex를 주었다. 하지만 이 경우 상위 태그가 여러 팝업의 크기를 가지고 있어 빈 공백이 많아져 다른 dom들과의 클릭 간섭을 일으켰다.

> 그래서 상위태그에 display:flex는 그대로 두고
그 안에 Js로 알림이 생길때마다 dom을 생성해서 추가하였다. 그와 동시에 setTimeout을 걸어 몇 초가 지나면 자동으로 없어지게 구현하였다.

<br>

**결과물**
![결과물](https://images.velog.io/images/eehwan/post/cffd01d4-4b70-4a67-ace1-5c94bb10f7e0/%EC%BA%A1%EC%B2%98.JPG)

#### 고찰

> 실시간 채팅이나 유저간 실시간 통신을 가능하게 해줄 수 있는 socketIO에 관심이 생겨서 시작한 이 프로젝트를 진행하며, 채팅을 먼저 구현하였다.

> 하지만 뭔가 부족한 거 같아 기존에 진행했던 patingBoard를 이용하여 이 프로젝트를 완성하게 되었다.

> 이 프로젝트까지 진행하여 완수하고 나니 상당히 자신감이 생겼고 더욱 다양한 기능들을 구형해고 만들고 싶다는 생각이 강해졌다.

<br>

*********************************************

<br>

## 비전공자인데 개발자로 전향한 이유 ?

<br>

>기존 학과에 만족하지 못하고 있었다. 그러던 중 접한 개발에서 끊임없이 접하는 오류와 해결, 그 과정에서 오는 희열이 컸다.

>또한 작은 프로젝트를 들어가서 며칠 내지 몇 주 넘게 한 가지에 몰두하여 작업하고 마무리하여 끝마칠 때 오는 만족감이 굉장이 컸다.

>기존에 나에게 맞지 않는 전공을 공부하고 있던 터라, 개발이 나의 적성과 흥미에 잘 맞는다는 것을 더욱 확실히 느낄 수 있었으며,
나에게 무엇보다 절실하게 다가왔다.

<br>

*********************************************
