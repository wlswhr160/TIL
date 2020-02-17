# JavaScript

* 웹  브라우저에서 많이 사용하는 프로그래밍 언어
* 넷스케이프 사의 브랜든 아이히(Brendan Eich)에 의해 모카라는 이름으로 시작 (모카 □ 라이브 스크립트로 이름 변경)
* 넷스케이프 사가 썬 마이크로시스템과 함꼐 자바스크립트라는 이름을 붙이고 본격적 발전



### 자바 스크립트의 활용

#### 웹에서 웹 애플리케이션으로

**초기의 웹**

* 변화 없는 정적 글자들의 나열
* 웹은 하이퍼링크라는 매개체를 사용해 웹 문서가 연결된 거대한 책에 불과

**자바스크립트의 등장**

* 웹 문서의 내용을 동적으로 바꾸거나 마우스 클릭 같은 이벤트로 처리

**웹은 애플리케이션의 모습에 점점 가까워짐**

* 대표적인 예는 웹 오피스 같은 문서 작성 도구
* 구글, 마이크로소프트에서는 웹 브라우저만으로 워드, 엑셀, 파워포인트 같은 애플리케이션 사용 가능
* 웹 애플리케이션은 웹 브라우저만 있으면 언제 어디서나 사용 가능

#### 인터넷 연결 없이 웹 브라우저에서 실행 가능한 웹 애플리케이션

* 스마트폰이나 스마트패드 내의 애플리케이션을 만들 때에도 자바스크립트 사용



### 1.3 자바스크립트의 종류

* 유럽 컴퓨터 제조협회(ECMA)는 자바스크립트를 ECMAScript라는 이름으로 표준화
* 웹 브라우저나 애플리케이션에 내장된 자바스크립트의 종류
* ECMAScript(ES)와 Jscript는 모두 자바스크립트를 의미



### 1.6 HTML 파일 만들기

#### HTML 파일을 만들고 실행하는 방법

* [파일] → [새 파일] 을 선택해 새 파일 대화상자 열기
* HTML 페이지 선택해 파일 생성 → 코드 생성

***Markup 언어 : 다른 환경의 machine간의 정보를 교환하기 위해 고안된 언어***
***정보를 표현하기 위한 수단.***  ex) <h1> 1234 </h1> 
***브라우저별로 경쟁이 붙는다  = 호환성이 떨어지게 된다. = 이용 편의성이 떨어진다.***

***→그래서 나온 것이 HTML5 표준 형식의 코드***

* 자동화 처리의 가능 : html5에서 추구하고자 하는 의미기반적 웹(시맨틱 웹) 이다. 의미기반의 태그 추가
  시맨틱 웹 : 의미기반적 웹

* 개발편의성 : 정규화(Normalization) 과정을 입력단에서부터 함으로서 편의를 제공. (ex, 예약 날짜 설정 - 달력 버튼)
  

[docktype](https://www.w3schools.com/tags/tag_doctype.asp)
→ 문서를 해석하는 사람에게 이 문서가 어떤 버전의 어떤 구조를 가지고 있는지 알려주는 사이트
     브라우저가 사용자 환경에 맞게 설정해주도록 도와주는 것. = 브라우저 편의를 위한 것



#### code 1-3.html

```
<div> 는 태그명, id="mydiv"는 속성, 그 사이는 값, </div>
기호로 싸여있는 것을 렌더링 한다 라고 한다. (그림, 글자)
```

![1](C:\Users\HPE\Desktop\1.JPG)

![2](C:\Users\HPE\Desktop\2.JPG)

`URI`

- URL : http://www.naver.com/abc - 유니크하게 정보를 식별하는 방법. 위치를 기반으로 식별

  ```
  http = 스킴, www.naver.com = 호스트, /abc = 경로
  ```

  

- URN



### http-server 설치

```
C:\Users\HPE\Downloads\java>node --version
v12.14.1
C:\Users\HPE\Downloads\java>npm init -y
C:\Users\HPE\Downloads\java>npm install http-server -g
```

![http-server](C:\Users\HPE\Desktop\http-server.JPG)



```
C:\Users\HPE\Downloads\java>npx http-server   → 엑세스 허용
Starting up http-server, serving ./
Available on:
  http://10.0.75.1:8080
  http://59.29.224.84:8080
  http://192.168.56.1:8080
  http://192.168.174.1:8080
  http://10.0.0.1:8080
  http://127.0.0.1:8080
  http://172.21.111.145:8080
Hit CTRL-C to stop the server  
```

![8080](C:\Users\HPE\Desktop\8080.JPG)

#### console log로 나타내기

![F12](C:\Users\HPE\Desktop\F12.JPG)

![console](C:\Users\HPE\Desktop\console.JPG)

![샵1샵2](C:\Users\HPE\Desktop\샵1샵2.JPG)

#### up, down 추가

![up down](C:\Users\HPE\Desktop\up down.JPG)

![updown](C:\Users\HPE\Desktop\updown.JPG)



#### Innertext 추가

![innertext](C:\Users\HPE\Desktop\innertext.JPG)

![up 대문자](C:\Users\HPE\Desktop\up 대문자.JPG)

![image-20200122135019490](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200122135019490.png)

> 이렇게 했을때, 순차적으로 내용을 바꾸는데, down의 위치에 있지 않기 때문에 오류가 난다.



![image-20200122135239510](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200122135239510.png)

> 이렇게 down 밑에 적어주면 가능하다.