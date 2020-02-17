## JavaScript 5



### 익명함수

함수는 코드의 집합을 나타내는 자료형이다. alert()나 prompt()가 함수의 예이다.

```
var 함수 = function() {};
```

함수가 코드의 집합이라고 말하는 이유는 괄호 내부에 코드를 넣기 때문이다.

![image-20200128142503506](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128142503506.png)

세미콜론을 넣어주는게 예의이다.



### p124 함수 재정의
동일한 이름의 함수가 중복해서 정의되는 것

![image-20200128143808564](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128143808564.png)

![image-20200128143817077](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128143817077.png)





![image-20200128143713510](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128143713510.png)

![image-20200128143720670](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128143720670.png)

**순서 호출**

선언문 형태로 쓰는 것과 함수 표현식 형태로 쓰는 것의 차이점을 알 수 있다. 우리가 왜 표현식 형태로 써야 하는지
밑의 code는 함수가 아니다. 그래서 오류가 나는 것이다.



### 선언적 함수

![image-20200128145533342](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128145533342.png)



### 매개변수

![image-20200128145934235](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128145934235.png)

![image-20200128145939304](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128145939304.png)

함수 보는 방법

![image-20200128151649086](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128151649086.png)

![image-20200128151709357](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128151709357.png)



### p.130 가변 인자 함수

가변 인자 함수는 매개변수의 개수가 변할 수 있는 함수
매개변수를 선언된 형태와 다르게 사용했을 때, 매개변수를 모두 활용하는 함수

파라미터(매개변수)의 개수가 변할 수 있는 (=고정되어 있지 않은 함수) 함수

**→ 함수 객체의 arguments 속성을 이용해서 매개변수를 이용(처리)**

모든 함수에는 arguments가 있다.
new function()을 이용해서 만들 수 있다. function이라는 개체가 arguments를 가지고 있기 때문에
이것을 이용해서 만들어지는 함수는 모두 arguments를 가지고 있다.

**자바스크립트의 모든 함수는 내부에 기본적으로 변수 arguments 가 있다.**

![image-20200128152225978](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128152225978.png)

![image-20200128152232362](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128152232362.png)

![image-20200128152624371](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128152624371.png)

![image-20200128152631309](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128152631309.png)

​														*→ arguments를 잘 활용하면 이렇게 가능하다.*

#### 매개변수가 다른 경우

매개변수의 개수를 가져와서 조건을 나누어 준다.



### p. 133 리턴 값

원래 return 키워드는 함수가 실행되는 도중에 함수를 호출한 곳으로 돌아가라는 의미
따라서 return 키워드를 사용하면 값을 지정하지 않아도 함수를 호출한 곳으로 돌아감

![image-20200128153551120](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128153551120.png)

![image-20200128153555379](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128153555379.png)

*return 이 있으면 아래의 함수는 처리하지 않는다.*

![image-20200128155426215](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128155426215.png)

![image-20200128155436594](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128155436594.png)

![image-20200128170605926](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128170605926.png)

find 개체를 이용하면 된다. find 해서 해당하는 item 이 조건을 만족하면 item을 return한다.
arguments를 배열로 만들기 위해서는 Array.from  할 수도 있다.

### p.135 내부 함수

프로그램 규모가 크거나, 여러 사람이 함께 작업하다 보면 동일한 이름의 함수가 만들어 질 수 있는데,
그 와중에 여러가지 충돌이 발생하게 된다. 내부 함수는 이러한 충돌을 막는 방법이다.

**함수 내부에서 함수를 정의하는 것을 내부 함수라 한다.**

![image-20200128161739219](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128161739219.png)

![image-20200128162126153](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128162126153.png)

![image-20200128162138710](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128162138710.png)

이것을 간단히 쓰면,

![image-20200128162253984](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128162253984.png)



함수의 재정의 오류

![image-20200128162704946](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128162704946.png)

![image-20200128162710612](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128162710612.png)

![image-20200128162809928](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128162809928.png)

![image-20200128162814252](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128162814252.png)

이게 내부함수다. 함수의 이름 중복을 막고, 동일한 이름의 내부함수와 외부함수가 있다라면 내부함수를 우선적으로 사용한다.

#### p. 139자기 호출 함수

다른 개발자에게 영향을 주지 않게 함수를 만들어 사용.
생성하자마자 한 번 호출된다.

```
let f = function ()
이렇게 호출하면 console.log("^^") 했을 때 ^^ 가 호출
이것을 다른 변수로 다룰 필요 없이 한 번만 호출되기 때문에
함수의 기능이 정의됨과 동시에 호출
```

![image-20200128163334116](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128163334116.png)

![image-20200128163345450](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128163345450.png)

![image-20200128163410563](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128163410563.png)

![image-20200128163415705](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128163415705.png)

#2가 자기 호출 함수. 괄호로 한 번 묶어준다.

### p.139 콜백 함수

결과를 확인하고 다음으로 넘어가는 처리 방식 : 동기화 처리

![image-20200128165131776](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128165131776.png)

![image-20200128165136276](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128165136276.png)

![image-20200128170242627](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128170242627.png)

이렇게 바꿔줄 수도 있다. callback(c, c1)



### 함수를 리턴하는 함수

![image-20200128171711661](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128171711661.png)

![image-20200128171717002](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128171717002.png)

맨 마지막 줄의 returnFunction()(); 에 의해 웃는얼굴 두 개 나온다. () 하나면 웃는얼굴 하나.



### 클로저

지역 변수의 유효 범위


![image-20200128172241609](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128172241609.png)

![image-20200128172246670](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128172246670.png)

output이라는 것은 함수 안에 정의되어 있다. 함수 안에 정의되어있는 변수는 해당하는 함수 안에서만 유효 범위를 가진다. f() 밖의 함수는 정의되어있지 않아서, 오류가 뜬다.

클로저의 정의는 워낙 다양하다. 지역 변수를 남겨두는 현상을 클로저라 부르기도 하고,
함수 내부의 변수들이 살아있는 것이므로 test() 함수로 생성된 공간을 클로저라 부르기도 한다.

호출 이후 반환값을 호출하니까 output을 쓸 수 있는 것이다. 

![image-20200128173412668](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128173412668.png)

```
function() { console.log(output); };		→클로저
```

함수 내부에 사용된 함수를 반환된 이후에 사용 가능. 지연 가능. 이러한 현상을 클로저

지역변수 output을 남겨둔다고 외부에서 마음대로 사용할 수 있는 것은 아님
반드시 리턴된 클로저 함수를 사용해야 지역 변수 output을 사용할 수 있다.
클로저 함수로 인해 남은 지역 변수는 클로저 함수 각각의 고유한 변수이다.

![image-20200128173726228](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128173726228.png)

![image-20200128173730242](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200128173730242.png)