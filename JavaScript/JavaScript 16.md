 ## JavaScript 16

### p.502 간단한 이벤트 연결

![image-20200130113114515](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130113114515.png)

![image-20200130113123537](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130113123537.png)

→ 클릭하는 것들이 콘솔에 보인다.



![image-20200130113246454](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130113246454.png)

→ 커서가 손가락 클릭 버튼으로 바뀐다.



![image-20200130113648374](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130113648374.png)

![image-20200130113753028](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130113753028.png)

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130113807773.png" alt="image-20200130113807773" style="zoom:50%;" />

→ 항목에 대해 클릭이 되고, 출력된 값에 대해서도 클릭이 되어 배로 늘어난다.
	이 때 필요한 것이 후손선택자.



#### 후손선택자

div, id가 input이라는 div를 기준으로 그 div에 대해서만 클릭을 잡겠다.

![image-20200130114240636](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130114240636.png)

![image-20200130113958963](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130113958963.png)

→ 항목에 대해 클릭은 가능하나, 출력된 값에 대해서는 클릭이 되지 않는다.



<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130132336568.png" alt="image-20200130132336568" style="zoom: 80%;" />





<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130133017486.png" alt="image-20200130133017486" style="zoom:80%;" />

![image-20200130133026232](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130133026232.png)



### 구구단

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130133327880.png" alt="image-20200130133327880" style="zoom:80%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130133342389.png" alt="image-20200130133342389" style="zoom: 67%;" />

**간단하게

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130133541798.png" alt="image-20200130133541798" style="zoom:80%;" />

**uppend는 계속 나오게**
**empty를 이용하여 하나의 값들만 출력되게**

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130134055446.png" alt="image-20200130134055446" style="zoom:80%;" />



### p.430 mouseover, mouseleave 이벤트 처리

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130135102938.png" alt="image-20200130135102938" style="zoom:80%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130135109304.png" alt="image-20200130135109304" style="zoom:50%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130135117343.png" alt="image-20200130135117343" style="zoom: 80%;" />



#### 진입, 진출 시 색 처리

![image-20200130141731861](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130141731861.png)

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130141739540.png" alt="image-20200130141739540" style="zoom:67%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130141754427.png" alt="image-20200130141754427" style="zoom: 67%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130141808036.png" alt="image-20200130141808036" style="zoom: 67%;" />

![image-20200130141833781](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130141833781.png)

![image-20200130142028898](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130142028898.png)

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130142045226.png" alt="image-20200130142045226" style="zoom:67%;" />

![image-20200130142104101](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130142104101.png)



![image-20200130142259610](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130142259610.png)

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130142308817.png" alt="image-20200130142308817" style="zoom:67%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130142320052.png" alt="image-20200130142320052" style="zoom:67%;" />

<img src="C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200130142336148.png" alt="image-20200130142336148" style="zoom:67%;" />

### p.431 jQuery 충돌 방지

```
$.noConflict()
```

변수로 사용 가능한 것 : _(언더바), $(달러)

$ 기호의 중복 사용 혼돈을 막기 위해서 $.noConflict()

가독성이 떨어지고 많이 써야 함, noConflict() 하고 jQuery 대신에 J를 쓰겠다. (J("div"), JJ("div"))

