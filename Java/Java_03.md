## Java_03

### 객체(object)

식별할 수 있는 대상,
객체  =  속성(field)  +  동작(method)
![image-20200219092930056](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219092930056.png)



#### 객체와 객체간의 상호작용

메소드 호출을 통해 객체가 다른 객체의 기능을 이용

![image-20200219093250295](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219093250295.png)



#### 객체 간의 관계

집합관계  :  부품과 완성품의 관계
사용관계  :  객체간의 상호작용
상속관계  :  상위 객체를 기반으로 하위 객체를 생성

![image-20200219093513936](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219093513936.png)



### 클래스(class)

인스턴스(instance)  :  클래스로부터 만들어진 객체

![image-20200219093902973](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219093902973.png)

**클래스 선언**
클래스 이름.java 소스 파일로 작성
접근제한자 class 클래스 이름 [extends 부모클래스명] { ... }

**클래스부터 객체를 생성**
클래스명 변수명;
변수명  =  new 클래스명();
			or
클래스명 변수명  =  new 클래스명();

⇒ new 연산자로 힙 메모리 영역에 객체를 생성
⇒ 객체 생성 후 객체의 주소를 반환
⇒ 클래스 변수에 저장하여 객체를 사용
![image-20200219094347776](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219094347776.png)



#### 클래스 용도

**라이브러리(API: Application Programming Interface) 클래스**
객체 생성 및 메소드 제공하는 역할

**실행 클래스**
main() 메소드를 제공하는 역할

![image-20200219095715028](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219095715028.png)

![image-20200219095731537](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219095731537.png)



#### 클래스 멤버

![image-20200219095749912](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219095749912.png)



#### 필드

![image-20200219101239669](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219101239669.png)

필드 선언

 - 클래스 중괄호 블록 어디에 존재해도 무관

 - 생성자나 메소드 블록 안에는 정의할 수 없다.

 - 필드를 선언할 때 초기값을 설정할 수도 있고, 생략 또한 가능 (생략하면 객체가 생성될 때 기본 초기값으로 자동 설정됨)

   ![image-20200219103100660](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219103100660.png)



**필드 사용**

- 클래스 내부에서 사용하는 경우 (생성자 또는 메소드에서 사용) ⇒ 필드 이름으로 접근
- 클래스 외부에서 사용하는 경우 ⇒ 클래스로부터 객체를 생성한 후 필드를 사용

![image-20200219103821229](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219103821229.png)

![image-20200219104358814](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219104358814.png)



#### 생성자(constructor)

클래스로부터 new 연산자로 객체를 생성할 때 호출되는 <u>**객체 초기화**</u>를 담당하는 메소드

객체 초기화 - 필드를 초기화하거나 메소드를 호출해서 객체를 사용할 준비를 하는 것
생성자가 성공적으로 동작하면 힙 영역에 객체를 생성하고 객체의 주소를 반환

![image-20200219104519783](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219104519783.png)



#### 기본 생성자(default constructor)

클래스에 생성자를 선언하지 않으면 바이트 코드에 자동으로 착되는 생성자
클래스에 생성자를 선언하지 않아도 new 연산자를 이용해서 객체를 생성할 수 있다.

![image-20200219105043279](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219105043279.png)

#### 생성자 선언

클래스명(매개변수, ...) { ... /* 객체 초기화 코드 */... }

매개변수는 생략할 수도 있고, 여러 개 사용할 수도 있다.
클래스에 생성자가 명시적으로 선언된 경우, 반드시 선언된 생성자를 호출해서 객체를 생성해야 한다.



#### 생성자 오버로딩(overloading)

매개변수의 타입, 개수, 순서가 다른 생성자를 여러 개 선언
⇒ 다양한 형식으로 객체를 쉽게 생성할 수 있도록 하기 위해



#### this()

생성자에서 다른 생성자를 호출 → 생성자 오버로딩 코드 작성 시 발생하는 중복을 해결
생성자에 첫번째 줄에서만 사용 가능



#### 메소드 선언부(signature)

리턴 타입, 메소드 이름, 매개변수 선언, 메소드 실행 블록

![image-20200219114957884](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219114957884.png)

**리턴 타입**

메소드 실행 결과 반환되는 데이터 타입
반환 값이 없을 수 있고,
반환 값이 있을 수 있다. → 선언부에 데이터 타입을 명시

void powerOn() { ... }
double divied() { ... }

![image-20200219131052537](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219131052537.png)

**메소드 이름**

- 숫자로 시작할 수 없고, _ 또는 $ 기호를 제외한 특수문자를 사용할 수 없다.
- (관례적으로) 소문자로 시작
- 서로 다른 단어가 혼합될 경우, 뒤에 오는 단어의 첫 글자를 대문자로 작성

![image-20200219132049176](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219132049176.png)



#### 매개변수 선언

매개변수의 타입이 일치하지 않으면 컴파일 오류가 발생



**매개변수의 개수를 모를 경우**
	1) 배열 타입으로 선언
	int sum(int[] values) { ... }

​	int[] params = { 1, 2, 3 };
​	int result = sum(params);
​				or
​	int result = sum(new int[] { 1, 2, 3 });

​	2) 배열을 생성하지 않고 값 목록만 넘겨주는 방식
​	int sum(int ... values) { ... }

​	int result = sum(1, 2, 3);
​			or
​	int result = sum(1, 2, 3, 4, 5);
​			or
​	int[] params = { 1, 2, 3 };
​	int result = sum(params);
​			or
​	int result = sum(new int[] { 1, 2, 3 });

![image-20200219133835131](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219133835131.png)



**리턴값이 있는 메소드**

- 메소드 선언에 리턴 타입이 있는 경우 → return 구문을 이용해서 리턴값을 지정

- return 구문을 통해서 반환하는 리턴값의 타입은 리턴 타입이거나 변환될 수 있는 타입이어야 함

  int plus(int x, int y) {
  	int result = x + y;
  	return result;
  }

  int plus (int x, int y) {
  	byte result = (byte)(x + y);
  	return result;
  }



**리턴값이 없는 메소드**
void로 선언된 메소드에서는 return 구문을 사용해서 메소드 실행을 종료

// Car.java

![image-20200219135846034](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219135846034.png)

// CarExample.java

![image-20200219135902367](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219135902367.png)

// console

![image-20200219135915140](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219135915140.png)

![image-20200219140035713](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219140035713.png)



#### 메소드 오버로딩(overloading)

- 같은 이름의 메소드를 여러 개 선언

- 매개변수의 타입, 개수, 순서가 다른 것

- 오버로딩 된 메소드가 호출되면 JVM은 매개변수 타입을 보고 메소드를 선택

  int plus(int x, int y) { ... }
  double plus(double x, double y) { ... }

  plus(10, 20);				⇒ int plus(int x, int y) { ... }
  plus (10.5, 20.3);		 ⇒ double plus(double x, double y) { ... }
  plus(10, 20.3);			 ⇒ double plus(double x, double y) { ... }

![image-20200219143737254](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219143737254.png)



#### 인스턴스 멤버 vs 정적 멤버

멤버 = 필드 + 메소드

인스턴스 멤버 = 객체마다 가지고 있는 멤버

- 인스턴스 필드 : 힙 영역에 객체마다 가지고 있는 멤버, 객체마다 다른 데이터를 저장
- 인스턴스 메서드 : 객체가 있어야 호출 가능한 메소드, 클래스 코드(메소드 영역)에 위치

정적 멤버 = 객체와 상관 없는 멤버, 클래스 코드(메소드 영역)에 위치

- 정적 필드 : 객체 없이 클래스만으로 사용 가능한 코드
- 정적 메서드 : 객체 없이 클래스만으로 사용 가능한 메서드

```
public class Car {
		int gas;
		void setSpeed(int speed) { ... }
}

Car myCar = new Car();
myCar.gas = 10;
myCar.setSpeed(60);
Car yourCar = new Car();
yourCar.gas = 20;
yourCar.setSpeed(80);
```

![image-20200219150128229](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219150128229.png)

#### this

객체 내에서 인스턴스 멤버에 접근하기 위해 사용
생성자와 메소드의 매개변수 이름이 필드 이름과 동일한 경우, 필드임을 지정하기 위해 사용



// Calculator.java

![image-20200219153231517](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219153231517.png)

// CalculatorExe

![image-20200219153314654](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219153314654.png)

// result

![image-20200219153325811](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219153325811.png)

// 정적 메소드 선언시 주의사항

![image-20200219153946257](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219153946257.png)



#### 싱글톤(singleton)

전체 프로그램에서 단 하나의 객체만 만들어지도록 보장하는 코딩 기법

```
public class 클래스명 {
	private 클래스명() { ... }
	
	// private를 걸어주지 않으면 바꿔치기 할 수 있다.
	private static 클래스명 singleton = new 클래스명();
	
	static 클래스명 getInstance() {
			return singleton;
	}
}
```

// 클래스명 변수1 = 클래스명.getInstance();

// 클래스명 변수2 = 클래스명getInstance();
![image-20200219155636451](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219155636451.png)

// Singleton

![image-20200219160938469](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219160938469.png)

// SingletonExe

![image-20200219161020362](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219161020362.png)

// result

![image-20200219161043050](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219161043050.png)



#### final 필드

초기값이 저장되면 최종값이 되어 프로그램 실행 중 변경이 불가능

**final 필드 초기화**
단순값인 경우, 필드 선언할 떄 초기화 ⇒ 주로 정적 필드(상수)인 경우
객체 생성 시 외부 데이터로 초기화가 필요한 경우, 생성자에서 초기화 ⇒ 주로 인스턴스 필드인 경우

// Person

![image-20200219164746480](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219164746480.png)



#### Static final 필드

상수

관례적으로 모두 대문자를 사용

// Earth

![image-20200219165247823](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219165247823.png)



#### 패키지(package)

물리적으로는 파일 시스템의 디렉터리
클래스 이름의 일부 ⇒ 클래스를 유일하게 만들어주는 식별자 역할
⇒ 클래스 이름이 동일하더라도 패키지 이름이 다르면 다른 클래스로 인식

![image-20200219170713935](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219170713935.png)

A 클래스 ⇒ com.mycompany.A
B 클래스 ⇒ com.yourcompany.B

패키지 명명 규칙

* 숫자로 시작 불가
* _ 또는 $ 기호를 제외한 특수문자 사용이 불가
* java로 시작하는 패키지는 자바 표준 API에서만 사용 가능
* (관레상) 모두 소문자로 작성



#### import문

* 사용하고자 하는 클래스 또는 인터페이스가 다른 패키지에 소속된 경우, 해당 패키지 클래스 또는 인터페이스를 가져와 사용하는 것을 컴파일러에 통지

  import 상위패키지.하위패키지.클래스이름;
  import 상위패키지.하위패키지.*;

* 하위 패키지는 별도로 import 해야한다.
  import com.mypage.*;
  import com.mypage.subpackage.*;
  com.mypage.subpackage.MyClass;

* 다른 패키지에 동일한 이름의 클래스가 존재하는 경우 ⇒ import 구문과 관계 없이 (패키지 명을 포함한) 클래스 전체 이름을 기술

* ![image-20200219171952591](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200219171952591.png)