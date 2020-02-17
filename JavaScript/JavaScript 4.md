# JavaScript 4

### 반복문

```
for ([1]변수=초기값; [2][5]조건문; [4][7]증가분) {
	[3][6]조건문을 만족하는 경우 수행할 구문
}
```

증가 후 비교, 



#### 배열

여러 개의 변수를 한꺼번에 선언해 다룰 수 있는 자료형
객체 자료형 중 하나

```
<script>
            // p98 배열
            // 배열 선언
            let arr = [ 273, 'String', true, function() {}, {}, [ 100, 200 ] ];
            //           숫자    문자열    불     함수         객체    배열
            console.log(arr);
            console.log(arr.length);
            console.log(arr[0]);	// 해당하는 배열의 0번째 값 출력
        </script>
```

![image-20200123160035656](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123160035656.png)

![image-20200123160021977](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123160021977.png)

* for loop 방법

![image-20200123160218345](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123160218345.png)

![image-20200123160228955](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123160228955.png)

* forEach

![image-20200123160704562](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123160704562.png)

![image-20200123160715506](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123160715506.png)

![image-20200123161409769](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123161409769.png)

#### while 반복문

![image-20200123162111873](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123162111873.png)

![image-20200123162116580](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123162116580.png)

while 반복문 : 계속 반복

![image-20200123163147490](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123163147490.png)

![image-20200123163251865](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123163251865.png)

![image-20200123163307043](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123163307043.png)

![image-20200123163334622](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123163334622.png)

```
    <script>
        //  숫자 맞추기 게임
        //  1~20 사이의 임의의 숫자를 맞추는 게임
        const MIN = 1;
        const MAX = 20;
 
        let answer = Math.floor(Math.random() * (MAX - MIN + 1)) + MIN;
        let guesses = 0; // 사용자가 입력한 회수
        let input;
        do {
            input = prompt(`${MIN} ~ ${MAX} 사이의 숫자를 입력하세요.`);
            input = Number(input);
            guesses ++;
 
            if (input > answer) {
                console.log("입력한 값 보다 작은 값을 입력하세요");
            } else if (input < answer) {
                console.log("입력한 값 보다 큰 값을 입력하세요");
            } else {
                console.log(`정답입니다. (시도회수: ${guesses})`);
            }
        } while (input !== answer);
    </script>
```

![image-20200123164902158](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123164902158.png)

![image-20200123164909302](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200123164909302.png)

* while 반복문ㅇ르 종료하려면 조건을 변화시킬 수 있는 요소가 있어야 한다.