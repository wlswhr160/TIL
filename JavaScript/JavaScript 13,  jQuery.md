## JavaScript 13,  jQuery

p. 407

---

### jQuery

* 모든 브라우저에서 동작하는 클라이언트 자바스크립트 라이브러리
* 2006년 1월 존 레식(John Resig)이 BarCamp NYC에서 발표
* 무료로 사용 가능한 오픈 소스 라이브러리
* jQuery는 다음 기능을 위해 제작됨
  * 문서 객체 모델과 관련된 처리를 쉽게 구현
  * 일관된 이벤트 연결을 쉽게 구현
  * 시각적 효과를 쉽게 구현
  * ajax 애플리케이션을 쉽게 개발
* 다운로드 → https://jquery.com/download/

페이지 전체가 가는게 아니고 데이터만 감. 이 데이터는 화면의 출력된(보여질) 데이터만 서버에서 만들어서 주는 것임. 그것이 가능하도록 하는 기수이 ajax. JavaScript를 이용해서 화면에 보이도록 함


**CDN 사용**

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>

**설치해서 사용**

C:\javascript>npm install jquery

![image-20200129151043240](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129151043240.png)



### p.415 $(document).ready()

![image-20200129153258072](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129153258072.png)

### p.417 기본 선택자

```
window.jQuery = window.$ = jQuery
```

#### 선택자 (selector)

CSS 선택자 대부분을 지원

$(*) ⇒ 전체 선택자, all seoector
$(".class") ⇒ 클래스 선택자
$("#id") ⇒ 아이디 선택자
$("element") ⇒ 요소(태그, element) 선택자
$("selector1, selector2, … , selectorN") ⇒ 다중선택자(multiple selector)

![image-20200129154329584](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129154329584.png)

![image-20200129154335736](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129154335736.png)

Span은 밑에 써지는게 아니라 자리가 남으면 옆으로 써진다.

후손선택자 : $("body *")

![image-20200129162017795](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129162017795.png)

```
<html>
<head>
    <script src="/node_modules/jquery/dist/jquery.js"></script>
    <script>
        $(function() {
            //  후손 선택자
            //  body 태그 아래의 모든 태그
            $("body *").css('color', 'red');

            //  요소 선택자(element selector)
            //  H1 태그
            $("H1").css('background', 'yellow');

            //  ID 선택자 => 해당 문서에서 유일해야 함
            $("#title").css('border', '1px solid red');

            //  클래스 선택자 
            $(".right").css('textAlign', 'right');

            //  다중 선택자
            $("span, #title, .right").css('text-decoration', 'underline');
        });
    </script>
</head>
<body>
    <h1 class="right">제목1</h1>
    <p>내용1내용1내용1내용1내용1내용1내용1내용1내용1내용1내용1</p>
    <p>내용1내용1내용1내용1내용1내용1내용1내용1내용1내용1내용1</p>
```

![image-20200129162413658](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129162413658.png)



### p.423 자식 선택자, 후손 선택자

https://api.jquery.com/child-selector/

자식 선택자 ⇒ $("parent > child")

후손 선택자 ⇒ $("parent child")

![image-20200129162613530](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129162613530.png)

![image-20200129165024830](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129165024830.png)

![image-20200129165031822](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129165031822.png)

ul#menu 를 하면 하위의 모든 항목들이 상속되어 나타나게 된다. 

```
ul#menu li
```

꺽새없이 띄어쓰기하면 그 밑의 밑의 항목들까지(후손들까지) 상속을 받는다.

```
ul#menu > li
```

위에 있는 li들은 color, border 속성이 다 먹히는데, 꺽새의 자식들은 상속받지 않는다.



### p.425 속성 선택자

![image-20200129170219204](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129170219204.png)

![image-20200129170225794](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129170225794.png)