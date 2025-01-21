# 2024-winter-Mogakso

2025.01~02 동계 모각소

**목표**
- HTML, CSS 마스터
- React 환경설정 완벽히 하고 기초 끝내기
- JS도 기초정도는 할 수 있으면 좋겠다..
---
## 01-16
기초적인 웹개발 환경 설정
---
## 01-20
HTML/CSS 기초 끝내기

### 태그
**기초**
- `<p>` : 문단
- `<b>` : 굵게
- `<br/>` : 줄바꿈
- `<li>` : 리스트
    - `<oi>` : 정렬된 리스트
    - `<ul>` : 정렬되지 않은 리스트
- `<a>` : 링크

**이미지, 동영상, 오디오**
- 이미지: `<img src="경로 or 주소" alt="설명">`
- 동영상: `<video src="경로 or 주소" 속성>` 
- 오디오: `<audio src="경로 or 주소">`  

**표**
- `<table>`:테이블 만들기 
- `<thead>, <tbody>`:테이블 헤더, 바디 만들기 (thead는 선택)
- `<tr>`: 테이블 행 만들기
- `<th>, <td>`:테이블 열 만들기(th는 열의 헤더, td는 열의 데이터)
- `<caption>`:표의 제목

**폼 관련 태그**
- button
```html
<body>
    <button name="btn" type="button">버튼</button>
</body>
```
- input
    - 속성
    type: 타입에 따라 모양새가 다름. 아래 참고
        - type별 input
        ```html
          <body>
            <input type="text" name="text" required/>
            <input type="password" name="password" required/>
            <input type="checkbox" name="checkbox" />
            <input type="checkbox" name="checkbox" />
            <input type="radio" name="radio" />
            <input type="radio" name="radio" />
            <input type="range" name="range"/>
            <input type="color" name="color" />
            <input type="date" name="date" />
            <input type="file" name="file" />
        </body>
        ```
    name: 입력창의 이름. 제출 시 value와 데이터를 구성함
    required: 해당 입력이 필수인 경우 설정
- select option
    - `<select>`:옵션 메뉴 제공
    - `<option>`:항목 제공
```html
<body>
    <select name="과일">
    <option value="">과일을 선택하세요</option>
    <option value="apple">사과</option>
    <option value="banana">바나나</option>
    <option value="orange">오렌지</option>
    <option value="lemon">레몬</option>
    </select>
</body>
```
- label(항목 설명)
```html
<body>
    <label>이름을 알려주세요
        <input type="text" name="user_name" />
    </label>

    <label>과일을 선택하세요
        <select name="fruit">
            <option value="apple">사과</option>
            <option value="banana">바나나</option>
            <option value="orange">오렌지</option>
        </select>
    </label>
</body>
```
- form(폼):데이터 제출을 위한 툴 ex.로그인인
    속성
    - `action` : 데이터를 보낼 URL
    - `method` : HTTP method
```html
<form action="" method="post">
    <input type="text" placeholder="아이디를 입력하세요" />
    <input type="password" placeholder="비밀번호를 입력하세요" />
    <button>제출</button>
</form>
```

**div와 span**
차이점
- `<div>`:브라우저의 한 줄 모두 차지 (블록 컨테이너)
- `<span>`:컨테이너의 크기만큼만 차지 (인라인 컨테이너)
```html
<body>
    <h1>레이아웃 설정하기</h1>
    <div>
    <h2>div</h2>
        <p>첫 번째 블록</p>
    </div>
    <div>
        <h2>div + span</h2>
        <p><span>두 번째</span> 블록</p>
    </div>
</body>
```

**시멘틱 태그**
<div>
    <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FIA3PW%2Fbtrv4KUR4Pu%2Fxhi1IJCC6lrXflJlkGi1y0%2Fimg.png" width="600">
</div>

- header : 사이트의 로고, 제목 등
- navigation : 사이트의 메뉴들 위치, 대체로 헤더 안에 있지만 다른 곳에 있어도 됨
- main : 본문
- article : 기사에서 하나의 글처럼 독립적으로 구성할 수 있는 요소
- aside : 사이드바, 주로 광고 위치
- footer : 저작권 정보, 연락처 등 위치

## 01-21
### HTML의 기본 구조

<div>
    <img src="https://prod-files-secure.s3.us-west-2.amazonaws.com/e07275ce-0724-496e-8178-adde224695a9/f0a480e8-5412-45bd-85c6-9af04da7c9e1/image.png" width="600">
</div>

### CSS

**style 주요 속성**

- `width` : 요소의 너비이다. 기본 값은 auto이다.
- `height` : 요소의 높이이다. 기본 값은 auto이다.
- `max-width` `min-width` : 요소가 가질 수 있는 최대, 최소 너비이다.
- `max-height` `min-height` : 요소가 가질 수 있는 최대, 최소 높이이다.

모두 px, em, rem단위 등으로 크기를 지정해준다.

- `margin` : 요소의 외부영역이다.
    - auto, px, em, vx 등의 단위로 크기를 설정한다.
    - 기본 값은 0이다.
    - `margin (위, 아래) (왼쪽, 오른쪽)` : 요소의 위와 아래, 왼쪽과 오른쪽의 값을 설정한다.
    - `margin (위) (왼쪽, 오른쪽) (아래)` : 요소의 위, 왼쪽과 오른쪽, 아래의 값을 설정한다.
    - `margin (위) (오른쪽) (아래) (왼쪽)` : 요소의 위, 오른쪽, 아래, 왼쪽의 값을 설정한다.
- `padding` : 요소의 내부영역이다. 기본값은 0이다. 내부 요소기 때문에 요소가 커질 수 있다.
    - px, em, vw, % 등의 단위로 크기를 설정한다.
    - `margin` 요소와 같이 단축 속성이다.
- `margin-top` `margin-bottom` `padding-right` `padding-left` : 개별 속성으로 특정 방향만 개별적으로 적용할 수 있다.
- `border` : 요소의 테두리를 설정한다.
    - `border (테두리 두께) (테두리 스타일) (테두리 색상)` : 테두리 두께, 스타일, 색상을 한꺼번에 명시할 수 있다.
    - 테두리 두께 : px, em단위 등으로 설정한다.
    - 테두리 스타일 : `solid` (실선), `dashed` (점선), `dotted` (동그란 점선) 등의 값이 있다.
    - 테두리 색상 : 원하는 색으로 설정할 수 있다.
- `border` 관련 개별속성
    - `border-width` : 테두리의 두께만 설정한다. 개별 속성이나 `margin` 과 `padding` 처럼 방향에 의한 단축 속성이기도 하다.
    - `border-style` : 테두리의 스타일만 설정한다. 개별 속성이나 `margin` 과 `padding` 처럼 방향에 의한 단축 속성이기도 하다.
    - `border-color`: 테두리의 색상만 설정한다. 개별 속성이나 `margin` 과 `padding` 처럼 방향에 의한 단축 속성이기도 하다.
- `border-radius` : 모서리 부분을 둥글게 할 수 있다.
    - 0이 기본값이고, px, em, vw단위 등으로 설정할 수 있다. `margin` `padding` 처럼 단축 속성이다.
    - `border-radius (왼쪽 위) (오른쪽 위) (오른쪽 아래) (왼쪽 아래)` : 시계방향으로 각 위치마다 다른 값을 줄 수 있다.
- `box-sizing` : 요소의 크기 계산 기준을 결정한다.
    - `box-sizing: content-box` : 요소의 내용을 기준으로 크기를 계산한다.
    - `box-sizing: border-box` : `padding` 과 `border` 를 합친 크기를 기준으로 크기를 계산한다.
- `overflow` : 요소의 크기 이상으로 내용이 넘쳤을 때, 어떻게 보여질 지를 제어한다.
    - `overflow: visible` : 기본 값이며, 그대로 보여준다.
    - `overflow: hidden` : 넘친 내용을 자른다.
    - `overflow: scroll` : 넘치는 부분만 잘라내고, 스크롤 바를 생성한다.
- `display` : 요소의 화면 출력 특성을 지정한다.
    - 기본 값은 요소의 특성에 맞게 설정 되어있다.
    - `display: block` : 해당 요소를 블록 요소로 만든다.
    - `display: inline` : 해당 요소를 인라인 요소로 만든다.
    - `display: flex` : 요소들의 레이아웃을 1차원으로 나열한다.
    - `display: grid` : 요소들의 레이아웃을 2차원으로 나열한다.
    - `display: none` : 요소를 숨긴다. HTML문서에 존재하지만 보여지지는 않는다. 레이아웃도 영향을 받는다.
- `opcaity` : 요소의 투명도를 설정한다. 0이 기본값이며, 레이아웃에는 영향을 주지 않는다.
- `font style` : 텍스트의 기울기를 설정한다.
    - `font style: normal` : 기본 값으로 아무런 기울기를 주지 않는다.
    - `font style: italic` : 텍스트를 이탤릭체 스타일로 기울인다.
- `font-weight` : 텍스트의 두께를 설정한다.
    - `font-weight: normal` : 기본 값으로 아무런 두께를 주지 않는다.
    - `font-weight: bold` : 약간 두껍게 한다.
    - 100 ~ 900까지 값을 줄 수 있으나, 400(normal)과 700(bold)을 주로 사용한다.
- `font-size` : 텍스트의 크기를 설정한다.
    - px, px, em, rem단위 등으로 지정한다.
- `line-height` : 줄의 높이를 설정한다.
    - `line-height: normal` 기본 값이다.
    - em단위로 요소의 텍스트 크기의 배수로 지정하는 걸 권장한다.
    - 글자가 y축 기준 가운데 정렬이 된다.
- `font-family` : 텍스트의 글꼴을 설정한다.
    - `font-family (글꼴) (글꼴) (글꼴계열)` : 명시한 글꼴들을 앞쪽부터 차례대로 사용하려고 시도한다. 글꼴은 여러 개 명시할 수 있다. 글꼴이름에 띄어쓰기 등 특수문자가 있으면 ""로 묶어야 한다. 아무런 글꼴도 찾지 못했을 경우 마지막에 명시한 계열의 아무런 글꼴을 사용한다.
    - 글꼴계열 : serif(바탕체), sans-serif(고딕체), monospace(고정너비).
- `color` : 텍스트의 색상을 설정한다.
    - `color: (색상)` : 기본값은 흰색 rgb(0, 0, 0)이다.
- `text-align` : 문자의 정렬방식을 설정한다.
    - `text-align: left` : 기본 값으로 왼쪽으로 정렬한다.
    - `text-align: right` : 오른쪽으로 정렬한다.
    - `text-align: center` : 가운데로 정렬한다.
- `text-decoration` 문자에 선을 넣는다.
    - `text-decoration: none` : 기본 값으로 선을 넣지 않는다. `<a>` 요소는 제외한다.
    - `text-decoration: underline` : 텍스트에 밑줄을 추가한다.
    - `text-decoration: line-through` : 텍스트에 중앙선을 추가한다.
- `text-indent` : 지정한 값만큼 들여쓰기를 한다.
    - px, em, rem 등의 단위로 설정할 수 있다.
    - 음수로 내어쓰기도 가능하다.
- `background-color` : 배경 색상을 설정한다.
- `background-image` : 배경 이미지를 추가한다.
    - `background-image: url("경로")` : 추가할 이미지의 절대경로 혹은 상대경로를 작성한다.
    - 이 후, 배경 이미지의 width, height를 따로 명시해야 한다.
- `background-repeat` : 배경의 반복을 제어한다. 기본적으로 바둑판식 배열로 정렬된다.
    - `background-repeat: repeat` : 기본 값으로 x, y축으로 반복된다.
    - `background-repeat: no-repeat` : 반복을 하지 않는다.
    - `background-repeat: repeat-x` : x축으로 반복한다.
    - `background-repeat: repeat-y` : y축으로 반복한다.
- `background-size` : 배경의 크기를 설정한다. 바둑판식 배열로 정렬된다. 가로나 세로 하나만 명시하면 그에 따라 비율이 유지된다.
    - `background-size: auto` : 기본값이며, 이미지의 실제 크기로 설정된다.
    - `background-size: cover` : 이미지의 비율을 유지하되, 요소의 더 넓은 너비에 맞춘다.
    - `background-size: contain` : 이미지의 비율을 유지하되, 요소의 더 짧은 너비에 맞춘다.
    - px,em,rem 등의 단위로 설정할 수 있다.
- `background-position` : 배경이미지 위치를 설정한다.
    - `background-position: (위치, x축) (위치, y축)` : 두 개의 값을 입력한다.
    - 방향 : top, right, center, left 등의 위치를 입력한다.
    - x, y축 : px, em, rem 등의 단위로 입력한다.
- `background-attachment` : 배경이미지 스크롤 특성을 설정한다.
    - `background-attachment: scroll` : 기본 값으로, 화면을 스크롤 하면 그에 맞춰 이미지도 이동한다.
    - `background-attachment: fixed` : 화면을 스크롤 하여도 이미지가 Viewport기준 위치한 자리를 유지한다.

---

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .color-primary {
            color:red;
        }
        .font-50px{
            font-size: 50px;
        }
    </style>
</head>
```

이런식으로 헤드 안에 style을 지정함

```html
<body>
    <h1>아주대학교 동계 모각소</h1>
    <p class="color-primary font-50px">소프트웨어학과</p>
    <img width="500px" src="https://blog.kakaocdn.net/dn/bezjux/btqCX8fuOPX/6uq138en4osoKRq9rtbEG0/img.jpg">
</body>
```

그럼 바디 안에 쓸 수 있음
코드에서 함수와 똑같은 역할을 하는 듯

바디 안에서 바로 쓰고 싶으면 아래와 같이 쓰면 됨

```html
<p style="color:coral">202322051</p>
<p style="color:rgba(130, 167, 214, 0.64)">202322051</p>
```

아니면 css 파일에 경로를 지정해줘서 전부 적용시킬 수도 있음

- html 파일

```html
    <table class="tb">
        <thead>
            <tr>
                <td>이름</td>
                <td>지역</td>
                <td>전화번호</td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>홍길동</td>
                <td>서울</td>
                <td>010-1111-1111</td>
            </tr>
        </tbody>
    </table>
```

- css 파일

```css
.tb>thead>tr>td{
    border: 1px solid #000;
}
```

---

링크 a

```html
<a href="[https://www.naver.com](https://www.naver.com/)" target="_blank">네이버</a>
```

**target 속성**

- _self : 링크 클릭 후 해당 창에서 열기
- _blank : 링크 새창으로 열기
- _parent : 부모창에서 열기 (부모 창이 없는 경우 _self 속성 처리)
- _top : 전체 브라우저 창에서 가장 상위 창 열기(부모 창이 없는 경우 _self 속성 처리)

---

**css 선택자**

- 전체 선택자
    
    ```html
    * { margin: 0; text-decoration: none; }
    ```
    
- 태그 선택자
    
    ```html
    p { background: yellowgreen; color: darkgreen; }
    ```
    
- 클래스 선택자
    
    ```html
    .class1 { background: yellowgreen; color: darkgreen; }
    ```
    
- ID 선택자
    
    ```html
    #id1 { background: yellowgreen; color: darkgreen; }
    ```
    
- 하위 선택자
    
    ```html
    div ul { border: 1px dotted black; }
    ```
    
    `<div>` 안에 있는 모든 ul (unordered list)에 적용
    
- 자식 선택자
    
    ```html
    div>ul { border: 1px dotted black; }
    ```