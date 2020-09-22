## HTML 기본 용어
---
- 태그
   : HTML페이지에서 객체를 만들 때 사용 ex) h1, p, br 등
- 요소
   : 태그를 사용해 만들어진 객체
- 속성
   : 태그에 정보를 추가할 때 사용, 시작 태그에 작성
   + 형식: 속성명="속성값"
- 주석
   : HTML코드 설명을 위해 작성
   + 형식: ```<!--주석내용-->```


## HTML5 페이지 구조
---
### 1. !doctype
    - HTML의 버전을 의미, HTML5는 <!doctype html>이라 작성
### 2. html태그
    - 모든 HTML페이지의 루트 요소로 모든 HTML태그는 html태그 내부에 작성
### 3. head태그
   - 사용자가 실제 보는 화면과는 크게 관계없지만 HTML페이지에 여러 정보 제공
   - 다음 태그만 포함 가능 
      + meta, title, script, link, style, base
4. body태그
    - 실제 사용자에게 보여지는 내용을 작성하는 부분

## 기본 태그
---
### [글자 관련 태그]

 - 제목 태그: 제목을 나타내기 위한 태그
   + h1, h2, h3, h4, h5, h6 (*숫자가 클수록 글자 크기 작아짐)

 - 본문 관련 태그 
   + p : 단락을 나타내는 태그
   + br : 줄바꿈 태그
   + hr : 수평줄 태그

 - 글자 형태 관련 태그
   + b : 굵은 글자
   + i : 기울어진 글자(이탤릭체)
   + small : 작은 글자
   + sub : 아래 첨자
   + sup : 윗첨자
   + ins : 밑줄 글자
   + del : 취소선 그어진 글자

 - 앵커 태그: 페이지 내에서 이동하거나 다른 페이지로 이동 시 사용
   + a: href 속성값으로 이동하고자 하는 요소의 위치 또는 문서의 위치 설정
     * 페이지 내 이동(id값 설정) ex) `<a href="#id값">` 
     * 다른 페이지로 이동(파일경로나 URL설정) ex) `<a href="./anchor.html">`


### [목록 관련 태그]

 - ol (ordered list)
   + 순서가 있는 목록을 만드는 태그

 - ul (unordered list)
   + 순서가 없는 목록을 만드는 태그

 - li
   + 목록의 아이템들을 나타내는 태그
   + ol 또는 ul 태그 내부에서 사용


### [표 관련 태그]

 - table : 표를 만들기 위한 태그, 아래 태그들이 table 태그 안에서 사용
   + caption : 표의 제목
   + thead : 표의 헤더
   + tbody : 표의 몸체
   + tfoot : 표의 푸터
   + tr : 표의 행 생성
   + th : 표의 제목 셀을 생성, tr태그 내부에서 사용
   + td : 표의 데이터 셀을 생성, tr태그 내부에서 사용
    + <**th,td태그의 속성**>
        - rowspan: 사용하는 행의 크기는 지정하는 속성(행 병합)
        - colspan: 사용하는 열의 크기를 지정(열 병합)


### [공간 분할 태그]

 - div : block 형식의 공간을 만드는 태그(의미는X)
 - span : inline 형식의 공간을 만드는 태그(의미는X)
 - 시맨틱 구조 태그 : 페이지의 구조를 의미적으로 분석 가능, 다음 태그들 포함
   + header, nav, aside, section, article, footer



## 멀티미디어 관련 태그
---
### 1. 이미지 태그
   - img
   - <img 태그의 속성>
      + src: 이미지의 주소 지정
      + alt: 이미지 로드할 수 없을 시 나오는 글자 지정
      + width: 이미지의 너비 지정
      + height: 이미지의 높이 지정

2. 오디오 태그
   - audio
   - <audio 태그의 속성>
      + src: 음악 파일의 경로 지정
      + preload: 음악 재생 전 모두 불러올지 지정
      + autoplay: 자동 재생 여부 지정
      + loop: 반복 재생 여부 지정
      + controls: 음악 재생 도구 출력 여부 지정
   - source : 브라우저와 브라우저의 버전마다 지원하는 음악 파일 종류가 다를 때 유용한 태그
      + ex) `<source src="오디오파일경로1" type="audio/mp3">`

3. 비디오 태그
   - video
   - <video 태그의 속성>
      + src: 동영상 파일의 경로 지정
      + poster: 동영상 준비 중일 때 이미지 파일의 경로 지정
      + preload: 비디오 재생 전 모두 불러올지 지정
      + autoplay: 자동 재생 여부 지정
      + loop: 반복 재생 여부 지정
      + controls: 비디오 재생 도구 출력 여부 지정
      + width: 동영상 너비 지정
      + height: 동영상 높이 지정
   - source : 브라우저와 브라우저의 버전마다 지원하는 동영상 파일 종류가 다를 때 유용한 태그
   + **Youtube 동영상은 Youtube에서 소스코드를 복사하여 넣을 수 있음


## 입력 양식 태그
---
입력 양식 태그는 사용자로부터 데이터를 받기 위해 사용

### [form 태그]
: 입력 양식을 만들기 위한 태그, 입력을 위한 태그들을 배치하여 작성
- < form 태그의 속성 >
   + action: 입력 데이터의 전달 위치 지정
   + method: 입력 데이터의 전달 방식 지정

### [입력을 위한 태그]
1. input : 사용자로부터 정보를 입력 받도록 하는 태그
   - <input 태그의 속성>
       + type : 입력 양식의 종류 결정 
         - type 속성값: button, checkbox, hidden, image, password, radio, text, file, reset, submit, text, email, tel, number, date
       + name : 서버로 양식 전송 시, 각 입력 항목 구분을 위한 이름값 설정
       + placeholder : 사용자가 값을 미입력시 안내 글 작성
       + disabled : 입력 양식을 비활성화
       + readonly : 읽기만 가능
       + value : 입력 양식의 값


2. textarea : 사용자로부터 여러 줄의 텍스트를 입력 받도록 하는 태그
   - <textarea 태그의 속성>
       + cols : 태그의 너비를 지정(글자 수)
       + rows : 태그의 높이를 지정(라인 수)
       + name : 서버로 양식 전송 시, 각 입력 항목 구분을 위한 이름값 설정
       + placeholder : 사용자가 값을 미입력시 안내 글 작성
       + disabled : 입력 양식을 비활성화


3. select : 여러 개의 목록에서 몇 가지를 선택할 수 있는 입력 양식
   - select 태그와 함께 사용되는 태그
      + optgroup : 옵션 그룹화
      + option : 선택할 수 있는 옵션 생성
   - <select 태그의 속성>
       + name : 서버로 양식 전송 시, 각 입력 항목 구분을 위한 이름값 설정
       + multiple : 여러 옵션을 선택할 수 있게 함
       + disabled : 입력 양식을 비활성화

### [label 태그]
: 입력 양식에 대한 설명을 제공
- <label 태그의 속성>
   + for:
    label과 연결할 입력 양식 태그를 설정(입력 양식의 id 속성값)

### [fieldset 태그]
: 입력 양식들을 하나의 그룹으로 묶기 위해 사용

### [legend 태그]
: fieldset에 대한 설명을 제공
