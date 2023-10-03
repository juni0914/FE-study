# React-etc

<br>

<h1> 1. Virtual DOM</h1>

## 🌟 DOM의 정의 🌟
<h4>
	
- DOM (Document Object Model)은 웹 페이지의 구조와 콘텐츠를 표현하는 데 사용되는 표준 프로그래밍 인터페이스다.<br><br>
- DOM은 웹 페이지의 모든 요소를 계층 구조로 표현하며, 각 요소는 객체로 표현된다.<br><br>
- 이 객체들은 JavaScript를 사용하여 조작하고 변경할 수 있으며, 웹 페이지의 동적 상호작용 및 구조 변경을 가능하게 한다.<br><br>
- DOM의 주요 특징은 다음과 같다.<br>
</h4>
<br>

### 🌈 HTML의 DOM 트리 구조 🌈

![image](https://github.com/juni0914/react-blog/assets/100837725/b7e46b5a-a229-4ff4-90b4-b3b8ed722698)

<h4> - DOM은 HTML과 스크립팅 언어(Javascript)를 서로 이어주는 역할이다. </h4><br>

![image](https://github.com/juni0914/react-blog/assets/100837725/e4e64b7a-befb-48fd-a25d-b3a2f0911c78)

### ⛅ Virtual DOM ⛅
<h4>
	
✔ 그렇다면 Virtual DOM을 알아보자.<br><br>

React의 장점 중에는 Virtual DOM이 있다. <br><br>

- Virtual은 말 그대로 가상이라는 뜻이고 DOM은 Document Object Model의 약자로 그대로 해석하면 문서 객체 모델을 의미한다. <br><br>
- 문서 객체한 HTML, head, body와 같은 태그들을 Javascript가 이용할 수 있는 객체를 의미한다.<br><br>
- 개발을 하면서 자주보게 되는 div, input, a 등이 DOM에 해당한다.<br><br>
- 가상 DOM(Virtual DOM)은 웹 애플리케이션의 성능을 향상시키기 위한 개념으로, 웹 개발에서 실제 DOM 조작이 발생하는 빈도와 비용을 줄이기 위해 도입되었다.<br><br>
- 아래는 가상 DOM이 나오게 된 주요 이유들이다.<br><br>
<hr>

* DOM 조작 비용

* 빈번한 업데이트

* 웹 애플리케이션 복잡성

* 다양한 브라우저 지원
</h4>

<h3>
🔥 리액트의 Virtual DOM은 개발자가 간편하게 UI를 업데이트하고 상태를 관리할 수 있도록 도와준다. <br><br>
🔥 개발자는 UI를 업데이트하고 상태를 변경할 때마다 실제 DOM 조작을 수행하는 대신<br><br> Virtual DOM을 업데이트하고 리액트가 최적의 방식으로 변경 사항을 실제 DOM에 적용한다. <br><br>
🔥 이로써 성능이 향상되며, 웹 애플리케이션의 반응성이 향상된다!<br><br>
</h3>
<br>
<br>

<h1> 2. Restful API</h1>

## 🌟 Restful API의 정의 🌟<br>
<h4>
	
✔ RESTful API(Representational State Transferful Application Programming Interface)는<br><br> 웹 애플리케이션의 데이터와 서비스를 외부에서 활용할 수 있도록 제공하는 인터페이스다.<br><br>
RESTful API는 웹 리소스에 접근하고 조작하기 위한 규칙과 규약을 정의하며, HTTP 프로토콜을 사용하여 통신한다.<br><br>
RESTful API를 이해하고 사용하는 것은 프론트엔드 개발자에게 매우 중요한 역할을 한다.<br><br><br><br>

🔥 RESTful API에 대한 주요 개념과 이점 <br><br>

- 자원(Resource): RESTful API에서는 모든 것이 리소스로 표현된다.<br><br>
이 리소스는 URI(Uniform Resource Identifier)로 식별되며, 프론트엔드 개발자는 이 URI를 통해 리소스에 접근하고 조작한다. <br><br>
예를 들어, /users, /products와 같은 리소스를 다룬다.<br><br>

- HTTP 메서드: HTTP 메서드(GET, POST, PUT, DELETE 등)는 RESTful API에서 다양한 작업을 수행하는 데 사용된다. <br><br>
프론트엔드 개발자는 이 메서드를 사용하여 리소스를 가져오기, 생성하기, 수정하기, 삭제하기 등의 작업을 수행한다. <br><br>

- 상태(State): RESTful API는 상태를 관리하며, 클라이언트와 서버 간의 통신을 통해 상태를 변경하거나 가져올 수 있다. <br><br>
이를 통해 프론트엔드 개발자는 원격 서버에 저장된 데이터를 가져오고 업데이트할 수 있다.<br><br>

- 표현(Representation): 리소스의 상태는 다양한 표현 형식으로 표시된다. <br><br>
주로 JSON 또는 XML 형식을 사용하며, 프론트엔드 개발자는 이 데이터를 파싱하여 화면에 표시하거나 다른 작업에 활용한다. <br><br>

- 무상태(Stateless): RESTful API는 무상태성을 가지고 있으며, 각 요청은 독립적으로 처리된다. <br><br>
서버가 클라이언트의 상태를 관리하지 않으며, 프론트엔드 개발자는 필요한 정보를 요청과 함께 제공해야 한다.<br><br>

- 유니폼 인터페이스(Uniform Interface): RESTful API는 일관된 인터페이스를 제공하며, <br><br>
이를 통해 프론트엔드 개발자는 다양한 서버와 통신하는 데 일관된 방법을 사용할 수 있다.<br><br>

- URI 설계: URI는 리소스를 식별하는 데 중요하다. <br><br>
명확하고 의미 있는 URI 설계는 API의 사용성을 높이고 프론트엔드 개발자가 빠르게 이해하고 활용할 수 있도록 도움을 준다.
</h4>

## 🌈 예시 코드 🌈<br>

```
// RESTful API 엔드포인트 URL
const apiUrl = 'https://jsonplaceholder.typicode.com/posts';

// GET 요청을 보내는 함수
async function fetchPosts() {
  try {
    const response = await fetch(apiUrl);
    
    if (!response.ok) {
      throw new Error(`HTTP Error! Status: ${response.status}`);
    }
    
    const data = await response.json();
    console.log('서버로부터 받은 데이터:', data);
    
    // 여기에서 데이터를 활용하여 웹 페이지에 표시할 수 있습니다.
  } catch (error) {
    console.error('오류 발생:', error);
  }
}

// GET 요청 실행
fetchPosts();

```
<br>
<br>

<h1> 3. forwardRef</h1>

## 🌟 정의 🌟
<h4>
	
- 함수 컴포넌트에서 ref 속성을 전달하고, 해당 ref를 자식 컴포넌트에 직접 전달하도록 도와주는 기능이다.<br><br>
- 이를 통해 함수 컴포넌트가 ref를 받아서 자식 컴포넌트에게 전달할 때 발생할 수 있는 문제를 해결할 수 있다.<br><br>
- forwardRef는 주로 컴포넌트 간 통신이나 DOM 요소에 대한 직접적인 접근이 필요한 경우에 사용된다.<br><br>

</h4>
<br>

### 🌈 forwardRef의 주요 특징과 사용 방법 🌈

<h4>
	
- forwardRef 함수 사용 : forwardRef 함수를 호출하여 컴포넌트를 생성한다. 이 함수는 두 개의 인자를 받는다. (props와 ref)<br><br>

- ref 속성 전달 : forwardRef로 생성한 컴포넌트를 다른 컴포넌트에서 사용할 때, ref 속성을 전달한다.<br> 이 ref는 함수 컴포넌트에서 사용될 수 있다.<br><br>

- ref 전달 : forwardRef 함수 내에서 전달받은 ref를 자식 컴포넌트(또는 DOM 요소)에 전달한다.<br><br>

이렇게 하면 함수 컴포넌트가 ref 속성을 받아서 자식 컴포넌트에게 직접 전달할 수 있으며, ref를 사용하여 자식 컴포넌트의 DOM 요소에 접근할 수 있다.<br><br>

</h4>

### ⛅ 예시 코드 ⛅
<h4>
	

```
import React, { forwardRef, useRef, useImperativeHandle } from 'react';

// forwardRef로 컴포넌트 생성
const CustomInput = forwardRef((props, ref) => {
  const inputRef = useRef(null);

  // useImperativeHandle을 사용하여 외부에서 접근 가능한 메서드 정의
  useImperativeHandle(ref, () => ({
    focus: () => {
      inputRef.current.focus();
    },
    // 다른 커스텀 메서드들도 여기에서 정의할 수 있다.
  }));

  return <input type="text" ref={inputRef} />;
});

// 부모 컴포넌트
function ParentComponent() {
  const inputRef = useRef(null);

  const handleButtonClick = () => {
    // 자식 컴포넌트의 focus 메서드 호출
    inputRef.current.focus();
  };

  return (
    <div>
      <CustomInput ref={inputRef} />
      <button onClick={handleButtonClick}>입력란에 포커스 주기</button>
    </div>
  );
}

```

- 위의 코드에서 CustomInput 컴포넌트는 forwardRef를 사용하여 ref를 받아서 input 요소에 직접 전달한다.<br><br>
- useImperativeHandle을 사용하여 외부에서 접근 가능한 메서드를 정의하고, <br>
  부모 컴포넌트에서는 ref를 사용하여 CustomInput 컴포넌트의 메서드를 호출한다. <br><br>
- 이를 통해 부모 컴포넌트는 자식 컴포넌트의 DOM 요소나 메서드에 접근할 수 있다. <br><br>
</h4>
<br>
<br>

<h1> 4. Flux pattern</h1>

## 🌟 정의 🌟
<h4>
	
- Flux는 리액트 애플리케이션의 상태 관리 패턴 중 하나로, 애플리케이션 데이터의 단방향 흐름을 유지하고 관리하기 위한 아키텍처다. <br><br>
- Flux 패턴은 Facebook에서 개발되었고, 리액트 애플리케이션의 상태 관리를 더욱 예측 가능하고 효율적으로 만들어주는데 도움을 준다.<br><br>


</h4>
<br>

### 🌈 Flux 패턴의 주요 요소 🌈<br>
![image](https://github.com/juni0914/react-blog/assets/100837725/0a788d1d-f7c9-4c00-abe2-957503161144)<br><br>
<h4>
	
1.액션(Action)<br><br>
액션은 애플리케이션에서 어떤 변화가 일어났음을 설명하는 객체다.<br><br>
액션은 주로 사용자의 입력 또는 네트워크 응답과 같은 이벤트에 의해 발생한다.<br><br>
예를 들어, "사용자가 로그인 버튼을 클릭했다" 또는 "새로운 데이터가 서버에서 도착했다"와 같은 상황에서 액션을 생성한다.<br><br><br>

2.디스패처(Dispatcher)<br><br>
디스패처러는 액션을 받아서 등록된 모든 스토어에 액션을 전달하는 중앙 허브 역할을 한다.<br><br>
액션을 처리할 스토어에 알려주고 스토어의 업데이트를 시작하는 역할을 한다.<br><br><br>

3.스토어(Store) / Model<br><br>
스토어는 애플리케이션의 상태를 포함하고 있으며, 상태를 관리하고 업데이트하는 로직을 구현한다.<br><br>
스토어는 뷰 컴포넌트에 데이터를 제공하고, 뷰 컴포넌트에서 발생한 액션을 처리하여 상태를 업데이트한다.<br><br><br>

4.뷰(View)<br><br>
뷰는 사용자 인터페이스를 표시하는 부분으로, 리액트 컴포넌트로 구현된다.<br><br>
뷰는 스토어로부터 상태 데이터를 받아와 렌더링하고, 사용자 입력을 감지하여 액션을 발생시킨다.<br><br><br>
</h4>

### ⛅ Flux 패턴의 흐름 ⛅<br><br>
<h4>

1.사용자는 뷰에서 어떤 상호 작용을 하면 액션을 발생시킨다.<br><br>


2.액션은 디스패처에 의해 스토어로 전달된다.<br><br>


3.스토어는 액션을 처리하고 상태를 업데이트한다.<br><br>


4.상태가 업데이트되면 스토어는 뷰에 변경된 데이터를 전달한다.<br><br>


5.뷰는 변경된 데이터를 화면에 렌더링한다.<br><br><br><br>


- 이러한 단방향 데이터 흐름은 예측 가능하며 애플리케이션의 상태 변화를 추적하기 쉽게 만들어준다.<br><br>

 

- 또한 여러 개의 뷰 컴포넌트가 동일한 스토어를 공유하여 데이터 일관성을 유지하고 중복 로직을 최소화할 수 있다.<br><br>

- Flux 패턴은 리액트에서 직접 사용할 수도 있지만, Redux나 Mobx와 같은 상태 관리 라이브러리가 Flux 패턴을 기반으로 만들어져 더욱 편리한 상태 관리를 제공한다.<br><br>

![image](https://github.com/juni0914/react-blog/assets/100837725/390affa9-0eb2-40fb-a0d5-6ca2877de321)<br><br>
각 요소들은 단방향 흐름에 따라 순서대로 역할을 수행하고, View로부터 새로운 데이터 변경이 생기면 처음부터 다시 이 순서대로 실행한다.<br><br>

 

이렇게 함으로써 예외 없이 데이터를 처리할 수 있게 된다.<br><br>

</h4>


<br>
<br>
