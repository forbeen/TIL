# TIL
## Vs code 주요 단축키
* `ctrl + K` -> `crtl + \` 위/아래 수직 화면 분할 
* `ctrl + \` 좌/우 수평 화면 분할
* `ctrl + 3` 터미널 실행/닫기
## 작업폴더 설명
* `html_basic/` : html기초 연습파일 모음
* `task/` : 과제제출 폴더, 파일 모음 (폴더명은 날짜별로 구성됨)
* `README.md` : 배운 내용 기록, 어려운 점 및 막힌 점 자유롭게 기록
### 2025/04/04 - HTML 3일차 문서와 레이아웃
* `h1~h6`, `p`, `br`, `em`, `strong`, `del`, `s`, `sup`, `sub`
* `<`이 기호의 유니코드= `&lt;` | `>`이 기호의 유니코드=`&gt;`
### 2025/04/07 - HTML 4일차 레이아웃
* `div`, `span`
* 웹/앱 레이아웃 방향과 의미에 따라 2개 이상의 요소를 묶어주는 레이아웃 요소
* `div`는 생성 시 반드시 그룹을 구분할 수 있는 이름을 설정해야 한다. `span`은 선택!
* 이름 작성 시 주의사항 : 반드시 용도에 맞는 의미있는 영단어 사용!!
### HTML 구조 공부 순서
1. 클론 코딩 & 클론 디자인할 사이트 정하기
2. 피그마에서 와이어프레임 만들기 (레이어, 폴더 이름 주의)
3. 피그잼에 일부 화면 넘겨서 태그 계획하기
4. 계획한 태그를 가족관계에 맞게 트리구조 만들기
5. vs code에서 실제 HTML 작성하기 (트리구조 순서에 맞게 바깥쪽 -> 안쪽 순서로!)
### 다른 환경에서 git 이어서 작업하기 (집)
1. 새폴더 연결하기
2. `git clone 저장소 주소 붙여넣기`
3. `cd 내려받은폴더명(til)`입력해서 main설정하기
4. 이어서 자유롭게 수정 후 저장
5. `git status` 상태확인
6. `git add` 스테이징 업로드
7. `git commit -m "메세지"` 
8. `git push origin main`으로 업로드
### (위 이어서) 다른 환경에서 git 이어서 작업하기 (학원)
* 학원에서 `git pull origin main`으로 집에서 올린 파일 내려받기
* main 연결이 완료된 환경에서도 위 명령어를 입력해야함
----
### 바로가기 메뉴 만들기
0. (조건) 화면이 수직으로 충분히 이동할 수 있을 만큼 스크롤 준비
1. 바로가기 메뉴 a 태그 준비하기
2. 바로가기 위치 div id명 준비하기
3. 위 1번 `a` 속성 `href` 값으로 `#`먼저 작성 후 위 2번 이름 작성하기
4. 위 3번 결과 예시> id가 abcd일 경우 `<a href="#abcd"></a>`
* `<a href="#"></a>` 이건 임시사이트 주소를 #으로 쓰겠다는 말 (연결페이지 제작 전)
* `<a href="#header"></a>` 이건 id가 header인 곳으로 바로가기 하겠다는 말 (같은 파일 내 다른 위치 이동)
* `<a href="./basic/index.html"></a>`링크태그에 묶여있는 무언가를 클릭했을 때 베이직 폴더에 있는 인덱스 파일로 이동하겠다는 말 (상대경로링크)
* `<a href="./basic/index.html#main"></a>`링크태그에 묶여있는 무언가를 클릭했을 때 베이직 폴더에 있는 인덱스 파일에 "메인"으로 이동하겠다는 말 (상대경로링크+바로가기링크)
----
### css프리텐다드 `link`주소
* `<link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard-dynamic-subset.min.css" />`
----
## CSS Style Sheet
* 외부스타일시트 파일 저장 **style**폴더에 `파일명.css`로 저장한다.
* 위 파일 생성 후 CSS연결을 원하는 HTML파일 head위치에 `<link>`태그로 연결한다.
* HTML작성 후 HTML의 모든 디자인형태를 초기화하는 `reset.css`도 반드시 연결해야한다.
* 웹글꼴(Noto Sans KR, Pretendard 등) 연결 시 HTML파일에 `<link>`태그 연결!
### head태그 내에 들어가는 link태그 작성 순서
1. 웹글꼴 포함 기타 플러그인 연결 주소
2. reset.css
3. 해당 HTML별 디자인.css
### 디자인 CSS 작성 시 작성 순서 빛 주의사항
* **부모->자식**순서로 가장 바깥쪽 부모부터 먼저 선택자를 만들고 디자인한다.
* 레이아웃 관련 요소에 `width, height` 속성 작성 시 영역 확인을 위한 `background-color`를 꼭 함께 작성해서 정확히 구분한다. 이 때 색상은 쉬운 영역 구분을 위한 `aqua, lime, yellow, pink`등의 밝은 색상 위주로 사용한다. 영역 확인과 디자인 작업을 모두 마친 후 위 색상은 제거로 마무리해야한다.
* 실제 디자인에 들어가는 색상은 **rgba 또는 헥사코드**로 입력하고 테스트용으로 입력하는 임시 색상은 영문명으로 입력해야 한다.
### 자주 이용하는 CSS 속성 값과 기본값
* `letter-spacing` 자간 글자 사이의 거리 | 기본값 0 | {letter-spacing:-0.02;}
* `line-height` 행간 문장 사이의 거리 | 기본값 1(100%) | {line-height:1.5;}
* `font-size` 글꼴 크기 | 기본값 16px(1em) | {font-size:1rem;}
* `color` 글자 색상 | {color:#111;} {color:rgba(0, 0, 255, 0.8);}
* `background-color` 블록or인라인 영역 배경 색상 | {background-color:#fff;}
* `width` 가로크기 | {width:50px;}
* `height` 세로크기 | {height:50px;}
* `margin` 선택영역 밖으로 떨어진 거리 | {margin-`top,bottom,left,right`:50px;}
* `border-radius` 모서리 라운드값 | {border-radius:20px;}
* `font-weight` 글꼴 두께 | 기본값400 | {font-weight:400;}
* `font-family` 선택 글꼴 입력 | {font-family:'Noto Sans KR', '보조글꼴'  sans-serif;}
----
### 막혔던, 궁금했던 사항들 (해결하면 하루 이틀 후 지움)
* 인용구를 사용하는 `q`(인라인), `blockquote`(블록) 태그들은 vs code에선 속성값인 `cite=""`에 링크를 적지만 사이트에선 클릭이 안된다캄
* 인라인끼리 형제인데 왜 `span`으로 안묶음? -> `span`은 `div`로 묶을 수 있음 같은 위치내에 형제들을 확인하고 블록일 경우 `div`로 그룹지음. 잘 이해가 안가면 figjam들어가서 공부용 확인하기
* 학원에서 이어받기 할때 ~~`git clone`하면 안됨!! 또 폴더를 내려받는거니까~~ (x) `git pull origin main` (o)