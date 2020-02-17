## JavaScript 6,  객체

정형화 : 해당하는 성격을 지닌 객체(행)를 이용하여 데이터가 쌓여있는 배열(열) 형태로 표현을 한다.


### 객체

속성과 방식을 정하는 

객체 정의 : 중괄호로 묶어준다.
이름이 공백 문자를 포함하는 경우에는 따옴표로 묶어준다.

```
console.log(person.favorite colors);		→ 이것은 안 된다.
------------------------------------		
console.log(person['favorite colors']); 	→ 올바른 표기법
```

객체이름을 사용할 때는 온점을 사용하거나, 대괄호에 따옴표를 묶어줘야 한다.

![image-20200129102600859](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129102600859.png)

![image-20200129102509834](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129102509834.png)

* 인덱스 : 0, 요소 : 빨강, 파랑, 초록

![image-20200129103005058](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129103005058.png)

![image-20200129103016359](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129103016359.png)

#### p.174 속성과 메서드

![image-20200129103755336](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129103755336.png)

![image-20200129103802802](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129103802802.png)

객체는 배열처럼 for 구문을 사용하여



### p.176 객체와 반복문

![image-20200129104904292](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129104904292.png)

![image-20200129104913142](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129104913142.png)

this. 할 때 띄어쓰기에 대해 엑세스 하려면 어떻게 해야하는가?

→ this 다음에 마침표를 뺀 후 대괄호로 묶을 수 있다.

```
return this['favorite color']
```

![image-20200129111630286](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129111630286.png)



### p.177 객체 관련 키워드 : in, with

#### p.178 객체와 반복문 : in

![image-20200129112145419](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129112145419.png)

![image-20200129112153468](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129112153468.png)

* 이어서 과목별 점수를 출력해보자.

![image-20200129112617568](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129112617568.png)

![image-20200129112626309](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129112626309.png)

**과목별 점수가 출력되는 것을 볼 수 있다.**

#### p.179 with

![image-20200129113121686](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129113121686.png)

![image-20200129113128108](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129113128108.png)



#### p.182 속성 추가

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129113908839.png" alt="image-20200129113908839" />

![image-20200129113914289](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129113914289.png)

**toString() 메서드 : 객체에 있는 속성을 출력하는 메서드**



#### p.184 속성 제거, Delete

Delete는 함수가 아니고 연산자이다, 단항 연산자(typeof, -)

그러나 Delete를 함수처럼 쓸 수도 있다.

![image-20200129114124337](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129114124337.png)

![image-20200129114130866](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129114130866.png)

**Delete 키워드는 괄호를 사용해도 되고 사용하지 않아도 된다.**



### p.185 객체와 배열을 사용한 데이터 관리

![image-20200129132022358](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129132022358.png)

![image-20200129131758049](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129131758049.png)

### p.189 함수를 사용한 객체 생성

![image-20200129133154520](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129133154520.png)

![image-20200129133205404](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129133205404.png)

### p.192 조금 더 나아가기

기본 매개변수 : 함수를 정의할 때 함수 파라메터에 기본값을 주는 것.

옵션 객체 : 함수의 매개변수로 전달하는 객체
이것은 "입력해도 되고, 입력하지 않아도 된다." 따라서 기본 매개변수처럼 값을 입력하지 않으면
초기화해주는 과정이 필요

**함수의 매개변수로 넘어가는 객체를 옵션객체라 한다. 초기화 중요**

![image-20200129134136688](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129134136688.png)

옵션 객체 사용 예 : 

```
function makestudent(obj) {
	let result = {
		name : obj.name
		korean : obj.korean
		...
	},
	getSum : function() {
		return this.korean + this.math + this.english + this.science;
	},
	getAverage : function() {
		return this.getSum() / 4
	}
	return result;
}

//  test 함수는 obj 객체를 매개변수로 받아들인다.
        function test(obj) {
            obj.valueA = obj.valueA || 0;
            obj.valueB = obj.valueB || 0;
            obj.valueC = obj.valueC || 0;

            with(obj) {
                console.log(`${valueA} : ${valueB} : ${valueC}`);
            }
        }
        test({ valueA: 52, valueB: 273 });
```

```javascript
let abc = '123'
abc
123
```

```javascript
let xyz = [1, 2, 3]
```



##### reference type : 실제 각 주소를 저장하고 있는 타입

##### value type



### p.194 참조 복사와 값 복사

![image-20200129135139536](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129135139536.png)

![image-20200129135144891](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129135144891.png)

### p.200 배열 복제

![image-20200129135513315](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129135513315.png)

![image-20200129135522234](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129135522234.png)

*값이 복사되는 게 아니라 주소가 복사되는 것이다. reference를 넘긴다.* 
*old- 실제 객체 주소가 저장되어있다.*
*old=>new 는 객체가 복사되는 게 아니라 주소가 복사!  → 얕은 복사!*

![image-20200129140418074](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129140418074.png)

![image-20200129140432944](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129140432944.png)

#### 똑같은 객체 복사하기

oldObject가 가지고있는 동일한 객체를 newObject가 reference 하는 것이다.

![image-20200129142607774](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129142607774.png)

![image-20200129142621527](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129142621527.png)



### 깊은 복사

![image-20200129143817708](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129143817708.png)

![image-20200129143825452](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129143825452.png)

배열의 깊은복사를 위해선s for loop 돌려서 복사했는데, 너무 노가다성을 띔.

전개연산자를 사용한 배열테크닉을 이용하면 쉽게 배열의 깊은복사를 할 수 있다.

#### 전개연산자를 이용한 배열의 결합

![image-20200129144050563](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129144050563.png)

![image-20200129144056305](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129144056305.png)

#### 전개연산자를 이용한 객체의 깊은 복사

![image-20200129144324255](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129144324255.png)

![image-20200129144329558](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200129144329558.png)

