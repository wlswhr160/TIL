1. 내가 만들고싶은 서비스가 무엇인지

2. 어떤 부가 서비스를 추가하고 싶은지, 유사 사례 연구 (Usecase)
   -> 장,단점 보완.
3. 우리는 이런걸 만들고 싶었고, 유사 사례는 이런 것들이 있었습니다. 이러한 장,단점을 보완했다.
4. Architecturing 





# JavaScript 2 (2)

https://www.w3schools.com/html/html_basic.asp

* 헤더

```
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
```

* 문단(단락을 나누는 p tag)

```
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

* 태그 (=요소)

```
<a href="http:///www.w3scholls.com">This is a link</a>
이 경우에 <a : 태그명 | herf="http:...com" : 속성 | This is a link : 값
```

* 이미지 태그

```
<img src="w3scholls.jpg" alt="W3Scholls.com" width="104" height="142">
이미지 태그는 닫는 태그가 없다. 
<img 		/>		: 이렇게 슬래시를 달아줘도 된다.
<p>___</p>			: 태그 값이 있다
<p/>				: 태그 값이 없다
```

* 버튼  <button>click me</button>

```
<button>click me</button>
```

* 리스트

```
<ul> : 동그라미 기호 
	<li>Coffee</li>
	<li>Tea</li>
<ul>
```

```
<ol> : 순서 1,2,3,4
	<li>Coffee</li>
	<li>Tea</li>
</ol>
```

<ul>
    <li>Coffee</li>
    <li>Tea</li>
</ul>

<ol>
    <li>Coffee</li>
    <li>Tea</li>
</ol>

* 테이블

```
<tr>
	<th>Firstname</th>
	<th>Lastname</th>
	<th>Age</th>
<tr>
```

* border : 테두리

![image-20200123101902347](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123101902347.png)

* colspan : 셀이 가로로 병합 (col:column의 약자, 기둥)

![image-20200123102033587](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123102033587.png)

* rowspan : 셀이 세로로 병합 (row:옆으로 늘어서있는)

![image-20200123102342801](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123102342801.png)

* class : 분류하다

```
<div class="cities">
	<h2>London</h2>
	<p>London is the capital of England.</p>
</div>
```

<div class="cities">
    <h2>Paris</h2> 
    <p>
        Paris is the capital of France.
    </p>
</div>



![image-20200123103148831](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123103148831.png)

**#을붙이는 이유 : div가 3개가 있는데, 하나의 div만 first라는 id를 부여, 이 하나에 대해서만 기능을 하고 싶을 때, #first 라는 규칙을 쓴다(id를 찾으려면 #(idname))

![image-20200123103805982](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123103805982.png)

<!DOCTYPE html>
<html>
<head>
<style>
h2 {
	color: pink;
}
p {
	color: black;
}
</style>
</head>
<body>


<div class="cities">
<h2>London</h2>
<p>London is the capital of England.</p>
</div> 

<div class="cities">
<h2>Paris</h2>
<p>Paris is the capital of France.</p>
</div>

<div class="cities">
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>
</div>



* Form

![image-20200123104719433](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123104719433.png)



### 입력

#### 문자열을 입력하는 방법

* 숫자를 입력 받는 방법
  * 문자열을 입력받은 후 숫자로 변환
  * 문자열을 입력할 떄 사용하는 함수는 prompt() - 매개변수 두 개 필요
* 개발자 도구(F12)에서 prompt('숫자를 입력하세요.')
  * let inputNumber = prompt('숫자를 입력하세요');	← 사용자 입력을 받는 코드
  * console.log(inputNumber);	                                    ← 입력받은 값을 콘솔에 출력
  * alert(inputNumber);                                                    ← 입력받은 값을 사용자에게 알림  

![image-20200123105036922](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123105036922.png)

![image-20200123105209306](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123105209306.png)

* let yn = confirm('1 + 2 = 3 이 맞습니까?');
  * console.log(yn);					← 확인을 클릭하면 true, 취소를 클릭하면 false를 반환

![image-20200123105716315](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123105716315.png)

**에러가 뜨는 이유 : 브라우저의 VM18026:1 이라는 변수가 생성되어 있기 떄문에 에러가 뜨는 것이다.

![image-20200123111439836](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123111439836.png)

**이런식으로 재선언되었기 때문에 에러가 생김.



**숫자와 문자열 덧셈 연산은 문자열이 우선**

*문자열 + 숫자 ⇒ 문자열 + 문자열 ⇒ 문자열문자열*

![image-20200123112109470](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123112109470.png)

**숫자와 문자열 덧셈을 제외한 사칙 연산은 숫자가 우선**

문자열 * 숫자 ⇒ 숫자 * 숫자 ⇒ 값

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123112338911.png" alt="image-20200123112338911" style="zoom:200%;" />

**강제적으로 형변환 = 강제적으로 형변환 (반대: 암시적 형변환)**
다른 데이터 타입을 숫자형으로 변환 ⇒ Number() 함수를 사용
다른 데이터 타입을 문자열로 변환 ⇒ String() 함수를 사용

![image-20200123113018626](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123113018626.png)

**NaN = Not a Number

<ul> 
    <li>자료형은 숫자나 자바스크립트로 나타낼 수 없는 숫자를 의미</li>
    <li>예) 자바스크립트에서는 복소수 표현이 불가능</li>
</ul>

![image-20200123113311633](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123113311633.png)

---

### 불 자료형 변환

#### Boolean() 함수

다른 자료형을 불(bool) 자료형으로 변환 (bool:참,거짓 표현) → 명시적인 형변환

<ul>
    <li>0, NaN, '', null, undefined ⇒ false로 변환</li>
    <li>나머지 ⇒ true로 변환</li>
</ul>

![image-20200123113735955](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123113735955.png)

**0, NaN, '', null, undefined 데이터에 대한 암시적인 형변환** 
⇒ Boolean() 함수의 결과와 동일

###### p.65 일치 연산자

**자동 형변환 (= 암시적 형변환)의 문제점 → 혼돈을 야기

<script>
    console.log('' == false);
    console.log('' == 0);
    console.log(0 == false);
    console.log('273' == 273);
</script>

⇒ 모두 true를 반환

**이렇게하면 비논리적인 형식으로 혼란을 가져올 수 있음

![image-20200123114558524](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123114558524.png)

**일치연산자 : 양변의 자료형과 값의 일치 여부를 확인.

=== : 양변의 자료형과 값이 모두 일치함
!== : 양변의 자료형과 값이 일치하지 않음

<script>
    console.log('' === false);
    console.log('' === 0);
    console.log(0 === false);
    console.log('273' === 273);
</script>

⇒ 모두 false를 반환

#### 템플릿 문자열

백틱(`)을 사용.

${} : 위에서 정의한 값을 사용할 수 있다.



### 스코프

선언된 변수를 사용할 수 있는 유효 범위
일반적인 프로그래밍 언어에서는 "특정 스코프 안에서 선언한 변수는 해당 스코프 안에서만 사용할 수 있다" 라는
규칙이 있다.

![image-20200123131437649](images/image-20200123131437649.png)

* let이라는 키워드를 쓰면 오류가 발생한다.

![image-20200123131719501](images/image-20200123131719501.png)

* let이라는 키워드를 쓰면 명시적으로 나타낼 수 있다.

![image-20200123131904781](images/image-20200123131904781.png)

* var 키워드의 비동기 함수

![image-20200123132043835](images/image-20200123132043835.png)

#### 익명함수(Annonymous function)

function () 

동기 : 일이 끝나고 다음 일이 단계적으로 실행되는 것
ex) 엄마가 아들한테 숙제 다 했냐 얘기하고, 아들에게 숙제 끝나면 얘기 해 ->  콜백

비동기 : 일이 끝나지 않은 상태에서 다음 일을 하는 것
ex) 메인이 되는 컨텐츠를 먼저 가져와서 뿌리고, 하나씩 다른 컨텐츠를 꽂아주는 것. 호출 후 콜백
ex) setTimeout 

#####  var와 let의 차이

![image-20200123134243412](images/image-20200123134243412.png)

![image-20200123134258868](images/image-20200123134258868.png)

var : 재정의해도 문제가 되지 않는다.

![image-20200123134500969](images/image-20200123134500969.png)

![image-20200123134724306](images/image-20200123134724306.png)

![image-20200123134736890](images/image-20200123134736890.png)

* 정의되지않은 1번이 있기 때문에 오류가 난다.



### 연습문제

1. 개념 정리

표현식
키워드 : 해당하는 언어에서 예약하는 미리 정의되어있는 값들(=예약어)
식별자 : 변수명, 함수명, 속성명, 메소드명,(이름들) 이 이름들은 유니크하게 구분할 수 있어야 함
주석 : 설명
문자열 : 문자, 단어들의 나열
숫자 : 말 그대로 숫자
불 : true, false
변수 : 변하는 수, 변하는 값을 저장하는 메모리 공간

2. 변수를 사용할 때 사용하는 키워드 : var
3. 자료형을 검사할 때 사용하는 것과 그 분류 : typeof() - 연산자