## JavaScript 19

### p.588 Colorbox 플러그인

![image-20200130160720170](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130160720170.png)

![image-20200130163037324](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130163037324.png)

![image-20200130163131417](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130163131417.png)





## JavaScript 21

### Ajax 개요



### CSV 형식

각 항목을 수미표로 구분해 데이터를 표현하는 방법

* 많은 양의 데이터를 전송할 때 활용



### XML 형식

XML : HTML형식처럼 태그를 가지고 데이터를 표현하는 것

* 각각의 태그에 사용자 정의 속성을 넣어 데이터를 표현할 수도 있다
  * 복잡한 데이터를 전달 가능
* 닫는 태그와 여는 태그 등이 쓸데 없이 용량 차지



### JSON 형식

CSV 형식과 XML 형식의 단점을 모두 극복한 형식

JavaScript에서 사용하는 객체 형태로 데이터를 표현하는 방법

* 우선, students.json 파일을 새로 만든다.

![image-20200130164131419](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130164131419.png)

* localhost:8080/students.json 에 들어가서 확인한다.

![image-20200130164152748](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130164152748.png)



![image-20200130171729575](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130171729575.png)

![image-20200130171737028](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130171737028.png)

![image-20200130171745682](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130171745682.png)



부모가 자식에게 내려주는값, 자식이 부모로부터 물려받는 값 =>  property

부모가 유지하고 있는 값, 자식이 유지하고 있는 값 => state



#### LAB

사이트 미리보기를 제작

* jQuery UI에서 제공하는 TAB 위젯을 이용
* 미리보기 사이트 명과 주소(URL)은 ajax 통신으로 가져오기
* /preview.html => 미리 보기 사이트
* /siteinfo.html => 미리 보기 사이트 명과 주소를 포함한 JSON 형식의 파일