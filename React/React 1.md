## React 1

### 리액트

페이스북에서 개발하고 관리하는 UI 라이브러리

UI를 제외한 나머지는 개발자가 다 해야하기 때문에, 진입장벽이 높다.

*Create-react-app : 리액트의 진입장벽을 낮추기위해 제공*

작업 디렉터리를 생성

#1. 명령 프롬프트(cmd.exe) 실행

#2. 작업 디렉터리 생성

``` 
C:\USER\HPE> mkdir C:\react
C:\USER\HPE> cd C:\react
C:\react>
```

#3. visual studio code 실행

#4. File > Open Folder > C:\react 를 선택 후 Open

#5. create-react-app 패키지 설치

```
C:\react> npm install -g create-react-app
```

#6. create-react-app으로 리액트 프로젝트 생성

```
C:\react> create-react-app hello-react
```

#7. 디렉터리 이동 후 실행

```
C:\react> cd hello-react
c:\react> npm start
```

![image-20200204095308916](images/image-20200204095308916.png)

<img src="images/image-20200204095125326.png" alt="image-20200204095125326" style="zoom: 25%;" />



스테이트가 바뀌면 값이 렌더링되어 사용자에게 보여지는 것 = UI
*UI = render (state)*

가상 돔 : UI를 빠르게 업데이트
				이전 UI 상태를 메모리에 유지, 변경될 UI의 최소 집합을 계산하는 기술
				전체 문서에 대해 변경된 부분들만 감지하여 바꾸는 것, 빠르고 효율적

#### p.3 리액트 개발 환경 직접 구축 ⇒  외부 패키지를 사용하지 않고 리액트 웹 페이지 제작

\#1 작업 디렉터리 생성(Visual Studio Code)

```
C:\react\hello-world
```

![image-20200204102842181](images/image-20200204102842181.png)

리액트 라이브러리 다운로드
https://unpkg.com/react@16.12.0/umd/react.development.js
https://unpkg.com/react@16.12.0/umd/react.production.min.js
https://unpkg.com/react-dom@16.12.0/umd/react-dom.development.js
https://unpkg.com/react-dom@16.12.0/umd/react-dom.production.min.js

<img src="images/image-20200204102512861.png" alt="image-20200204102512861" style="zoom:33%;" />

<img src="images/image-20200204103012722.png" alt="image-20200204103012722" style="zoom: 33%;" />

- Development ⇒ 개발 환경에서 사용파는 파일 → 에러 메시지 확인이 가능
- Production ⇒ 실행(배포) 환경에서 사용하는 파일
- react ⇒ 플랫폼 구분 없이 공통으로 사용되는 파일 (리액트 코어)
- React-dom ⇒ 웹 환경에서 사용되는 파일

#3. C:\react\hello-world\sample1.html,   C:\react\hello-world\sample1.js 파일생성

![image-20200204103125877](images/image-20200204103125877.png)

#4 아래 화면과 같은 출력을 제공하는 sample1.html 작성

### 안녕하세요

<button>좋아요</button> 			<== "좋아요" 상태에서 버튼을 클릭하면 "좋아요 취소"로 변경

#4-1 react를 사용하지 않고 처리

<img src="images/image-20200204103815715.png" alt="image-20200204103815715" style="zoom:80%;" />

#4-2 react 기반으로 구현

<img src="images/image-20200204112410341.png" alt="image-20200204112410341" style="zoom:80%;" />



<img src="images/image-20200204130743078.png" alt="image-20200204130743078" style="zoom:80%;" />

<img src="images/image-20200204130721780.png" alt="image-20200204130721780" style="zoom:80%;" />



* liked 라는 상태변수를 가지고 있음

* 정의된 것을 내 입맛대로 바꾸는 것 = 상속

* 정의 = React.Component class에 이벤트처리, 동작 등이 정의되어있다. (extends-확장,)

* Component에서 정의한 것을 최초로 실행하는 것 = Constructor 

* Super = 상위 계층 

* State 변수 정의 (props:부모로부터 전달받은 값, state:자기자신이 갖고있는 값)

* 자기 자신은 liked라는 값을 가지고 있는 것이다.

* render : 사용자 화면에 보여주는 것, button 을 Return함.
  여기에 text로 보여져야 함
  return 으로 보여지는 값 : React.createElement → 태그를 만들어주는 것

* Set method를 이용해 상태를 바꿔줘야 함.

* ReactDOM의 render 함수를 이용하여 react.createElement - 태그를 만들어준다.

* #react-root : 아이디가 react-root인 것을 가져옴  <div id=react-root>

* 첫 번째 : 내가 만들 태그(문자 : html--위의 'button', 
  react.create는 리액트 컴포넌트--'Likebutton')

* #react-root : 아이디가 react-root인 것을 가져옴  <div id=react-root>

* 현재 상태의 반대로 바꾸려면

  ![image-20200204113133972](images/image-20200204113133972.png)

상태 변수에 따라 값을 바꿔줌

개발자는 어떤 사용자의 UI 또는 네트워크에서 가져온 데이터의 변화에 따라 변경된 내용만 반영될 수 있다면 빠르게 자동으로 update 된다.  → React를 사용하는 이유.

* return : 메소드의 인자를 반환(인자의 메소드)
* Setstate : 소괄호 - 함수
* Onclick: ()----> 함수. 

```
=> this.setState({ liked: !this.state.liked }) 이게 함수절
```

```
{ OnClick: () => {
	console.log(this.state.liked);
	this.setState({ liked: !this.state.liked})''
}},
```



#5 http-server를 실행해서 확인
Terminal - New Terminal

```
C:\react> npx http-server
```

<img src="images/image-20200204103919618.png" alt="image-20200204103919618" style="zoom:80%;" />

#5-1 Jquery 기반

```
https://jquery.com/download/
```

<img src="images/image-20200204105136469.png" alt="image-20200204105136469" style="zoom:80%;" />

![image-20200204104749256](images/image-20200204104749256.png)

![image-20200204104927561](images/image-20200204104927561.png)

![image-20200204105029372](images/image-20200204105029372.png)

![image-20200204125415661](images/image-20200204125415661.png)

![image-20200204125425017](images/image-20200204125425017.png)



![image-20200204131205929](images/image-20200204131205929.png)

![image-20200204131313622](images/image-20200204131313622.png)



### p.9 바벨(babel)사용

#### 바벨

자바스크립트 코드를 변환해주는 compiler
최신 문법을 사용하는 용도 외에도 다양하게 활용될 수 있다.

<ol>
    <li>주석 제거</li>
    <li>코드 압축</li>
</ol>

##### 플러그인

바벨은 자바스크립트 파일을 입력으로 받아서 또 다른 자바스크립트 파일을 출력으로 준다.
자바스크립트 파일을 변환해 주는 작업은 **플러그인** 단위로 이루어진다.
*두 번의 변환이 필요하다 = 두 개의 플러그인을 사용한다.*

##### 프리셋(preset)

하나의 목적을 위해 여러 개의 플러그인이 필요할 수 있는데, 이러한 플러그인의 집합



#1. 증가, 감소 버튼으로 count 상태값을 변경하는 코드를 작성

![image-20200204132713335](images/image-20200204132713335.png)

sample3.html

![image-20200204132854213](images/image-20200204132854213.png)



<img src="images/image-20200204133558079.png" alt="image-20200204133558079" style="zoom:80%;" />

![image-20200204133606153](images/image-20200204133606153.png)



## 템플릿

```
<html>
    <body>
        <h2>프로젝트가 마음에 들면 좋아요 버튼을 클릭해 주세요</h2>
        <div id="react-root"></div>

        <script src="react.development.js"></script>
        <script src="react-dom.development.js"></script>
        <script>
            class LikeButton extends React.Component {
                constructor(props) {
                    super(props);
                    this.state = { liked: false };
                }
                render() {
                    const text = this.state.liked ? '좋아요 취소' : '좋아요';
                    return React.createElement(
                        'button', 
                        { onClick: () => this.setState({ liked: !this.state.liked }) },
                        text,
                    );
                }
            }
            // P9 코드1-6 참조
            class Container extends React.Component {
                constructor(props) {
                    super(props);
                    this.state = { count: 0 };
                }
                render() {
                    return React.createElement(
                        'div',
                        null, 
                        React.createElement(LikeButton), 
                        React.createElement(
                            'div',
                            { style: { marginTop: 20 } }, 
                            React.createElement('span', null, '현재 카운트: '),
                            React.createElement('span', null, this.state.count), 
                            React.createElement(
                                'button', 
                                { onClick: () => this.setState({ count: this.state.count + 1 })},
                                '증가',
                            ),
                            React.createElement(
                                'button', 
                                { onClick: () => this.setState({ count: this.state.count -1 })},
                                '감소',
                            ),
                        ),
                    );
                }
            }

            ReactDOM.render(
                React.createElement(Container), 
                document.querySelector('#react-root')
            );
        </script>
    </body>
</html>

```

![image-20200204141438283](images/image-20200204141438283.png)

#1-3 JSX 버전으로 변경

C:\react\hello-world\sample4.html

```
<html>
	<body>
		<h2>프로젝트가 마음에 들면 좋아요 버튼을 클릭해 주세요<h2>
		<div id="react-root"</div>
		
		<script src="react.development.js"></script>
		<script src="react-dom.development.js"></script>
		<script src="sample4.js"></script>
	<body>
<html>
```

![image-20200204141900932](images/image-20200204141900932.png)



C:\react\hello-world\src\sample4.js (수정전: #1-2 코드 일부를 이전)

```
class LikeButton extends React.Component {
    constructor(props) {
        super(props);
        this.state = { liked: false };
    }
    render() {
        const text = this.state.liked ? '좋아요 취소' : '좋아요';
        return React.createElement(
            'button', 
            { onClick: () => this.setState({ liked: !this.state.liked }) },
            text,
        );
    }
}
// P9 코드1-6 참조
class Container extends React.Component {
    constructor(props) {
        super(props);
        this.state = { count: 0 };
    }
    render() {
        return React.createElement(
            'div',
            null, 
            React.createElement(LikeButton), 
            React.createElement(
                'div',
```

<img src="images/image-20200204142631239.png" alt="image-20200204142631239" style="zoom:80%;" />



#2 바벨 패키지를 설치하고 JavaScript를 변환(Compile)

* babel 패키지 설치

```
C:\react\hello-world> npm install @babel/core @babel/cli @babel/preset-react
```

* 자바스크립트 파일 변환<img src="images/image-20200204150638346.png" alt="image-20200204150638346" style="zoom:80%;" />

```
C:\react\hello-world>npx babel --watch ./src --out-dir ./ --presets @babel/preset-react
```

![image-20200204150707668](images/image-20200204150707668.png)



### P.14 웹팩(webpack)

물리적인 특정 위치와 매핑

Cache : 일정 시간동안 가지고 있는 것, 캐시를 사용하지 않기 위해 [npx http-server -c-1] 한다.

##### ESM

웹팩은 ESM과 commonJS를 모두 지원하는데, 이들 모듈 시스템을 이용해서 코드를 작성하고 웹팩을 실행하면 예전 버전의 브라우저에서도 동작하는 자바스크립트 코드를 만들 수 있다.

// file1.js

export default function funct1() {...}
export function func2() {...}
export const variable1 = 123;
export let variable2 = 'hello';

- export default 해도 되고, 여러 개 export 구문을 통해 함수를 다른 파일에서 쓸 수 있다.

//file2.js

import myFunc1, { func2, variable1, variable2 } from './file1.js';

//file3.js

import { func2 as myFunc2 } from './file1.js';

**default로 하면 이런 형태를 생략하고 쓸 수 있다. 이런 형태를 모듈 문법이라고 한다**

#1 작업 디렉터리 생성

```
C:\react> mkdir webpack-test
C:\react> cd webpack-test
C:\react\webpack-test> npm init -y
C:\react\webpack-test> mkdir src
```

![image-20200204154026062](images/image-20200204154026062.png)

#2 외부패키지 설치

```
C:\react\webpack-test>npm install webpack-cli react react-dom
```



#3 코드 작성

#3-1 C:\react\webpack-test\index.html

![image-20200204154648655](images/image-20200204154648655.png)

#3-2 C:\react\webpack-test\src\index.js

<img src="images/image-20200204154637364.png" alt="image-20200204154637364"  />

*중괄호를 안썼다면 default를 가져가겠다.*

<img src="images/image-20200204155055702.png" alt="image-20200204155055702" style="zoom:80%;" />

#3-3 C:\react\webpack-test\src\button.js

![image-20200204155421899](images/image-20200204155421899.png)

<ul>
    <li>props : 속성 => 부모 컴포넌트가 전달</li>
    <li>State : 상태 => 자신, 보유값(해당 컴포넌트)</li>
</ul>



#4 웹팩을 이용해서 두개의 자바스크립트 파일을 하나로 결합 

```
C:\react\webpack-test> npx webpack
```

![image-20200204162757209](images/image-20200204162757209.png)

### P.18 create-react-app 으로 시작하기

- 리액트로 웹 애플리케이션을 만들기 위한 환경을 제공
- 바벨과 웹팩도 포함
- 테스트, HMR(Hot-Module-Replacement), ES6+ 문법, CSS 후처리 등을 제공



#1 개발 환경 설정

```
C:\react>cd c:\react
C:\react>npx create-react-app cra-test
C:\react>cd cra-test
```

#2  개발 서버 실행

```
C:\react\cra-test>npm start
```

⇒ 브라우저가 자동으로 http://localhost:3000/ 접속

<img src="images/image-20200204165152491.png" alt="image-20200204165152491" style="zoom:50%;" />

특별한 이유가 없다면 index.html에 직접 연결하는 것보다는 src 폴더 밑에서 import 키워드를 사용해서 포함시키는 게 좋다.

![image-20200204165436831](images/image-20200204165436831.png)

**중괄호가 나오는 순간 JSX 이다**  (그전까진 html과 다를 바 없음)

#3 빌드하기

```
C:\react\cra-test>npm run build
```

<img src="images/image-20200204170121796.png" alt="image-20200204170121796"  />

자바스크립트 파일에서 import 키워드를 이용해서 가져온 CSS 파일 → 
build/static/css/main.{해시값}.chunk.css 파일에 모두 저장

자바스크립트 파일에서 import 키워드를 이용해서 가져온 PONT, IMAGE 등의 리소스 파일 → 
build/statkc/media 폴더에 저장 (10k 이하의 작은 파일은 data url 형식으로 자바스크립트 파일에 저장)



<ul>
<h6>[해쉬(Hash)]</h6>
    <li>임의 크기 입력 → 고정 크기 출력</li>
    <li>유일성 보장 a≠b → H(a)≠H(b)  ⇒ 무결성 보장<br>
		무결성을 체크하는 방법은 항상 해시로 한다.</li>
    <li>단방향성 = 일방향성<br>
		인증 정보 저장·처리(Authorization)</li>
    <li>빠른 연산</li>
    <li>충돌 회피</li>
</ul>

<ol>
<h6>[Tupel]</h6>
    <li>지식</li>
    <li>소유</li>
    <li>특징</li>
</ol>

---

구글 이미지 검색 → 큰 이미지, 작은 이미지 각각 C:\react\cra-test\src 로 다운로드

![image-20200204174133246](images/image-20200204174133246.png)

![image-20200204174141610](images/image-20200204174141610.png)



#### 1.3.4 코드 분할하기(p.27)

visual studio code 에서 src 내에 새 파일 생성하기

![image-20200205100039144](images/image-20200205100039144.png)

#1 코드를 분할하지 않고 사용



C:\react\cra-test\src\Todo.js

```
// P27 코드 1-20
import React from 'react';

export function Todo({ title }) {
    return <div>{title}</div>;
}

export default Todo;
```



C:\react\cra-test\src\TodoList.js

<img src="images/image-20200205095606810.png" alt="image-20200205095606810" style="zoom:80%;" />

C:\react\cra-test\src\App.js

![image-20200205095645756](images/image-20200205095645756.png)

#개발 서버 실행 (CMD에서 실행)

```
C:\react\cra-test> npm start
```

npm start를 하면 3000번 포트가 열리면서 이러한 창이 나타난다.

![image-20200205102546678](images/image-20200205102546678.png)

#2 코드 분할을 통해서 동적으로 자바스크립트 파일을 로딩

```
C:\react\cra-test\src\TodoList.js
```

⇒ main.chunck.js 파일에 Todo.js 파일의 본문이 포함되지 않음
→ "할일추가" 버튼을 클릭하면 2.chunck.js 파일(Todo.js 파일의 본문 내용을 포함)이 내려옴
→ 2.chunck.js 파일은 최초 한번만 다운로드

![image-20200205104726129](images/image-20200205104726129.png)





