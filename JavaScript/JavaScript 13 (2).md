## JavaScript 13 (2)

![image-20200130093336780](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130093336780.png)

![image-20200130093348375](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130093348375.png)

동시적으로 선택 가능한 것 : checkbox

베타적으로 선택 가능한 것 : radio

file이라는 type : 임의의 파일을 

![image-20200130093800063](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130093800063.png)

![image-20200130093708309](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130093708309.png)

[file:///C:/javascript/java/code1-3.html?lastName=Lee&firstName=Yeojin&pw=flduwld160&pw2=flduwld160&ismarried=N&color=red&color=blue&photo=&%EC%A0%84%EC%86%A1=%EC%A0%9C%EC%B6%9C#](file:///C:/javascript/java/code1-3.html?lastName=Lee&firstName=Yeojin&pw=flduwld160&pw2=flduwld160&ismarried=N&color=red&color=blue&photo=&전송=제출#)

요청 파라미터(request parameter) : get방식 (get method)  → (name=value)
위의 주소에 lastName~ 부터 파라미터.
POST방식으로 하고 싶다면,

```
form action="#" method="post"
```

Default는 Get

* 적어주라는 메세지를 남기고 싶다.

![image-20200130094817225](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130094817225.png)

![image-20200130094823560](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130094823560.png)

* 성과 이름을 따로 적어주고 싶다.

![image-20200130094900953](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130094900953.png)

![image-20200130094924511](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130094924511.png)

### 속성 선택자

| 선택자 형태 | 설명                                                    |
| ----------- | ------------------------------------------------------- |
| E[A=V]      | 속성 안의 값이 특정 값과 같은 객체 선택                 |
| E[A!=V]     | 속성 안의 값이 특정 값과 같은 문서 객체 선택            |
| E[A~=V]     | 속성 안의 값이 특정 값을 단어로 시작하는 문서 객체 선택 |
| E[A^=V]     | 속성 안의 값이 특정 값으로 시작하는 문서 객체 선택      |
| E[A$=V]     | 속성 안의 값이 특정 값으로 끝나는 문서 객체 선택        |
| E[A*=V]     | 속성 안의 값이 특정 값을 포함하는 문서 객체 선택        |

![image-20200130103001509](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130103001509.png)

#### A!=V

> 속성값이 다른 문서 객체 선ㄴ택

![image-20200130101651285](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130101651285.png)

![image-20200130101535107](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130101535107.png)

type이 file인 사진을 제외한 나머지 항목에 "(필수입력)" 적용, 글자색을 바꾸었다.



#### A~=V

> 속성값에 단어가 포함된 객체 선택

![image-20200130102122421](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102122421.png)

![image-20200130102128314](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102128314.png)

#### A^=V

> 속성값이 글자로 시작하는 객체를 선택

![image-20200130102248996](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102248996.png)

![image-20200130102309065](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102309065.png)

#### A$=V

> 속성값이 글자로 끝난는 객체를 선택

![image-20200130102421267](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102421267.png)

![image-20200130102441129](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102441129.png)

#### A*=V

> 속성값에 글자를 포함한 객체를 선택

![image-20200130102550579](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102550579.png)

![image-20200130102600192](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130102600192.png)

---

* hide : 해당하는 Element를 숨기는 명령.

![image-20200130104712125](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130104712125.png)

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130104734521.png" alt="image-20200130104734521" style="zoom:50%;" />

---

![image-20200130104635912](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130104635912.png)

![image-20200130104628899](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130104628899.png)

---

![image-20200130104646634](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130104646634.png)

![image-20200130104652601](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130104652601.png)

---

* margin : 10px 	20px	30px		40px

  ​				 top	   right	bottom	left

![image-20200130104900329](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130104900329.png)

→ 상, 하, 좌, 우 가 바뀌는 것을 볼 수 있다.

---

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130105120701.png" alt="image-20200130105120701" style="zoom:67%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130105126599.png" alt="image-20200130105126599" style="zoom:33%;" />

---

내가 char red만 찾고 싶다

```
div[class="char red"] {
background: indigo;
}
```

![image-20200130110904775](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130110904775.png)

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130110851096.png" alt="image-20200130110851096" style="zoom:50%;" />

---

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130111355736.png" alt="image-20200130111355736" style="zoom: 80%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130111428036.png" alt="image-20200130111428036" style="zoom: 50%;" />

---

![image-20200130111535456](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130111535456.png)

![image-20200130111542614](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130111542614.png)

---

![image-20200130111741621](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130111741621.png)

![image-20200130111754450](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130111754450.png)

---

![image-20200130112402435](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130112402435.png)

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130112409072.png" alt="image-20200130112409072" style="zoom:50%;" />

→ 기본값으로 변경된 것을 볼 수 있다.

