## Java

What is Java?

https://www.youtube.com/watch?time_continue=6&v=2Xa3Y4xz8_s&feature=emb_logo

![image-20200217095050232](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217095050232.png)

![image-20200217095134163](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217095134163.png)



* 플랫폼 별로 컴파일러를 다르게 가져가야 함(다르게 운영)



![image-20200217095416891](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217095416891.png)

* Java VM이 설치되면 플랫폼에 관계 없이 동일한 코드가 실행될 수 있음

![image-20200217095728673](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217095728673.png)

![image-20200217101142408](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217101142408.png)

* Java virtual machine이 깔려있으면 어느 플랫폼이든 상관 없이 실행 가능하다.
  * Java VM만 있으면 내가 만든 프로그램이 어디서든 돌아가는 구조를 가진다.



* JVM 구조(아키텍처)

![image-20200217102103922](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217102103922.png)



//소스 코드를 만들어서 실행하는 절차

작성(편집) ---> 컴파일 ---> 링크 ---> 로더 ---> 실행

![image-20200217102225812](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217102225812.png)

![image-20200217102235948](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217102235948.png)

![image-20200217102241691](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217102241691.png)

### JAVA_HOME 및 PATH 환경 변수 등록

시작메뉴 ---> 환경 변수 

![image-20200217103158371](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217103158371.png)



![image-20200217103328044](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217103328044.png)

***명령 프롬프트를 <u>새로 실행 후</u> 확인***

* set JAVA_HOME
* set PATH

![image-20200217103603931](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217103603931.png)



### C:\workspaces\HelloJava.java 파일을 생성

```
class HelloJava {
    public static void main (String args[]) {
        System.out.println("Hello Java!!!");
    }
}
```

![image-20200217104623143](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217104623143.png)

![image-20200217104705775](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217104705775.png)



![image-20200217105142139](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217105142139.png)

![image-20200217105021067](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217105021067.png)

![image-20200217105242669](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217105242669.png)



// HelloJava.java 우클릭

build path -> configure build path

* Java는 이름을 맞춰줘야 한다. 이름이 다르면 오류가 발생함.

Public class = 접근(실행)할 수 있게 한다. 접근 허용 범위.
Private class =  접근(실행)을 제한한다.

Public static = 하나의 인스턴스를 실행시킨다. (static = 인스턴스 하나만 생성)

string : 데이터타입

args : 변수 이름

![image-20200217112140937](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217112140937.png)

![image-20200217113014980](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217113014980.png)



* main 함수
  운영체제가 내 프로그램을 실행하는데 내 함수들이 굉장히 많다, 이중 무엇을 호출해야 할 지 모를 때 Hello Java의 실행을 약속한 것이 main부터 시작한다. (진입하는 진입점이 된다.)
* 해당하는 HelloJava를 하나 만들어야 하는데, 

* Private data에 대해 접근할 수 있는 public method를 제공한다.







### 변수(Variable)

- 값을 저장할 수 있는 메모리의 특정 주소에 붙여진 이름
- 변수 선언 

```
int 	age;		⇐ 정수(int)값을 저장할 수 있는 age 변수를 선언
double	value;
===== 	=====
타입		이름
```

* 동일 타입의 변수는 콤마로 구분해서 동시에 정의
  * int x;	int y;	int z;
    => int x, y, z;
* 변수 이름 규칙
  * 첫 번째 글자는 문자, "$", "_" 이어야 하고, 숫자로 시작할 수 없다
    (문자이어야 함. ex/ price, $price, _companyName)
    (1v(숫자), @speed(특수기호), $#value(샵)⇐ 불가능
  * 영어 대소문자를 구분한다
  * firstName과 firstname은 다른 변수이다.
* 첫 번째 글자는 소문자로 시작하고, 다른 단어가 붙을 경우 첫글자를 대문자로 한다. (관례)
  * maxSpeed, firstName, carBodyColor, ...
* 변수 이름의 길이는 제한이 없다.
* 자바 예약어는 변수 이름으로 사용할 수 없다. ( 자바랑 비슷함 )



#### 자바 예약어

자바 언어에서 의미를 가지고 사용되는 단어

* 기본 타입 ⇒ boolean, byte, char, short, int, long,float, double
* 접근 제한자 ⇒ private, public, protected
* 클래스와 관련된 것 ⇒ class, abstract, interface, extends, implements, enum객체와 관련된 것 ⇒ new, instanceof, this, super, null메소드와 관련된 것 ⇒ void, return제어문과 관련된 것 ⇒ if, else, switch, case, default, for, do, while, break, continue논리값 ⇒ true, false예외 처리와 관련된 것 ⇒ try, catch, finally, throw, throws기타 ⇒ package, import, synchronized, final, static 

![image-20200217151757242](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217151757242.png)

![image-20200217151807009](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217151807009.png)

변수 값 복사 = 변수의 값을 다른 변수에 저장

```
int x = 10;
int y = x;
x = 20;
System.out.println("x = " + x + " , y = " + y);		// x = 20,   y = 10
```

![image-20200217151924684](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217151924684.png)



#### 로컬 변수

메소드 블록 내에서 선언된 변수

→ 메소드 블록 내에서만 사용이 가능
→ 메소드 실행이 끝나면 자도으로 삭제

![image-20200217152056163](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152056163.png)



#### Java Data Type

![image-20200217152111439](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152111439.png)

![image-20200217152123942](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152123942.png)

![image-20200217152131285](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152131285.png)



#### 정수 리터럴

![image-20200217152147101](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152147101.png)



#### Char 타입 - 하나의 문자를 저장

작은 따옴표로 감싼 문자 리터럴

```
char var1 = 'A';		⇒ 유니코드 65
char var2 = '';
char var3 = '홍';
cahr var4 = 65;			⇒ 'A'
char var5 = 0x0041		⇒ 'A'
```



#### 문자열(String)

큰따옴표로 감싼 문자들

```
char var1 = "A"		⇒ X
String var2 = 'A';	⇒ X
String var3 = "A";	⇒ O
```



#### 이스케이프 문자(escape)

문자열 내부에서는 \는 이스케이프 문자를 뜻 함

![image-20200217152533475](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152533475.png)

![image-20200217152541789](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152541789.png)



#### 자동 타입 변환(Promotion)

값의 허용 범위가 작은 타입이 큰 타입으로 저장될 때 ⇒ 큰 타입 = 작은 타입;

byte < short < int < long < float < double

byte byteValue = 10;
int intValue = byteValue;

char 타입을 int 타입으로 자동 타입변환하면 유니코드 값이 int 타입에 저장

![image-20200217152716458](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217152716458.png)

#### 강제 타입 변환(castring)

큰 허용 범위 타입을 작은 허용 범위 타입으로 강제로 나누어 한 조각만 저장

작은허용범위타입 = (작은허용범위타입) 큰허용범위타입;

```
public static void main(String[] args) {
		int intValue = 256;
		byte byteValue = (byte)intValue;

		System.out.println(intValue);		// 10
		System.out.println(byteValue);	// 10
```

// 실수 타입을 정수 타입으로 캐스팅하면 소수점 이하를 버림

```
double doubleValue = 3.14;
		int intValue2 = (int)doubleValue;
		System.out.println(doubleValue);	// 3.14
		System.out.println(intValue2);	// 3
	}
```



// 자동 타입 변환이 발생하는 경우(예)

![image-20200217154908738](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217154908738.png)

피 연산자 중 하나가 long 타입이면 다른 피연자는 long 타입으로 자동 변환
피 연산자 중 하나가 double 타입이면 다른 피연자는 double 타입으로 자동 변환

![image-20200217155612180](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217155612180.png)



#### + 연산자

- 문자열 결합 ⇐ 피연산자 중 하나라도 문자열인 경우 (나머지 피연산자는 모두 문자열로 자동 변환)
- 덧셈 연산 ⇐ 피연산자가 모두 숫자

![image-20200217155724857](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217155724857.png)



#### 문자열을 다른 기본 타입으로 강제 타입 변환

String stringvalue = "";



stringValue="10";

byte byteValue = Byte.parseByte(stringValue);										//

stringValue = "200";

short shortValue = Short.praseShort(stringValue);								//

stringValue = "300000";

int intValue = Integer.parseInt(stringValue);											//

stringValue = "400000000";

long longValue = Long.parseLong(stringValue);										//

stringValue = "12.345";

float floatValue - Float.parseFloat(stringValue);										//

stringValue = "12.345";

double doubleValue = Double.parseDouble(stringValue);						//

stringValue = "true";		//		or "false"

boolean booleanValue = Boolean.parseBoolean(stringValue);				//

```
System.out.println(byteValue);		// 10
		System.out.println(shortValue);		// 200	
		System.out.println(intValue);		// 300000
		System.out.println(longValue);		// 400000000
		System.out.println(floatValue);		// 12.345
		System.out.println(doubleValue);	// 12.345
		System.out.println(booleanValue);	// true
	}
}
```



#### 기본 타입을 문자열로 변환

String stringValue = String.valueOf(data);



#### 시스템 입출력

System.out.println("Hello Java!!!")

⇒ https://docs.oracle.com/javase/8/docs/api/java/lang/System.html

println(내용)	⇒ 내용을 출력하고 행을 변경
print(내용)       ⇒ 내용만 출력
printf("형식문자열", 값1, 값2, ...)	⇒ 첫번째 문자열 형식대로 내용을 출력

![image-20200217163752491](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217163752491.png)

![image-20200217163555119](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217163555119.png)



![image-20200217164145601](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217164145601.png)



%d		⇒ 정수														⇒ 123
%6d	  ⇒ 6자리 정수, 왼쪽 빈 자리 공백			 ⇒ ___123
%-6d	 ⇒ 6자리 정수, 오른쪽 빈 자리 공백		 ⇒ 123 ＿＿＿
%06d    ⇒ 6자리 정수, 왼쪽 빈 자리 0 채움		  ⇒ 000123

예

```
public static void main(String[] args) {
		System.out.printf("이름: %s, 나이: %3d\n", "홍길동", 3);
		System.out.printf("이름: %1$s, 나이: %2$3d\n", "이순신", 323);
	}
```

%10.2f		⇒  소수점 이상 7자리, 소수점 이하 2자리, 왼쪽 빈자리 공백 		⇒ ___123.45
%-10.2f	   ⇒ 소수점 이상 7자리, 소수점 이하 2자리, 오른쪽 빈자리 공백 	 ⇒ 123.45 ＿＿＿
%010.2f	  ⇒ 소수점 이상 7자리, 소수점 이하 2자리, 왼쪽 빈자리 0 채움	   ⇒ 0000123.45

![image-20200217165132500](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217165132500.png)



\t		 ⇒ 탭
\n		⇒ 줄바꿈
%%	 ⇒ %

![image-20200217170116956](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217170116956.png)

![image-20200217165730103](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217165730103.png)



#### System.in.read()

키보드로 입력한 키코드를 읽어서 반환하는 메소드

![image-20200217170440313](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217170440313.png)

한계(단점)

- 2개 이상 키가 조합된 한글은 읽을 수 없음
- 키보드로 입력된 내용을 통문자열로 읽을 수 없음



#### Scanner 클래스

통문자열을 읽어 사용 가능

![image-20200217172415930](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200217172415930.png)