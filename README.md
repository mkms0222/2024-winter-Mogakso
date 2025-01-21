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

### html/css [개발자의품격]
