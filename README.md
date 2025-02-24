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
개발자의품격 - html, css 입문 1시간으로 끝내기 시청

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

## 01-31
### React 인프런 chap01-05
### React란?

사용자 인터페이스를 만들기 위한 Javascript 라이브러리

리액트를 사용하지 않을 때에는 새로운 브라우저로 이동할 때 리소스를 다시 열어야 했음
→ 서버의 크기가 커지면 곤란

리액트가 만들어짐

### React의 특징

1. 컴포넌트 기반 설계

캡슐화 되어 관리가 쉬움

1. virtual DOM

![image.png](attachment:b3a31aad-bbad-4bf0-86a0-fa4fa72d6309:image.png)

가상의 돔을 만들고 실제 돔을 바꿈

# JSX

### JSX란?

Javascript + HTML

**특징**

- 태그를 명시적으로 달아주어야 함
- 하나의 태그로 감싸져 있어야 함
- HTML과 비슷하지만 태그의 속성 이름이 조금씩 다름
    - class → className
    - for → htmlFor
    - onclick → onClick

```html
// 잘못된 코드
<button class="btn">Hello, world!</button>
<input type="text">
```

```html
// 올바른 코드
<div>
	<button class="btn">Hello, world!</button>
	<input type="text"/>
</div>
```

### JSX에서 Javascript 사용하기

index.js 파일 생성

```jsx
// 예제 코드
const Button = props => {
  const { kind, ...other } = props;
  const className = kind === "primary" ? "PrimaryButton" : "SecondaryButton";
  return <button className={className} {...other} />;
};

const App = () => {
  return (
    <div>
      <Button kind="primary" onClick={() => console.log("clicked!")}>
        Hello World!
      </Button>
    </div>
  );
};
```

### JSX 조건문

조건문에서 false값은 출력되지 않고(화면에서 보여지지 않음) true값만 출력되기 때문에 이를 이용한 연산을 많이 사용함

⭐앞으로 많이 사용하는 방식

- 삼항연산자
- AND 연산자 : A & B
- OR 연산자 : A | B

    ‘A가 참이면 B를 출력한다’는 식의 조건문으로 활용함


if문 - 즉시 실행 함수

js에서 많이 사용하는 방식은 아님

### JSX 반복문

반복문을 사용하려면 각각의 속성마다 key값을 넣어주어야 함

배열을 전부 출력하는 방식으로 반복문을 사용하는 듯?

### JSX 스타일링

css처럼 style로 묶어서 처리

다른 점? → css와는 다르게 object형태로 나타냄

### 컴포넌트란?

하나의 JSX를 반환하는 함수

**변환 전**

```jsx
function App() {
	return (
		<div>
			<h1>Hello,</h1>
			<h2>World</h2>
		</div>
	);
}
```

**변환 후**

```jsx
// App.js
import Hello from "./Hello.js";
import World from "./World.js";

function App() {
	return (
		<div>
			<Hello></Hello>
			<World></World>
		</div>
	);
}
```

```jsx
// Hello.js
export default function Hello() {
	return <h1>Hello</h1>
}
```

```jsx
// World.js
export default function World() {
	return <h2>World</h2>
}
```

컴포넌트 생성 시 주의사항

- 컴포넌트 이름은 **파스칼 케이스**로

    ex) MyComponent, ArticlePage, UserProfile

- 컴포넌트는 의미단위로 쪼개서 파일을 분리
- 최상위 컴포넌트의 이름은 일반적으로 App
    - 암묵적인 룰이라고 함

### Props

부모 컴포넌트에서 자식 컴포넌트로 내려주는 데이터

여기부터 자바랑 정말 비슷해지는 듯?? extends(상속)와 비슷한 느낌이 든다

```jsx
function App() {
	return (
		<div>
			<MyComponent value={'test'}/>
		</div>
	);
}

function MyComponent(props) {
	return <div>{props.value}</div>;
}
```

- 구조분해할당 구문 활용
- 특정 Props에 기본 값(defaultProps)을 줄 수 있음
- Props는 읽기 전용

### State

컴포넌트 내부에서 사용되는 변수

- state값이 변하면 컴포넌트가 리렌더링 됨
- 렌더링 사이클에서 값이 보존됨

const [state, setter 함수]

```jsx
function App() {
	const [value, setValue] = useState(0);

	return (
		<div> {value} </div>
	);
}
```

여기서 setValue는 **value값을 변경하는 함수의 이름**

어떤 동작으로 창이 바뀌게 된다면 state를 통해 바뀐 값을 적용시켜주어야 함

### Hooks 종류

- useState ⭐⭐

    컴포넌트의 상태를 관리하고 상태가 바뀔 때 마다 React가 **자동으로 UI를 업데이트** 해줌

    ```jsx
    const [state, setState] = useState(initialValue);
    ```

    - `state`: 현재 상태의 값이다. 예를 들어, 버튼 클릭 수를 나타내는 상태라면, `state`는 현재 클릭된 횟수를 담고 있다.
    - `setState`: 상태를 업데이트하는 함수이다. 이 함수를 호출하면 상태가 변경되고, React가 UI를 다시 렌더링한다.
    - `initialValue`: 상태의 초기값이다. 예를 들어, 카운터를 0에서 시작하고 싶다면 `useState(0)`과 같이 초기값을 설정할 수 있다.
- useEffect

    특정 로직의 함수만 실행시키고 싶을 때 사용

    → 성능 개선, 시간이나 메모리 낭비를 줄임

- useCallback
- useMemo, useContext, useREF …

### React 렌더링 과정

Rerendering: 상태가 변경되면 화면을 다시 그림

- 마운트: 컴포넌트가 생성되는 것
- 언마운트 : 컴포넌트가 삭제되는 것

### 이벤트 연결하기

JSX에서 camelCase 형태의 속성에 함수를 전달

```jsx
<button onClick={handleClick}>
	Button
</button>
```

이벤트 함수를 정의할 때는 LifeCycle을 고려해야함

### 이벤트 종류

- Mouse 이벤트
    - onClick : onMouseDown + onMouseUp
    - onMouseDown
    - onMouseUp
    - onMouseEnter
    - onMouseLeave
    - onMouseMove
- Keyboard
    - onKeyDown
    - onKeyUp
    - onKeyPress
- Focus, Form 이벤트
    - onFocus : 요소가 포커스 될 때 발생
    - onBlur : 요소의 포커스가 사라졌을 때 발생
    - onChange : 요소값이 변경되었을 때 발생

### Form

Controlled Component(제어 컴포넌트) : React에 의해 입력 요소의 값이 제어되는 컴포넌트

```jsx
function TextInput() {
	const [text, setText] = useState('');

	return (
		<input
			type="text"
			value={text}
			onChange={(e) => {
				setText(e.target.value);
			}}
		/>
	);
}
```

- TextInput
- Textarea
- CheckBox : true or false로 return
- Uncontrolled


## 02-03
### React 인프런 메모장 프로젝트

### 메모장 앱의 전체적인 틀

- `App.js` : 앱의 전체적인 틀 작성
    - `App.css` : 스타일 작성
    - `MemoComponent.js` : 메모장의 타이틀과 내용 작성
    - `SideBar.js` : 메모장의 사이드 바
        - `MemoList.js` : 여러 메모를 클릭을 통해 불러옴
            - `MemoItem.js` : `MemoList.js`로 받은 클릭으로 어떤 메모가 선택되었는지 알려줌
        - `SideBarHeader.js` : 사이드바의 윗 부분
        - `SideBarFooter.js` : 사이드바의 밑 부분


### **css 정리**

- `display: flex` : 왼쪽 정렬..?
- `flex: 1` : 공간 균등 분배, `flex: <flex-grow> <flex-shrink> <flex-basis>` 의 단축 속성
- `white-space: nowrap` : 텍스트가 줄바꿈 되지 않도록 설정
- `text-overflow: ellipsis` : 넘치는 텍스트를 …(말줄임표)로 표시
- `overflow: hidden` : 부모 요소의 크기를 초과하는 자식 콘텐츠를 보이지 않게 숨김
- `padding: 5px 12px` : 내용(content)과 테두리(border) 사이의 내부 여백을 지정
- `font-size: 2rem` : 글자 크기를 기준값의 2배로 설정
- `opacity: 0.4` : 요소의 투명도 설정
- `justify-content: center` : 가로 정렬
- `align-items: center` : 세로 정렬, 부모 요소에 `display: flex;`가 있어야 동작함
- `margin: auto` : 블록 요소 가운데 정렬
- `outline: none` : 블록 요소가 활성화 되었을 때 테두리

### **함수 컴포넌트의 기본 툴**

```jsx
function Name() {
	return (
		<div>(내용)</div>
		);
}

export default Name;
```

### 이론 정리

- import와 export의 차이
    - export란

        변수로 선언한 것을 내보낸다

        컴포넌트를 만들고 다른 파일에서 사용하게 하기 위해 export로 내보내주는 것

    - import란

        export를 통해 내보내진 것을 가져다 사용하는 것

        ```jsx
        import [export한 것] from [파일 위치]
        ```

- extents (상속)
    - 부모에서 선언
    - 정의를 모두 하며 자식은 메소드
    - 변수 그대로 사용 가능

    부모에서 구현되어 있는 것을 그대로 사용 가능

- 불변성

    객체가 생성된 이후 그 상태를 변경할 수 없는 것

    기존의 값을 바꾸는 것이 아니라 새로운 값을 생성하여 변

    경하는 방식

    - `map()` 함수란?

        배열의 각 요소를 변환하여 새로운 배열을 생성하는 함수

        **예제**

        ```jsx
        {**memos.map((memo, index)** => (
                <MemoItem
                  key={index}
                  onClickItem={() => {
                    setSelectedMemoIndex(index);
                  }}
                  onClickDelete={(e) => {
                    deleteMemo(index);
                    e.preventDefault();
                    e.stopPropagation();
                  }}
                  isSelected={index === selectedMemoIndex}
                >
                  {memo.title}
                </MemoItem>
              ))}
        ```

- **child 속성**
    1. childNode

    ![image.png](attachment:97953ab2-5b14-4dd4-be71-5404b1bf6aab:image.png)

    1. childElement

    ![image.png](attachment:ee4baf68-2c11-4fc5-ac07-4ef85f01c3c3:image.png)

    메모장 코드에서 {children} 사용

    **MemoList.js**

    ```jsx
    <div>
          {memos.map((memo, index) => (
            **<MemoItem
              key={index}
              onClick={() => {
                setSelectedMemoIndex(index);
              }}
              isSelected={index === selectedMemoIndex}
            >
              {memo.title}
            </MemoItem>**
          ))}
        </div>
    ```

    **MemoItem.js**

    ```jsx
    function MemoItem({ **children**, onClick, isSelected }) {
      return (
        <div
          className={"MemoItem" + (isSelected ? " selected" : "")}
          onClick={onClick}
        >
          **{children}**
        </div>
      );
    }

    export default MemoItem;
    ```

    MemoItem.js에서 {children}을 내보내면 MemoList.js에서 children을 받아 <MemoItem />과 같은 형태로 사용


### Local Storage

함수 2가지

1. localStorage.setItem →  문자열 형태로 저장

    ```jsx
    localStorage.setItem('age', 100)
    ```

2. localStorage.getItem → 문자열로 출력

    ```jsx
    localStorage.setItem('age')
    -> '100'
    ```


→ 무조건 문자열 형태로 출력되기 때문에 `JSON.stringify` 혹은 `JSON.parse` 를 통해 저장함


## 02-05
### React 인프런 chap09-14

## Chap09 - 설계

컴포넌트 구분은 간결하게? 그려보면서 하는게 좋은듯

컴포넌트를 나누면서 간단히 이름도 붙여놓으면 파일 생성할 때 편할 것 같음

페이지를 구현할 때는 `step` 이라는 변수명을 사용해서 배열의 인덱스처럼 사용하는 것 같다

1. step = 0일 때

    ![image.png](attachment:4212ad60-7cc3-47ec-875d-70ba1b629da2:image.png)

2. step = 1일 때

    ![image.png](attachment:802cf646-135f-4bb3-bb90-28b1172cfcca:image.png)


## Chap10 - 라우터 적용

### Routing

라우팅이란? 주소에 맞게 적절한 페이지를 로드하는 것

```jsx
import { Route, Routes } from "react-router-dom";

...

function App() {
  return (
    <div className="App">
      <Routes>
        <Route path="/done" element={<CompletionPage />} />
        <Route path="/survey/:surveyId" element={<SurveyPage />}>
          <Route path=":step" element={<SurveyPage />} />
        </Route>
      </Routes>
    </div>
  );
}
```

<Route path=":step" element={<SurveyPage />} />

이렇게 따로 안빼주면 http://localhost:3000/survey/id/0/0이런식으로 뒤에 url이 추가로 붙게됨

root index.js에서는

```
import React from "react";
import ReactDOM from "react-dom/client";
import { BrowserRouter } from "react-router-dom";

import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </React.StrictMode>,
);

```

`BrowserRouter` 를 import 해주어야함

### params?

parameter 매개변수

`useParams()` 사용해서 매개변수처럼 사용할 수 있음

http://localhost:3000/survey/id/0

survey, id가 매개변수에 해당

### navigate Hook

```jsx
import { useNavigate } from "react-router-dom";
```

`useNavigate` import해서 사용

```jsx
<button
  onClick={() => {
    navigate(**`${step - 1}`**);
  }}
>
이전
</button>
```

## Chap11 - 컴포넌트 스타일링

### **styled component의 장점**

1. 자바스크립트처럼 사용 가능
2. 명확하게 구분 가능?

```jsx
const SelectInputWrapper = styled.div`
  display: flex;
  flex-direction: column;
  gap: 24px;
`;

const ItemWrapper = styled.div`
  input[type="checkbox"] {
    display: none;
  }

  input[type="checkbox"] ~ span {
    width: 24px;
    height: 24px;
    border: 3px solid #e2dfdf;
    box-sizing: border-box;
    display: inline-block;
    border-radius: 100%;
    vertical-align: middle;
    margin-right: 10px;
  }

  input[type="checkbox"]:checked ~ span {
    border: 8px solid #6542f1;
  }

  input[type="checkbox"] ~ div {
    font-size: 14px;
    line-height: 18px;
    display: inline-block;
    vertical-align: middle;
  }

  input[type="checkbox"]:checked ~ div {
    font-weight: bold;
  }
`;

```

## Chap12 - 전역 상태 관리

### 전역 상태(Global State)

원래 컴포넌트 내부에 있어야 할 스테이트를 밖으로 빼면서 필요한 컴포넌트만 연결해서 사용하는 것

전역 상태 관리 라이브러리

- Redux
- Recoil
- ContextAPI
- MobX

### Recoil이란?

- Atom
    - 여러 개의 컴포넌트에 연결 가능
    - useState와 비슷한 개념? 저장소?
    - onChange를 통해서 호출

    ```jsx
    const textState = atom({
      key: 'textState',
      default: '',
    });
    ```

    - `useRecoilState()`를 통해 atom을 읽고 쓰게할 수 있음
- Selector
    - Atom에 있는 데이터가 컴포넌트로 갈 때 selector를 거쳐서 가게됨
    - 중간에서 **데이터를 가공**하는 작업을 함

    ```jsx
    const charCountState = selector({
      key: 'charCountState',
      get: ({get}) => {
        const text = get(textState);

        return text.length;
      },
    });
    ```

    - `useRecoilValue()` 훅 통해 charCountState 값을 읽어옴

**전체적인 틀**

- App
    - SurveyPie
        - QuestionBox
            - Title
            - Desc
            - Body
                - SelectInput
                - TextInput
                - TextAreaInput
            - ActionButtons
        - ProgressIndicator
            - Bar
    - CompletionPage

결국 최적화하기 위해 어떤 코드를 따로 빼고 넣어야할지 판단해야함 → recoil을 제대로 쓰는 방법?

## Chap13 - API 연동

### Axios란?

node.js와 브라우저를 위한 Promise 기반 HTTP 클라이언트

서버 사이드에서는 네이티브 node.js의 `http` 모듈을 사용하고, 클라이언트(브라우저)에서는 XMLHttpRequests를 사용

**특징**

- 브라우저를 위해 [XMLHttpRequests](https://developer.mozilla.org/ko/docs/Web/API/XMLHttpRequest) 생성
- node.js를 위해 [http](http://nodejs.org/api/http.html) 요청 생성
- [Promise](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise) API를 지원
- 요청 및 응답 인터셉트
- 요청 및 응답 데이터 변환
- 요청 취소
- JSON 데이터 자동 변환
- [XSRF](https://ko.wikipedia.org/wiki/%EC%82%AC%EC%9D%B4%ED%8A%B8_%EA%B0%84_%EC%9A%94%EC%B2%AD_%EC%9C%84%EC%A1%B0)를 막기위한 클라이언트 사이드 지원

git clone을 통해서 서버를 가져온 후 실행시키면 저장된 데이터 베이스를 확인할 수 있음


## 02-07
### 구글 로그인 구현[1]

# 할 일

기초적인 구글 연동 로그인 구현

로그인 하면 환영합니다!, 로그아웃

### 참고자료

[Google OAuth 로그인 구현](https://velog.io/@nuri00/Google-OAuth-%EB%A1%9C%EA%B7%B8%EC%9D%B8-%EA%B5%AC%ED%98%84)

[🔐 리액트로 구글 로그인 구현해보기 (Google OAuth)](https://velog.io/@049494/%EA%B5%AC%EA%B8%80-%EB%A1%9C%EA%B7%B8%EC%9D%B8)

[구글 소셜 로그인 기능 구현 (react-oauth/google)](https://velog.io/@seongsimk/%EA%B5%AC%EA%B8%80-%EC%86%8C%EC%85%9C-%EB%A1%9C%EA%B7%B8%EC%9D%B8-%EA%B8%B0%EB%8A%A5-%EA%B5%AC%ED%98%84-react-oauthgoogle)

### 패키지 설치

`npm install react-router-dom`

`npm install web-vitals`

`npm install @react-oauth/google@latest`

`npm install jwt-decoode@3.1.2`

- jwt import에서 자꾸 오류가 나서 4.0.0 버전에서 3.1.2 버전으로 다운그레이드

`npm install cross-env --save-dev`

onRank 디렉토리 안에 `npm create-react-app web` 생성

---

## **구글 로그인 과정**

![image.png](attachment:4532d4ba-d566-456a-bc84-59b349dafc5a:image.png)

### **access token 받아오기(JWT)**

Access Token을 발급하기 위해서 session 방식과 JWT방식을 사용하는데 보통 jwt를 많이 사용함

**JWT(Json Web Token)이란?** json 객체에 인증에 필요한 정보들을 담은 후 비밀키로 서명한 토큰

토큰의 형식 ↓

```jsx
header.payload.signature
```

토큰에 사용자의 이름, 등록 시간 등의 정보를 담기 때문에 동시간 사용자가 급증해도 서버를 무리 없이 운영할 수 있음

session과 jwt의 가장 큰 차이는 **session DB**를 사용하냐 사용하지 않아도 되냐의 차이인 듯
session에서는 session DB에 모든 정보가 저장되어있기 때문에 session ID만 주면 됨 페이지를 요정하면 DB에서 정보를 찾음

JWT는 토큰에 모든 정보를 저장하기 때문에 페이지를 요청했을 때 서버는 토큰이 유효한지만 확인하면 됨

### **서버에 데이터를 요청/호출하는 방법(Axios)**

1. fetch함수 사용
    - fetch함수는 비동기적으로 HTTP  요청을 보내고 응답 데이터를 처리할 수 있음
    - Promise를 반환함
    - `response.json()`을 호출해야 데이터를 JSON으로 변환할 수 있음

    ```jsx
    fetch("https://api.example.com/data")
      .then(response => {
        if (!response.ok) {
          throw new Error("Network response was not ok");
        }
        return response.json();
      })
      .then(data => console.log(data))
      .catch(error => console.error("Fetch error:", error));

    ```

2. axios 사용
    - node.js를 위해 http 요청 생성, Promise API 지원

    ```jsx
    import axios from "axios";

    axios.get("https://api.example.com/data")
      .then(response => console.log(response.data))
      .catch(error => console.error("Axios error:", error));

    ```


fetch 함수를 사용하면 데이터를 자동으로 json으로 변환해주지 않기때문에 axios 사용하기로 결정

실제로 단점이 설치해야한다 밖에 없다고 함

구글 로그인을 위해서는 [API 액세스 허용](https://www.notion.so/onRank-1-1917e0a7d0ce80fab412f925abbcdd88?pvs=21)을 받아야함

→ 휘래오빠가 받아놨음

클라이언트 ID :
[57872182024-eqlac1aaaecfcbk1vppfadtd67ch9i16.apps.googleusercontent.com](http://57872182024-eqlac1aaaecfcbk1vppfadtd67ch9i16.apps.googleusercontent.com/)

클라이언트 보안 비밀번호 :

![image.png](attachment:2a2ec924-a96c-4f83-b111-eb1c92ac4f07:799c24d7-2949-4cd7-b250-cec540715457.png)

이 url은 요청 보낼 서버의 url이기 때문에 설정해주면 됨

```jsx
[O// App.js
      const response = await axios.post(
        "http://localhost:8080/login/oauth/add",
        {
          token: credentialResponse.credential,
        },
      );

// .env
REACT_APP_GOOGLE_AUTH_CLIENT_ID=57872182024-eqlac1aaaecfcbk1vppfadtd67ch9i16.apps.googleusercontent.com

```

로그인 버튼을 누르면

![image.png](attachment:bd7e8c8d-2518-43e6-ad51-95a2225c3d28:image.png)

**400 오류: redirect_uri_mismatch** 발생..

구글 클라우드에서 localhost:3000을 추가해야할 것 같은데…

로컬 호스트에 추가해서 엑세스 차단 해제 완료!

![image.png](attachment:53bf6f78-0a1b-45ee-a329-e746f8f483f2:image.png)

### Google OAuth 로그인 버튼 및 로그인 처리

`import { GoogleLogin, googleLogout } from "@react-oauth/google";`

GoogleLogin을 통해 로그인 버튼을 랜더링 할 수 있음

```jsx
<GoogleLogin onSuccess={handleLoginSuccess} onError={handleLoginError} />
```

로그인을 성공한다면 `handleLoginSuccess`함수 실행
실패한다면 `handleLoginError` 함수 실행

만약 로그인을 성공한다면 백엔드에 로그인한 정보를 보내줘야함
그때 사용하는게 **jwt 토큰**
구글에서 반환한 `credentialResponse.credential` 을 디코딩하여 사용자 정보를 불러옴

`setUser(decoded)` 를 통해 user에 저장

axios를 이용하여 백엔드 서버에 토큰 전달

- axios에 대한 자세한 설명

    axios는 **비동기 요청을 처리하기 때문에** `async/await` 또는 `.then()` 을 사용할 수 있음

    비동기 함수란? 실행되는 동안 코드의 흐름을 멈추지 않고 다른 작업을 계속할 수 있는 함수

    - async : 함수 앞에 붙이면 항상 promise를 반환하는 비동기 함수가 됨

        → 바로바로 실행 가능한 코드를 작성하기 위함!

    - await : promise가 완료될 때 까지 기다렸다가 결과 반영

        → 해당 작업이 끝날 때 까지 기다려줌


    **HTTP 요청 - GET, POST, PUT, DELETE 등이 있음**

    1. GET 요청 (데이터 가져오기)

        ```jsx
        const fetchData = async () => {
          try {
            const response = await axios.get("https://api.example.com/users");
            console.log(response.data); // 서버에서 받은 데이터 출력
          } catch (error) {
            console.error("데이터 가져오기 실패:", error);
          }
        };

        ```

    2. POST 요청 (데이터 생성)

        ```jsx
        const sendData = async () => {
          try {
            const response = await axios.post("https://api.example.com/users", {
              name: "John Doe",
              age: 30,
            });
            console.log(response.data);
          } catch (error) {
            console.error("데이터 전송 실패:", error);
          }
        };

        ```

    3. PUT 요청 (데이터 수정)

        ```jsx
        const updateData = async () => {
          try {
            const response = await axios.put("https://api.example.com/users/1", {
              name: "John Smith",
            });
            console.log(response.data);
          } catch (error) {
            console.error("데이터 수정 실패:", error);
          }
        };

        ```

    4. DELETE 요청 (부분 수정)

        ```jsx
        const updatePartialData = async () => {
          try {
            const response = await axios.patch("https://api.example.com/users/1", {
              age: 35,
            });
            console.log(response.data);
          } catch (error) {
            console.error("데이터 부분 수정 실패:", error);
          }
        };

        ```


로그아웃 처리를 하고싶다면 googleLogout함수를 사용하면 됨

### useState 사용

useState는 컴포넌트의 상태를 관리하는 Hook

상태란 컴포넌트가 변화하는 값을 의미 즉, 웹에서의 동작을 통해 상태가 변한다면 useState로 상태를 관리해주어야 함

```jsx
  const [user, setUser] = useState(null);
  const [error, setError] = useState(null);
```

여기에서 user와 setUser를 살펴보면
user는 로그인한 사용자의 정보를 관리하는 역할이고 setUser는 로그인 후 사용자 정보를 **업데이트**하는 역할

## 전체 구현 코드

```jsx
// App.js

import { GoogleLogin, googleLogout } from "@react-oauth/google";
import axios from "axios";
import jwt_decode from "jwt-decode";
import React, { useState } from "react";

function App() {
  const [user, setUser] = useState(null);
  const [error, setError] = useState(null);

  const handleLogout = () => {
    googleLogout();
    setUser(null);
    console.log("로그아웃 성공");
  };

  const handleLoginSuccess = async (credentialResponse) => {
    try {
      const decoded = jwt_decode(credentialResponse.credential);
      setUser(decoded);
      console.log("Google User Info:", decoded);

      const response = await axios.post(
        "http://localhost:8080/login/oauth/add",
        {
          token: credentialResponse.credential,
        },
      );

      console.log("서버 응답:", response.data);
    } catch (err) {
      console.error("로그인 처리 중 오류:", err);
      setError("오류 발생");
    }
  };

  const handleLoginError = () => {
    console.log("로그인 실패");
    setError("Google 로그인 실패");
  };

  return (
    <div>
      <h1>Google Login</h1>
      {user ? (
        <div>
[I          <h2>환영합니다, {user.name}!</h2>
          <img src={user.picture} alt="User Profile" />
          <button onClick={handleLogout}>로그아웃</button>
        </div>
      ) : (
        <GoogleLogin
          onSuccess={handleLoginSuccess}
          onError={handleLoginError}
        />
      )}
    </div>
  );
}

export default App;

```

```jsx
// index.js

import "./index.css";

import { GoogleOAuthProvider } from "@react-oauth/google";
import React from "react";
import ReactDOM from "react-dom/client";

import App from "./App";
import reportWebVitals from "./reportWebVitals";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <React.StrictMode>
    <GoogleOAuthProvider
      clientId={process.env.REACT_APP_GOOGLE_AUTH_CLIENT_ID}
      onScriptLoadError={() => console.log("실패")}
      onScriptLoadSuccess={() => console.log("성공")}
    >
      <App />
    </GoogleOAuthProvider>
  </React.StrictMode>,
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```

## 02-14
### 구글 로그인 구현[2]

# 할 일

코드 수정하고 구글 연동 로그인 하면 회원 정보 입력하는 창으로 넘어가도록 구현

회원정보 입력하면 백엔드로 요청보내고 창은 메인 페이지로 이동

**코드 수정**

- 구글 연동된 창이 새로 생기는게 아니라 기존 창에서 넘어가도록 구현
- 구글 로그인 버튼 이쁘게 만들기 → 사실 와이어 프레임 보고 하면 될듯

- 토큰

    **토큰 전달하고 인증 받는 과정**

    1. 클라이언트 → 서버 : 로그인 요청
    2. 서버 → 클라이언트 : 토큰 생성 후 응답
    3. 클라이언트 : 토큰 저장

        프론트는 이때 토큰을 받아와야함?

    4. 클라이언트 → 서버 : 토큰 정보와 함께 요청

        토큰에 여러 정보들을 담아서 서버에 요청

    5. 서버 : 토큰 검증
    6. 서버 → 클라이언트 : 응답

    **리프레시 토큰과 엑세스 토큰**

    토큰 유효기간이 너무 길면 탈취 당할 수도 있음
    토큰 유효기간이 너무 짧으면 사용자가 불편해짐

    이 문제를 해결하기 위해 → **리프레시 토큰**이 있음

    ![image.png](attachment:ea308ac2-5f43-4121-b9d3-94d9dc37289a:image.png)

    1. 클라이언트 → 서버 : 인증요청
    2. 서버 → 클라이언트 : 엑세스 토큰, 리프레시 토큰 응답
    3. **서버 → DB : 리프레시 토큰 저장**

    …

    1. 서버 → 클라이언트 : 토큰 만료 응답
    2. 클라이언트 → 서버 : 엑세스 토큰 발급 요청
    3. 서버 → DB : 리프레시 토큰 조회, 유효성 검사
    4. 서버 → 클라이언트 : 새로운 액세스 토큰 응답

    **예제 코드**

    백엔드에서 액세스 토큰과 리프레시 토큰을 전송해주는데 이때 프론트는
    엑세스 토큰을 **메모리 또는 상태에 저장**, 리프레시 토큰을 **HttpOnly 쿠키(자동 저장됨)** 로 관리하는 것이 일반적

    ```jsx
    import axios from "axios";

    const API_URL = "https://your-api.com";

    export const login = async (email, password) => {
      try {
        const response = await axios.post(`${API_URL}/auth/login`, {
          email,
          password,
        });

        // 서버 응답에서 엑세스 토큰 받아오기
        const accessToken = response.data.accessToken; // 보통 JSON 형태로 응답됨
        localStorage.setItem("accessToken", accessToken); // 임시 저장 (보안 취약하므로 실제 앱에서는 메모리 저장이 더 좋음)

        return response.data;
      } catch (error) {
        console.error("Login failed", error);
      }
    };

    ```

    `withCredentials: true` 를 통해 쿠키 설정,
    API 요청을 보낼 때는 **엑세스 토큰을 헤더에 포함**해야 함

    ```jsx
    export const fetchUserData = async () => {
      try {
        const accessToken = localStorage.getItem("accessToken"); // 저장된 토큰 가져오기

        const response = await axios.get(`${API_URL}/user/me`, {
          headers: {
            Authorization: `Bearer ${accessToken}`, // 엑세스 토큰을 포함
          },
          withCredentials: true, // 쿠키 포함 (리프레시 토큰 자동 전송)
        });

        return response.data;
      } catch (error) {
        console.error("Failed to fetch user data", error);
      }
    };
    ```

    리프레시 토큰을 이용해 새로운 엑세스 토큰 요청

    ```jsx
    export const refreshAccessToken = async () => {
      try {
        const response = await axios.post(`${API_URL}/auth/refresh-token`, {}, {
          withCredentials: true, // 쿠키에 저장된 리프레시 토큰 자동 전송
        });

        const newAccessToken = response.data.accessToken;
        localStorage.setItem("accessToken", newAccessToken); // 새로운 토큰 저장

        return newAccessToken;
      } catch (error) {
        console.error("Token refresh failed", error);
        return null;
      }
    };
    ```


## 기본 설정

### URL 설정

로그인 화면: `/auth/oauth`

메인 페이지: `/`

회원가입 화면: `/auth/add`

### API 설정

구글 소셜 로그인 : `/auth/oauth/check`

회원 정보 입력 : `/auth/add`

### 컴포넌트 분리

```jsx
src/
│── api/
│   └── index.js  # API 관련 코드
│
│── components/oauth/  # OAuth 관련 UI 컴포넌트
│   ├── FormInput/
│   │   └── index.js
│   ├── GoogleLoginButton/
│   │   ├── index.js
│   │   └── index.css
│   ├── LoginAddForm/
│   │   └── index.js
│
│── hooks/
│   └── useForm.js  # 커스텀 훅 관련 코드
│
│── mocks/  # Mock API 관련 파일
│   ├── browser.js
│   ├── handler.js
│   ├── server.js
│
│── pages/  # 페이지 단위 컴포넌트
│   ├── oauth/
│   │   ├── Login/
│   │   │   ├── index.js
│   │   │   └── index.css
│   │   ├── LoginAdd/
│   │   │   ├── index.js
│   │   │   └── index.css
│   ├── studies/
│   │   └── Main/
│   │       └── index.js
│
│── App.css
│── App.js

```

**꼭 해야하는거**

1. 구글 로그인 성공
2. isNewUser 받아서 페이지 이동
3. 회원정보 입력 후 name, phoneNumber, school, department 백엔드한테 POST해주기

구현하면서 가장 어려웠던 부분은 어떤 동작에서 백엔드한테 정보를 넘겨줘야할지..
보다는 url이랑 api를 헷갈려하고있던 것 같음

그리고 휘래오빠가 말했던게 로그인을 했을 때 기존 회원인지 신규 회원인지 구별하는 방법을 어떻게할지가 문제였다 하지만 지선생님의 도움을 받아서 isNewUser라는 bool값을 이용하라는 힌트를 얻음


## 02-18
### 공지사항 구현[1]

# 공지사항(Notice) 기능 정리

공지사항(Notice) 기능을 구현하여 사용자에게 중요한 정보 및 업데이트를 전달할 수 있도록 함

**주요 기능**

- 공지사항 목록 조회
- 공지사항 상세 조회
- 관리자 권한으로 공지사항 작성/수정/삭제
- 공지사항의 중요도 표시 (예: 일반, 중요, 긴급)
- 공지사항 작성 날짜 및 작성자 정보 표시
- 공지사항 검색 및 필터링 기능

## UI 구성

### 공지사항 목록 페이지

- 제목
- 작성자
- 작성 날짜
- 중요도 표시 (색상 또는 아이콘 활용)
- 페이지네이션 적용

### 공지사항 상세 페이지

- 제목
- 작성자 및 작성 날짜
- 공지 내용
- 첨부파일 다운로드 기능 (선택사항)

### 공지사항 작성/수정 페이지 (관리자용)

- 제목 입력 필드
- 내용 입력 필드 (Markdown 또는 WYSIWYG 에디터 사용 가능)
- 중요도 선택 (드롭다운 또는 버튼 그룹)
- 파일 업로드 기능 (선택사항)
- 저장 및 취소 버튼

### 공지사항 목록 조회 (GET 요청)

```jsx
import axios from "axios";
import { useEffect, useState } from "react";

function NoticeList() {
  const [notices, setNotices] = useState([]);

  useEffect(() => {
    axios.get("http://localhost:8080/api/notices")
      .then(response => setNotices(response.data))
      .catch(error => console.error("공지사항 가져오기 실패:", error));
  }, []);

  return (
    <div>
      <h1>공지사항</h1>
      <ul>
        {notices.map(notice => (
          <li key={notice.id}>{notice.title} - {notice.author}</li>
        ))}
      </ul>
    </div>
  );
}
export default NoticeList;

```

### 공지사항 작성 (POST 요청)

```jsx
const createNotice = async (title, content, priority) => {
  try {
    const response = await axios.post("http://localhost:8080/api/notices", {
      title,
      content,
      priority
    });
    console.log("공지사항 등록 완료:", response.data);
  } catch (error) {
    console.error("공지사항 등록 실패:", error);
  }
};

```

### 공지사항 수정 (PUT 요청)

```jsx
const updateNotice = async (id, title, content, priority) => {
  try {
    const response = await axios.put(`http://localhost:8080/api/notices/${id}`, {
      title,
      content,
      priority
    });
    console.log("공지사항 수정 완료:", response.data);
  } catch (error) {
    console.error("공지사항 수정 실패:", error);
  }
};

```

### 공지사항 삭제 (DELETE 요청)

```jsx
const deleteNotice = async (id) => {
  try {
    await axios.delete(`http://localhost:8080/api/notices/${id}`);
    console.log("공지사항 삭제 완료");
  } catch (error) {
    console.error("공지사항 삭제 실패:", error);
  }
};

```
