## React 3.

### p.106 UI 라이브러리를 사용하지 않는 코드

C:\react\hello-react2\todo.html 파일을 생성
C:\react\hello-react2>npx http-server
 http://localhost:8080/todo.html → 실행 확인



### P.107 동일한 기능을 리액트로 작성

// 템플릿

```
import React from 'react';

class MyComponent extends React.Component {
    state = {
        desc: '', 
        currentId: 1, 
        todoList: [],
    };

    onAdd = () => {
        const { desc, currentId, todoList } = this.state;
        const todo = { id: currentId, desc };
        this.setState({
            currentId: currentId + 1, 
            todoList: [ ...todoList, todo ]
        });
    };

    onDelete = e => {
        const { todoList } = this.state;
        const id = Number(e.target.dataset.id);
        const newTodoList = todoList.filter(todo => todo.id !== id);
        this.setState({ todoList: newTodoList });
    };

    onSaveToServer = () => {
        console.log(this.state.todoList);
    };

    onChangeDesc = e => {
        // this.setState({ desc: e.target.value });
        const desc = e.target.value;
        this.setState({ desc });
    };

    render() {
        const { desc, todoList } = this.state;
        return (
            <div>
                <h3>할 일 목록</h3>
                <ul>
                    {
                        todoList.map(todo => { 
                            console.log(todo);
                            return (                            
                            <li key={todo.id}>
                                <span>{todo.desc}</span>
                                <button data-id={todo.id} onClick={this.onDelete}>삭제</button>
                            </li>
                            );
                        })
                    }
                </ul>
                <input type="text" value={desc} onChange={this.onChangeDesc} />
                <button onClick={this.onAdd}>추가</button>
                <button onClick={this.onSaveToServer}>서버에 저장</button>
            </div>
        );
    }
}

export default MyComponent;
```



### P.109 컴포넌트의 상태값을 사용하는 코드

// App.js - LAB1

![image-20200206172501545](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200206172501545.png)



// LAB2

![image-20200206173612342](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200206173612342.png)



### P.110 부모 컴포넌트에서 속성값을 내려 주는 코드

// App.js

![image-20200206175205618](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200206175205618.png)

// Title.js

![image-20200206175220024](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200206175220024.png)

// Todo.js

![image-20200206175242887](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200206175242887.png)

![image-20200206175302278](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200206175302278.png)

![image-20200206175547272](C:\Users\HPE\AppData\Roaming\Typora\typora-user-images\image-20200206175547272.png)



### P.111 React.memo, React.PureComponent 사용

자식 컴포넌트는 부모 컴포넌트가 렌더링될 때 함께 렌더링된다.
"증가2" 버튼을 클릭했을 때 자식 컴포넌트도 함께 렌더링된다. ⇒ 불필요한 렌더링이 발생한다. 
⇒ 방지하기 위해서는 React.memo, React.PureComponent를 사용

// App.js

![image-20200207093416824](images/image-20200207093416824.png)



// Todo.js

![image-20200207093433720](images/image-20200207093433720.png)



// Title.js

![image-20200207093450971](images/image-20200207093450971.png)



#### Title.js - React.memo 사용

![image-20200207093838675](images/image-20200207093838675.png)

![image-20200207093747288](images/image-20200207093747288.png)

// 함수형 컴포넌트인 경우, React.memo를 이용해서 자식 컴포넌트의 불필요한 렌더링을 줄일 수 있음
// props 값이 변경되는 경우에만 호출되는 것을 확인할 수 있음

#### Title.js - React.PureComponent 사용

// 클래스형 컴포넌트인 경우,
// React.PureComponent를 이용하면 자식 컴포넌트의 불필요한 렌더링을 줄일 수 있음
// 함수형 Component

![image-20200207094138897](images/image-20200207094138897.png)



### P.112 setState

// 클래스형 컴포넌트에서 상태값을 변경할 때 호출하는 메소드
// setState 메소드로 입력된 객체는 기존 상태값에 병합(merge)

// App.js

![image-20200207095136687](images/image-20200207095136687.png)



### P.113 setState 메소드를 연속해서 호출하면 발생하는 문제점

**리액트는 효율적인 렌더링을 위해서 여러 개의 setstate 메서드를 배치로 처리 → state 변수와 화면(UI) 간 불일치가 발생할 수 있음**

![image-20200207101242002](images/image-20200207101242002.png)



// 방법 1. 호출 직전의 상태값을 매개변수로 받아서 처리

![image-20200207101551198](images/image-20200207101551198.png)



// 방법2. 상태값 로직을 분리해서 사용

![image-20200207102523194](images/image-20200207102523194.png)



### P.114 sestState 메소드

 비동기로 처리되지만 호출 순서는 보장된다.

![image-20200207104601931](images/image-20200207104601931.png)



### P.115 SetState 메소드의 두번째 매개변수

처리가 끝났을 때 호출되는 콜백 함수
https://ko.reactjs.org/docs/react-component.html#setstate

![image-20200207104705521](images/image-20200207104705521.png)



### P.117 comde 3-18

JSX 코드에서 태그 사이에 표현식이 들어가면, 표현식을 기준으로 분할되어서 들어간다

![image-20200207110646192](images/image-20200207110646192.png)



### P.116 리액트 요소

![image-20200207112025183](images/image-20200207112025183.png)

![image-20200207112101881](images/image-20200207112101881.png)



### P.119 리액트 요소가 돔 요소로 만들어지는 과정

// App.js

![image-20200207113704008](images/image-20200207113704008.png)



// Todo.js

![image-20200207113719419](images/image-20200207113719419.png)



// Title.js

![image-20200207113733756](images/image-20200207113733756.png)



// result

![image-20200207113826892](images/image-20200207113826892.png)



### P.137 componentDidMount 메소드

```
C:\react\hello-react2\src\Box.js
```

// App.js

![image-20200207153953481](images/image-20200207153953481.png)

// Box.js

![image-20200207154848648](images/image-20200207154848648.png)





### P.140 shouldComponentUpdate, getSnapshotBeforeUpdate

![image-20200207163511012](images/image-20200207163511012.png)

![image-20200207163529868](images/image-20200207163529868.png)



### P.145 자식 컴포넌트에서 발생한 예외를 부모 컴포넌트에서 처리

#### ErrorBoundary.js

// Counter.js

![image-20200207164553274](images/image-20200207164553274.png)



// App.js

![image-20200207164308695](images/image-20200207164308695.png)



// ErrorBoundary.js

![image-20200207164533586](images/image-20200207164533586.png)

* 부모 컴포넌트에서 child 컴포넌트에서 발생하는 에러를 잡고 싶아서, 그에 맞는 조치를 취함
* 그 에러정보를 담고있는 상태변수 error:null 을 만들고, 에러에 값이 있으면 문자열, 
  값이 없으면 해당하는 child를 rendering 해준다.
* 그러한 error를 잡기 위해서는 144p 에 있는 getDerivedState를 이용한다.

![image-20200207165316980](images/image-20200207165316980.png)

![image-20200207165553486](images/image-20200207165553486.png)



### P.148 컨텍스트 API

상위 컴포넌트에서 하위에 있는 모든 컴포넌트로 직접 데이터 전달이 가능

![image-20200207171231463](images/image-20200207171231463.png)

// 컨텍스트 API를 사용하지 않으면 속성값(pros)로 전달

![image-20200207171847638](images/image-20200207171847638.png)



// 컨텍스트 API를 사용

![image-20200207173106836](images/image-20200207173106836.png)



// 중간 컴포넌트의 렌더링 여부에 상관 없이 Provider 컴포넌트의 값이 바뀌면
// Consumer 컴포넌트가 렌더링을 수행한다.

![image-20200207174000797](images/image-20200207174000797.png)



### P.150 여러 컨텍스트를 중첩해서 사용

![image-20200207174904303](images/image-20200207174904303.png)