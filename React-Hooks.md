# React-Hooks

<br>

<h1> 1. useState</h1>

### 🌟 정의 🌟
<h4>
	
- useState는 리액트에서 제공하는 Hook 중 하나로, 함수 컴포넌트에서 상태(state)를 관리하는 데 사용된다.<br><br>
- 이 Hook을 사용하면 컴포넌트의 상태를 초기화하고 업데이트할 수 있다.<br><br>
- useState는 함수 컴포넌트에서 상태를 관리하는 간단하면서도 강력한 방법이다. 함수 컴포넌트에서 상태를 초기화하고 업데이트할 때 사용하며, 여러 개의 상태를 관리할 수 있다.
</h4>
<br>

### 🌈 예시 코드 🌈

```
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={increment}>Increment</button>
    </div>
  );
}

export default Counter;
```
### ⛅ 설명 ⛅
<h4>
	
1. useState 함수를 사용하여 상태를 초기화한다. 이 함수는 배열을 반환하며, 첫 번째 요소는 현재 상태의 값을 가지고 있고, 두 번째 요소는 상태를 업데이트하는 함수다. <br><br>위의 예시에서는 count라는 상태와 setCount라는 상태를 업데이트하는 함수를 생성한다. 초기값으로 0을 설정한다.<br>

2. increment 함수는 버튼 클릭 시 호출되는 함수로, setCount 함수를 사용하여 count 상태를 업데이트한다. 현재 count 값을 가져와서 1을 더한 후 새로운 상태로 설정한다.<br>

3. JSX 내부에서 {count}를 사용하여 현재 상태를 표시한다. 상태가 변경될 때마다 컴포넌트는 다시 렌더링되며, 업데이트된 상태를 화면에 반영한다.<br>

4. 버튼을 클릭하면 increment 함수가 호출되어 상태를 업데이트하고, 화면에 현재 카운트가 표시된다.<br>
</h4>
<br>
<br>

<h1> 2. useEffect</h1>

### 🌟 정의 🌟
<h4>
	
- useEffect는 리액트에서 제공하는 Hook 중 하나로, 함수 컴포넌트에서 부수 효과(side effects)를 수행하거나 컴포넌트 생명주기와 관련된 작업을 처리하는 데 사용된다.<br><br>
-  useEffect를 사용하면 컴포넌트가 렌더링될 때, 업데이트될 때, 혹은 언마운트될 때 원하는 작업을 실행할 수 있다.<br><br>

</h4>
<br>

### 🚀 기본 구조 🚀

```
import React, { useEffect } from 'react';

function MyComponent() {
  useEffect(() => {
    // 여기에 원하는 부수 효과 코드를 작성
  }, [/* 의존성 배열 */]);

  return (
    // 컴포넌트의 JSX 내용
  );
}

export default MyComponent;

```

### 🚢 기본 구조 설명 🚢
<h4>
- useEffect는 함수를 인자로 받는다. 이 함수는 컴포넌트가 렌더링될 때마다 실행되며, 기본적으로 컴포넌트가 렌더링될 때와 업데이트될 때마다 실행된다. <br><br>
- 하지만 두 번째 인자로 전달하는 배열인 "의존성 배열"을 통해 실행 조건을 세밀하게 제어할 수 있다. 의존성 배열에 포함된 값이 변경될 때만 useEffect 내의 함수가 실행된다.
</h4>
<br>

### ⛅ 설명 ⛅

<h4>
	
1. 데이터 가져오기 및 업데이트: API 요청과 같은 비동기 작업을 수행하거나, 상태가 변경될 때 데이터를 가져오거나 업데이트할 수 있다.<br>

2. 이벤트 리스너 등록 및 해제: 컴포넌트가 렌더링될 때 이벤트 리스너를 등록하고, 언마운트될 때 해당 이벤트 리스너를 해제할 수 있다.<br>

3. 외부 라이브러리 통합: 외부 라이브러리와의 통합 작업을 수행할 수 있다.<br>

4. 컴포넌트 생명주기 시뮬레이션: componentDidMount, componentDidUpdate, componentWillUnmount와 같은 생명주기 메서드와 유사한 작업을 수행할 수 있다.<br>
</h4>

<br>

### 🌈 예시 코드 🌈

```
import React, { useState, useEffect } from 'react';

function Timer() {
  const [seconds, setSeconds] = useState(0);

  // useEffect를 사용하여 타이머 업데이트
  useEffect(() => {
    const intervalId = setInterval(() => {
      setSeconds((prevSeconds) => prevSeconds + 1);
    }, 1000);

    // 컴포넌트가 언마운트될 때 타이머 해제
    return () => clearInterval(intervalId);
  }, []); // 빈 의존성 배열: 컴포넌트가 마운트될 때 한 번만 실행

  return (
    <div>
      <p>Elapsed Time: {seconds} seconds</p>
    </div>
  );
}

export default Timer;
```

<h1> 3. useRef</h1>

### 🌟 정의 🌟
<h4>
	
- useRef는 리액트에서 제공하는 Hook 중 하나로, DOM 요소에 직접 접근하거나 컴포넌트 내에서 변경되지 않는 값을 유지하는 데 사용된다.<br><br>
- useRef를 사용하면 DOM 요소를 선택하거나 컴포넌트 내에서 가변적인 값을 저장할 수 있다.<br><br>

</h4>
<br>

### 🚀 기본 구조 🚀

```
import React, { useRef } from 'react';

function MyComponent() {
  // useRef를 사용하여 변수를 생성
  const myRef = useRef(initialValue);

  return (
    // ...
  );
}

export default MyComponent;
```

### 🚢 기본 구조 설명 🚢
<h4>
	
- useRef를 사용할 때 초기값(initialValue)을 전달할 수 있으며, 이 값은 .current 속성을 통해 접근할 수 있다. .current는 useRef 객체의 현재 값을 나타낸다. <br><br>

</h4>
<br>

### 🌈 예시 코드 1. DOM 요소에 접근 🌈

```
import React, { useRef, useEffect } from 'react';

function AutoFocusInput() {
  const inputRef = useRef(null);

  useEffect(() => {
    // 컴포넌트가 마운트될 때 input 요소에 자동으로 포커스 설정
    inputRef.current.focus();
  }, []);

  return <input ref={inputRef} />;
}


export default Timer;
```
<h4> 
- useRef를 사용하여 DOM 요소에 직접 접근할 수 있다. 특히 포커스 설정, 스크롤 조작, 애니메이션 제어 등과 같은 작업에 유용하다.
</h4><br>

### 🌈 예시 코드 2. 가변 상태 유지 🌈 🌈

```
import React, { useRef, useEffect } from 'react';

function Timer() {
  const secondsRef = useRef(0);

  useEffect(() => {
    const intervalId = setInterval(() => {
      secondsRef.current += 1; // 컴포넌트 다시 렌더링되지 않음
      console.log(`Elapsed Time: ${secondsRef.current} seconds`);
    }, 1000);

    return () => clearInterval(intervalId);
  }, []);

  return (
    <div>
      <p>Elapsed Time: {secondsRef.current} seconds</p>
    </div>
  );
}
```
<h4>
- 컴포넌트의 렌더링과 무관하게 값을 유지할 수 있다. 이 값은 변경되어도 컴포넌트가 다시 렌더링되지 않는다.
</h4><br>

### 🌈 예시 코드 3. 이전 값 비교 🌈

```
import React, { useRef, useEffect } from 'react';

function MyComponent() {
  const prevValueRef = useRef(initialValue);

  useEffect(() => {
    // 이전 값과 현재 값을 비교
    if (prevValueRef.current !== value) {
      console.log('Value has changed:', value);
    }

    // 이전 값을 업데이트
    prevValueRef.current = value;
  }, [value]);

  return (
    // ...
  );
}

```
<h4> 
-이전 값과 현재 값을 비교할 수 있다. 이전 값과 현재 값을 비교하면서 특정 동작을 수행할 때 유용하다.
</h4><br>

</h4>

<br>


