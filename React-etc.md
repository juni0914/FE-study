# React-etc

<br>

<h1> 1. Virtual DOM</h1>

### 🌟 DOM의 정의 🌟
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
