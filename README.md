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
### table 태그 요소와 속성 (모두 블록)
* `table`, `thead`, `tbody`, `tfoot`, `tr`=행, `th`=제목열, `td`=내용열
* 모든 행에 들어가는 열의 개수는 동일하게 작성한다.
* 제목행 `thead`는 제목`th`만 존재해야함
* 수평 열 합치기 속성=`colspan` 수직 행 합치기=`rowspan`
* td 또는 th 열에만 주는 속성으로 적용 순서는 아래와 같다.
1. 합치고 싶은 가로(세로)방향 열 2개 이상 정하기(개수 제한 없음)
2. 위에서 정한 태그 확인하기
3. 위 태그 중 먼저 시작한 태그 속성으로 colspan="합치는 칸의 개수"
4. 합쳐지는 첫번째를 제외한 나머지 태그는 주석으로 가리기

## 위치속성 float
* 블록, 인라인 요소를 좌(left), 우(right) 사용하는 위치 속성
* 좌/우 배치하고 싶은 요소가 형제인 경우 사용
* 형제가 3개 이상인 경우 1->2옆으로 두고 3을 내리고 싶은 경우, 형제3에게 'clear:both`를 선언하여 이전 형제의 float 정렬 제거하기
### * 오른쪽으로 보내고싶은 형제 요소가 2개 이상이라면?
* 2개를 묶어서 그룹으로 처리하고 `float:right`를 한번만 작성한다.
* `float:right`는 2번 이상 사용하면 역순이 되므로 **한번만 작성해야 한다!!**
### float를 적용하는 형제의 부모의 높이가 max-content(기본값)이라면?
* 부모의 높이를 제대로 인식못하므로 높이를 강제 (px) 시키거나 `overflow:hidden`높이를 안주고 영역 재인식을 시켜 float에 의한 오류를 제거해야 한다.
## form 태그 관련 속성 주요 뜻과 사용 용도
* 입력 양식 `input type=` text, password, email, search, number 등..
* 선택 양식 `input type=` checkbox, radio, seclect, option 등..
* 입력 양식과 선택양식에 따라 같은 스펠링의 속성의 뜻이 달라지므로 주의해야 한다.!
## 양식에 따라 다른 속성의 뜻
* `value` : 입력양식(사용자가 입력한 값(속성작성x)), 선택양식(사용자가 선택해서 서버에 전송되는 값(속성작성o))
* `name` : 입력양식(사용자가 선택해서 서버에 전송되는 값(작성o)), 선택양식(2개 이상의(1개도 가능) 선택양식을 묶어주는 동일 그룹(작성o))
* 입력양식에서 `value`의 초기값을 작성하는 경우: 쇼핑몰의 주문수량 (기본값 1)
## form 속성에 사용자정의값의 이름 작성할 경우 주의사항
* name, value, id, class 등 속성의 이름을 작성할때는 **중복명칭_개별명칭**을 섞어서 작성한다.
* 중복명칭에서 주로 사용하는 단어 : `admin, user`
* 개별명칭은 요소의 특징에 따라 달라진다. (`male, id, btn, pw` 등)
* 중복명칭 설정 시 작성방향도 동일하게 해야한다. 
`user_id == user_pw` O
`user_id == pw_user` X
## 목록양식 select와 option (선택 목록이 2개 이상일 경우)
* 기존목록과 비교해서 외우기 select(ul), option(li)
* `select`태그는 `option`을 묶어주는 개념으로 그룹 속성(name)이 함께 적용된다.
* `option`태그는 사용자가 실제 선택하는 값이므로 데이터 구분값 속성(value)를 작성한다.
* `option`태그 작성 시 value속성은 필수가 아닌 사용자가 선택하는 데이터에만 사용한다.
* 선택option -> `. 1. 컬러(x) 2. 블랙(black) 3. 화이트(white) 4. 코랄(coral)
## 선택양식 radio, checkbox 주의사항과 label 주의사항
* radio, checkbox는 name(동일 그룹), value(개별 데이터값) 속성을 구분해서 사용한다.
* `id`속성을 적용할때는 javascript와 연결을 위해서 하거나 또는 label의 `for`속성 연결을 위해서 사용한다. 이때 id값은 기존 개별데이터값을 가진 `value`와 동일한 값을 작성해도 된다.
* `label`은 사용자가 선택하는 이미지 또는 글자를 묶어서 작성하고 기존 선택양식 input의 형제로 작성한다면 반드시 `for`속성을 입력해서 input의 id와 동일하게 입력하고, 반대로 input의 부모로 작성한다면 for을 입력하지 않아도 된다. 대신 이경우엔 선택하는 이미지 또는 글자를 반드시 다른 인라인 태그로 묶어야 한다.
* input radio, checkbox는 사용자커스텀CSS 디자인이 불가능하기 때문에 사이트에 어울리는 모습으로 디자인하고 싶다면 `display:none`으로 숨기고 선택글자를 묶은 태그에 `background-image` 디자인 해야한다.
### input과 label이 형제인 경우
* `<input id="a"><label for="a">선택글자</label>`
### input과 label이 부모-자식인 경우
* `<label><input id="a"><span>선택글자</span></label>`
## button 속성 종류와 사용처
* `<button type="속성종류" id="버튼구분명">보이는글자 or 이미지</button> 
* 속성종류 1. button : 범용기능(주소찾기, 중복확인, 이전, 다음, 재생, 정지 등) ~~모든 형태가 가능해서 구분이 어려울땐 button으로 가능~~
* 속성종류 2. submit : `form action`주소에 `method`값 형태로 전달되는 최종 서버전송버튼
* 속성종류 3. reset : 취소 or 삭제 버튼(가입취소, 주문취소 등)
----
### 막혔던, 궁금했던 사항들 (해결하면 지우기)
* input태그의 속성 수정하고싶을 때 선택자는 `input::placeholder`이렇게 적어야함 / 글고 각 속성별로 문법이 다르다는