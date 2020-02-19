## Java_2

2020-02-18 (화)

### 연산자와 연산식

 2 + 3 = 5 에서, (2, 3은 operand | + 는 operator | 2+3=5 는 expression)

연산자(operator) : 연산에 사용되는 표시나 기호
피연산자(operand) : 연산자와 함께 연산되는 데이터
연산식(expression) : 연산자와 피연산자를 사용하여 연산 과정을 기술한 것

== : 메모리 상에 있는 값(내용)을 비교

리터럴 상수 : s1과 s2는 동일한 Java를 가르키고, new라는 객체 생성하면 같은 내용이라도 새롭게 생성된다.
s3와 s4가 새로 생김.

#### 연산자 종류

산출되는 값의 타입이 연산별로 다름

![image-20200218093914559](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218093914559.png)

#### 연산자의 우선순위

여러 연산식으로 구성된 연산은 다음 우선순위에 따라 수행

![image-20200218094059154](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218094059154.png)

* 단항 → 이항 → 삼항
* 산술 → 비교 → 논리 → 대입 순
  예) System.out.println( x > 0 && y < 0 );
* 우선순위가 같은 연산자는 왼쪽에서 오른쪽 방향으로 수행 (대입연산자는 예외/ 대입연산자는 오른쪽부터)
  예) System.out.println( 100 * 2 / 3 % 5);
  예) a =b =c =5;

괄호를 이용해서 연산자의 우선순위를 변경

![image-20200218094247406](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218094247406.png)

#### 단항, 이항, 삼항 연산자

피연산자의 수에 따라 구분

* 단항 연산자 : 부호, 증감 연산자
  예) ++x;
* 이항 연산자 : 산술, 비교, 논리 연산자
  예) x + y;
* 삼항 연산자 : 조건 연산자
  예) (sum > 90) ? "A" : "B";

#### 부호 연산자

boolean 타입과 char 타입을 제외한 기본 타입에 사용, 
**부호 연산자의 연산 결과는 int**

![image-20200218094456443](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218094456443.png)



![image-20200218094909389](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218094909389.png)

byte result3 = (byte)-b; 또는 int result3 = -b; 형식으로 처리해야 함 (후자를 권장)

#### 증감 연산자

boolean 타입 외 모든 기본 타입 피연산자에 사용
다른 연산자와 함께 사용될 경우 증감 연산자 위치에 따라 결과가 달라질 수 있음

![image-20200218095038153](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218095038153.png)

#### 논리 부정 연산자

boolean 타입에만 사용 가능

![image-20200218095316312](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218095316312.png)

#### 산술 연산자

![image-20200218101140292](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218101140292.png)

피연산자 타입이 동일하지 않을 경우 다음 규칙에 따라 일치시킨 후 연산을 수행

<ul>
    <li>피연산자가 byte, short, char 타입일 경우 모두 int 타입으로 변환</li>
    <li>피연산자가 모두 정수 타입이고 long 타입이 포함된 경우 모두 long 타입으로 변환</li>
    <li>피연산자 중 실수 타입이 있을 경우 허용 범위 큰 실수 타입으로 변환</li>
</ul>

#### 문자열 결합 연산자

+++ 연산자의 피연산자 중 한 쪽이 문자열인 경우
+가 있고 좌, 우에 operand 가 있을 떄 결합연산자

#### 비교 연산자

피연산자의 크기를 비교하여 true/false를 산출
동등 비교 연산자는 모든 타입에 사용 가능
크기 비교 연산자는 boolean 외 모든 기본 타입에 사용 가능

![image-20200218101420361](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218101420361.png)

---

##### LAB

입력한 글자의 알파벳 여부를 확인하시오.

![image-20200218102543053](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218102543053.png)

#### 논리 연산자

Boolean 타입만 사용 가능

![image-20200218102604151](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218102604151.png)

#### 대입 연산자

왼쪽엔 무조건 변수가 온다.
오른쪽 피연자의 값을 왼ㅉ꼬 피연산자인 변수에 저장

![image-20200218102733790](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218102733790.png)

연산의 결과는 오른쪽에 있는 값에 대해서 증가, 감소, 나누기 등을 처리한 결과가 된다. (복합대입연산자)

#### 삼항 연산자

3개의 피연자를 필요로 하는 연산자
? 앞의 조건식에 따라 콜론 앞뒤의 피연산자 선택

![image-20200218102814706](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218102814706.png)

![image-20200218102844592](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218102844592.png)

##### LAB 2

사용자가 입력한 숫자가 홀수인지 짝수인지를 판단하시오.

- java.util.Scanner 클래스 이용

![image-20200218103540042](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218103540042.png)

### 조건문

#### if문

![image-20200218103713314](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218103713314.png)

#### if-else 문

![image-20200218103727631](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218103727631.png)

#### if-else if-else 문

다중조건문
첫번째 조건을 만족하지 않으나 두번째 조건을 만족하면 if-else 블록
모든 조건을 만족하지 않으면 마지막 else문을 수행하는 것이다.

![image-20200218103744547](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218103744547.png)

#### switch 문

변수를 만족하는 case를 찾아가는 것이다.

![image-20200218103800166](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218103800166.png)

##### LAB 3

사용자가 입력한 알파벳이 모음인지 자음인지를 판단하시오.

* System.in.read() 매소드를 이용
* a, e, i, o, u    ⇒    모음

![image-20200218104657446](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218104657446.png)



### 반복문

#### for 문

조건이 만족하지 않을 때 까지 반복 수행한다.

![image-20200218104727980](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218104727980.png)

#### while문

조건이 만족할 때 까지 반복 수행한다.
조건이 맞아야 실행 가능한 것이다.

![image-20200218104801916](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218104801916.png)

#### do-while문

무조건 한 번은 실행한다. 조건일 끝날 때 체크하기 때문에 무조건 한 번은 실행해야한다.

![image-20200218104853031](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218104853031.png)

#### break 문

* for, while, do-whild, switch 문의 실행을 중지할 때 사용

  중지한다 : 밖으로 나온다. 반복절을 벗어나옴을 의미.

![image-20200218104936455](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218104936455.png)

* 반복문이 중첩되어 있는 경우, Label을 이용해서 바깥 반복문을 빠져나갈 수 있음.

  ![image-20200218105026528](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218105026528.png)

  ![image-20200218105659882](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218105659882.png)

X : Label의 이름을 붙여준 것이다.

#### continue 문

* form, while, do-while 문에서만 사용
* for 문의 증감식, while, do-while 문의 조건식으로 이동

![image-20200218111619495](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218111619495.png)



### 참조 타입(reference type)

![image-20200218111634566](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218111634566.png)

#### 기본 타입 변수와 참조 타입 변수의 차이

// 기본 타입 변수
int age = 25;
double price = 100.5;

// 참조 타입 변수
String name = "신용권";
String hobby = "독서";

![image-20200218111805665](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218111805665.png)

#### 메모리 사용 영역(Runtime Data Area)

![image-20200218111936225](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218111936225.png)

메소드 영역(method area) - 클래스별 정적 필드(static filed), 상수(constant), 생성자(constructor), 매서드(method) 코드 등을 분류해서 저장
힙 영역(heap area) - 객체와 배열이 생성되는 영역
JVM 스택 영역(stack area) - 메소드가 호출되면 프레임이 추가되고, 메소드가 종료되면 프레임이 제거

![image-20200218112325241](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218112325241.png)



참조 타입 변수는 스택 영역에 힙 영역에 생성된 객체의 주소를 가짐

![image-20200218112631248](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218112631248.png)



#### 참조 타입 변수 간 ==, != 연산

동일 객체(= 같은 주소) 참조 여부를 판단할 때 사용

```
public static void main(String[] args) throws IOException {
		String s1 = "Java String";
		String s2 = "Java String";
		String s3 = new String("Java String");
		String s4 = new String("Java String");
		
		System.out.println( s1 == s2 );
		System.out.println( s1 == s3 );
		System.out.println( s1 == s4 );
		System.out.println( s3 == s4 );
		
		String s5 = null;
		String s6 = null;
		System.out.println( s5 == s6 );	// true
	}
```

#### null 

참조 타입 변수는 객체를 참조하지 않는다는 뜻으로 null 값을 가질 수 있음
null로 초기화된 참조 변수도 스택 영역에 생성

![image-20200218113408598](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218113408598.png)

#### NullPointerException

참조 타입 변수가 null 상태에서 존재하지 않는 객체의 데이터나 메소드를 사용하는 경우 발생

![image-20200218114131893](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218114131893.png)

#### String 타입 변수에 문자열 리터럴을 대입하는 경우

문자열 리터럴을 힙 영역에 String 객체로 생성하고, 변수가 String 객체를 참조 

String name = "신용권";			(쌍따옴표: 문자열 형태의 리터럴, 프로그래머가 지정해주는값)
String hobby = "자바";

![image-20200218114323100](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218114323100.png)

문자열 리터럴이 같은 경우에는 같은 String 객체를 공유

String name1 = "신용권";
String name2 = "신용권";

![image-20200218114445879](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218114445879.png)

#### new 연산자를 이용한 String 객체 생성

힙 영역에 새로운 String 객체를 생성

String name1 = new String("신용권");
String name2 = new String("신용권");

![image-20200218114637779](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218114637779.png)

#### 문자열 리터럴과 new 연산자로 생성된 객체를 비교

​          ==   ⇒  주소를 비교
equals()   ⇒  값(문자열)을 비교

String 변수에 null 대입 → String 변수가 참조하는 객체가 없음 ⇒ 참조를 읽은 String 객체는 Garbage Collector를 통해 메모리에서 자동으로 제거

String hobby = "여행";
hobby = null;

![image-20200218114906785](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218114906785.png)



#### 배열(array)

같은 데이터 타입만 
한 번 생성된 배열은 길이를 늘이거나 줄일 수 없다.

**배열 생성 방법 1. 값 목록으로 배열 생성**

배열 변수 선언 
int[] intArray;	(이 방식을 더 많이 사용함)
int intArray[];

배열 생성 방법

값 목록으로 배열 생성
    타입[] 변수 = { 값0, 값1, 값2, ...}

배열 변수 선언 후 다른 실행문으로 값 목록으로 배열 생성하는 것은 불가
타입[] 변수;
변수 = { 값0, 값1, 값2, ...};		// ⇐ 컴파일 오류가 발생

배열 변수 선언 후 값 목록이 나중에 결정되는 경우 → new 연산자를 이용
타입[] 변수;
변수 = new 타입[] { 값0, 값1, 값2, ...};

![image-20200218132057180](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218132057180.png)

**배열 생성 방법 2. new  연산자를 이용한 배열 생성 → 타입별 기본값으로 배열 요소가 초기화**

타입[] 변수 = new 타입[배열크기];

![image-20200218132255009](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218132255009.png)

![image-20200218132448998](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218132448998.png)

![image-20200218132640897](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218132640897.png)



#### main() 메소드의 String[] args 매개변수

운영체제에서 내가 만든 app의 진입경로

![image-20200218133207849](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218133207849.png)

![image-20200218133235402](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218133235402.png)

![image-20200218133340453](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218133340453.png)

C:\workspaces\HelloJava\bin > java HelloJava aaa bbb ccc ddd eee

![image-20200218133455682](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218133455682.png)

Gugudan.java 파일을 생성
파라미터로 전달한 단을 출력(여러 단을 입력하면 낮은 단에서 높은 단으로 순차적으로 출력)
예) java Gugudan 5 7 9 4 ⇒ 4단, 5단, 7단, 9단 출력

![image-20200218140213043](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218140213043.png)

##### Java SortName

인원수는 ? 5
이름은? 홍길동
문숙경
김소정
탁성건
박상우
정렬결과 >> 김소정, 문숙경, 박상우, 탁성건, 홍길동

![image-20200218145057927](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218145057927.png)



프로그램 실행 시 전달된 문장에 포함된 단어를 역순으로 출력하시오.
예) java reverseWord "Welcome to Java World"
==>>> emocleW ot avaJ dlroW
[ 참고  ] String.split() 메소드, String.charAt() 메소드

![image-20200218153415051](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218153415051.png)



### 2차원 배열

#### 행렬 구조

int [] [] scores = new int[2] [3];

![image-20200218153608957](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218153608957.png)

scores.length				 ⇒	2 // A
scores[0].length			⇒	3 // B
scores[1].length			⇒	3 // C



#### 계단식 구조

![image-20200218154202888](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218154202888.png)

int[] [] scores = new int[2] [];
scores[0] = new int[2];
scores[1] = new int[3];
scores.length		 	⇒ 2 // A
scores[0].length		⇒ 2 // B
scores[1].length		⇒ 3 // C



#### 값 목록을 이용한 2차원 배열 생성

타입[] [] 변수 = { { 값1, 값2, ...}, { 값1, 값2, ...},  ... };

![image-20200218155008475](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218155008475.png)



#### 참조 타입 배열

![image-20200218155739514](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218155739514.png)



#### 배열 복사

for 문을 이용해서 요소 하나 하나를 복사
System.arraycopy()를 이용

![image-20200218160255933](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218160255933.png)

---

![image-20200218160502519](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218160502519.png)

---

![image-20200218162018436](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218162018436.png)

System.arraycopy 메소드를 이용해서 배열을 복사할 때
원본 배열과 타겟 배열의 크기가 다르면 어떻게 될까?
원본 > 타겟 => java.lang.ArrayIndexOutOfBoundsException
원본 < 타겟 => ㄴ마는 부분은 초기값으로 채워짐



#### 향상된 for 문

배열이나 컬렉션 등을 쉽게 다룰 수 있는 방법
반복 실행을 위한 루프 카운터 변수나 증감식을 필요로 하지 않을 때 사용

![image-20200218170738906](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218170738906.png)

#### 열거형

열거 상수 (한정된 값) 를 저장하는 타입

**열거형 선언**
public enum 열거형 이름{....}
예) public enum Week { MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY,  SATURDAY, SUNDAY }

![image-20200218170844714](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200218170844714.png)

**열거형 변수 선언**
열거형 변수 이름;
예) Week today;
	  Week reservationDay;

**열거 상수 저장**
열거형 변수 = 열거타입. 열거상수;
예)
Week today = Week.SUNDAY;
today = Week.SUNDAY;

로봇의 기능을 숫자로 정의/제어

