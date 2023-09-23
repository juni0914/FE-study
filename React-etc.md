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

<h4> - DOM은 HTML과 스크립팅 언어(Javascript)를 서로 이어주는 역할 </h4><br>

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
