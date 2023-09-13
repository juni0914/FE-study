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
<h1> 4. useContext</h1>

### 🌟 정의 🌟
<h4>
	
- useContext는 React의 훅 중 하나로, React 컴포넌트 간에 상태나 데이터를 공유하기 위해 사용된다.<br><br>
- 이를 통해 상태를 props를 통해 일일이 전달하지 않고, 컴포넌트 트리에서 필요한 곳에서 데이터를 직접 사용할 수 있다.<br><br>

</h4>
<br>

### 🌈 예시 코드 🌈

```
import React, { useContext, createContext } from 'react';

// 데이터를 저장할 컨텍스트를 생성
const MyContext = createContext();

// 컨텍스트 프로바이더를 제공하는 상위 컴포넌트
function MyProvider({ children }) {
  const sharedData = 'This is shared data from context';

  return (
    <MyContext.Provider value={sharedData}>
      {children}
    </MyContext.Provider>
  );
}

// 하위 컴포넌트에서 컨텍스트 사용
function ChildComponent() {
  // useContext를 사용하여 컨텍스트 데이터에 접근
  const dataFromContext = useContext(MyContext);

  return <div>{dataFromContext}</div>;
}

function App() {
  return (
    <MyProvider>
      <ChildComponent />
    </MyProvider>
  );
}

export default App;

```
### ⛅ 설명 ⛅
<h4>
	
1. createContext: createContext 함수로 컨텍스트를 생성한다. 이 함수는 컨텍스트 객체와 Provider 컴포넌트를 반환한다.<br>

2. MyProvider: 상위 컴포넌트인 MyProvider는 MyContext.Provider 컴포넌트로 컨텍스트를 제공한다. value prop을 사용하여 컨텍스트에 공유할 데이터를 설정합니다. 이 컨텍스트는 자식 컴포넌트에서 사용할 수 있도록 한다.<br>

3. ChildComponent: useContext 훅을 사용하여 컨텍스트 데이터에 접근한다. 이 컴포넌트는 컨텍스트에서 제공하는 데이터를 사용하여 UI를 렌더링한다.<br>

4. App: 최상위 컴포넌트인 App은 MyProvider로 감싸져 있으며, 이 하위에 있는 ChildComponent에서 컨텍스트 데이터를 사용할 수 있도록 한다.<br>
</h4>
<br>
<br>
<h1> 5. useMemo</h1>

### 🌟 정의 🌟
<h4>
	
- useMemo는 리액트 훅 중 하나로, 계산 비용이 높은 함수의 결과 값을 캐시하고, 의존성 배열에 지정된 값들이 변경될 때만 다시 계산하여 성능을 최적화하는 데 사용된다.<br><br>

</h4>
<br>

### 🌈 예시 코드 🌈

```
function expensiveAdd(a, b) {
  console.log('Adding numbers...');
  return a + b;
}

```
<h4>이 함수를 useMemo를 사용하여 호출하면, 함수의 결과가 이전과 동일한 경우에는 이전 결과를 재사용하고, 의존성 배열에 지정된 값이 변경될 때만 함수를 다시 계산한다.</h4>

```
import React, { useMemo, useState } from 'react';

function MyComponent() {
  const [x, setX] = useState(0);
  const [y, setY] = useState(0);

  const result = useMemo(() => {
    return expensiveAdd(x, y);
  }, [x, y]);

  return (
    <div>
      <p>X: {x}</p>
      <p>Y: {y}</p>
      <p>Result: {result}</p>
      <button onClick={() => setX(x + 1)}>Increment X</button>
      <button onClick={() => setY(y + 1)}>Increment Y</button>
    </div>
  );
}

export default MyComponent;


```
### ⛅ 설명 ⛅
<h4>
	
1. 위의 코드에서 useMemo를 사용하여 expensiveAdd 함수를 호출하고 있습니다. 이 함수는 x와 y라는 두 개의 상태값을 의존성 배열로 갖고 있으며, 즉 x 또는 y가 변경될 때만 expensiveAdd 함수를 다시 호출하게 된다.

2. 이렇게 함으로써, expensiveAdd 함수가 호출되는 횟수를 최적화할 수 있으며, 렌더링 성능을 향상시킬 수 있다. 그리고 화면에 렌더링되는 결과 역시 캐시된 값인 result를 보여주게 된다.<br>

</h4>
<br>
<br>
<h1> 6. useCallback</h1>

### 🌟 정의 🌟
<h4>
	
- useCallback은 리액트 훅 중 하나로, 함수를 메모이제이션하고 해당 함수의 의존성 배열에 지정된 값이 변경될 때만 새로운 함수를 생성한다. 주로 렌더링 성능 최적화를 위해 사용된다.<br><br>

- 일반적으로 함수 컴포넌트 내에서 함수를 정의하면, 해당 함수는 컴포넌트가 리렌더링될 때마다 새로 생성된다. 이는 불필요한 함수 생성과 메모리 낭비를 초래할 수 있다. 이런 경우 useCallback을 사용하여 함수를 메모이제이션하면, 의존성 배열의 값이 변경될 때만 함수가 재생성되어 성능을 향상시킬 수 있다.<br><br>

</h4>
<br>

### 🌈 예시 코드 🌈

```
import React, { useState, useCallback } from 'react';

function MyComponent() {
  const [count, setCount] = useState(0);

  // handleClick 함수를 메모이제이션
  const handleClick = useCallback(() => {
    setCount(count + 1);
  }, [count]); // count가 변경될 때만 handleClick 함수 재생성

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleClick}>Increment Count</button>
    </div>
  );
}

export default MyComponent;

```

### ⛅ 설명 ⛅
<h4>
	
1. 위의 코드에서 handleClick 함수는 useCallback을 사용하여 정의되었다. 함수 내에서 count 상태값을 의존성 배열로 지정하였으므로, count 값이 변경될 때만 handleClick 함수가 재생성된다.

2. 이렇게 하면 컴포넌트가 리렌더링되더라도 함수가 새로 생성되지 않고, 성능 최적화를 할 수 있다. 특히 콜백 함수를 자식 컴포넌트에 props로 전달할 때 유용하게 사용된다.<br>

</h4>
<br>
<br>
<h1> 7. useReducer</h1>

### 🌟 정의 🌟
<h4>
	
- useReducer는 상태 관리를 위한 훅(Hook) 중 하나로, 컴포넌트 내에서 복잡한 상태 관리 로직을 다루는 데 도움을 주는 기능이다.<br><br>

- 주로 컴포넌트의 상태를 변경하고 업데이트하는 로직을 분리하여 관리할 때 사용된다.<br><br>

- useState와 함께 사용되지만, useReducer는 더 복잡한 상태 관리 시나리오에서 더 강력하고 유용하다.<br><br>

🌟 useReducer의 핵심 개념은 "액션(Action)"과 "리듀서(Reducer)"다.<br><br>

 

⭐ 액션(Action)
- 액션은 상태를 변경하기 위해 발생하는 이벤트나 작업을 나타내는 객체다.

- 주로 객체 안에 type 프로퍼티와 추가 데이터를 포함하고, 이 객체를 이용하여 상태 변경의 의도를 표현한다.<br><br>

 

 


⚡리듀서(Reducer)
- 리듀서는 현재 상태와 액션을 받아서 새로운 상태를 반환하는 순수 함수다.

- 이 함수는 이전 상태를 변경하지 않고, 주어진 액션에 따라 새로운 상태를 생성하여 반환한다.

- 리듀서 함수는 useReducer 훅 안에서 정의되며, 상태 변경 로직을 담당한다.<br><br>

🌈 기본 구조

```
const [state, dispatch] = useReducer(reducer, initialState);
```
- state: 현재 상태를 나타내는 변수
- dispatch: 액션을 발생시키는 함수다. 이 함수를 호출하면 리듀서가 실행되고, 새로운 상태가 반환된다.
- reducer: 상태를 변경하는 로직을 정의한 함수
- initialState: 초기 상태를 나타내는 값
</h4>
<br>

### 🌈 예시 코드(1) 🌈

```
import React, { useState, useReducer } from 'react';

const ACTION_TYPES = {
  deposit: 'deposit',
  withdraw: 'withdraw' 
};

const reducer = (state, action) => {
  switch (action.type){
    case ACTION_TYPES.deposit:
      return state + action.payload;
    case ACTION_TYPES.withdraw:
      return state - action.payload;
    default:
      return state;
  }
};

function App() {
  const [number, setNumber] = useState(0);
  const [money, dispatch] = useReducer(reducer, 0);

  return (
    <div>
      <h2>잔고 : {money} 원</h2>
      <input
        type="number"
        value={number}
        onChange={(e)=> setNumber(parseInt(e.target.value))}
        step="10000"
      />
      <button
        onClick={()=> dispatch({type: ACTION_TYPES.deposit, payload: number})}>예금</button>
      <button
        onClick={()=> dispatch({type: ACTION_TYPES.withdraw, payload: number})}>출금</button>
    </div>
  );
}

export default App;
```
### 🌈 예시 코드(2) 🌈

```
//Student.js

import React from 'react'

const Student = ({name, dispatch, id, isHere}) => {
  return (
    <div>
    <span style={{
        textDecoration: isHere ? 'line-through' : 'none',
        color: isHere ? 'gray' : 'black'
    }}
    onClick={()=>{
        dispatch({type: 'mark-student', payload: {id}})
    }}>{name}</span>
    <button onClick={()=>{
        dispatch({type:'delete-student', payload: {id}})
    }}>삭제</button>
    </div>
  )
}

export default Student
```

```
//App.js

import React, { useState, useReducer } from 'react';
import Student from './Student';

const ACTION_TYPES = {
  addstudent: 'add-student',
  deletestudent: 'delete-student',
  markstudent: 'mark-student'
}

const reducer = (state, action) => {
  switch (action.type){
    case ACTION_TYPES.addstudent:
      const name = action.payload.name;
      const newStudent = {
        id: Date.now(),
        name: name,
        isHere: false
      };
      return{
        count: state.count + 1,
        students: [...state.students, newStudent]
      };
    case ACTION_TYPES.deletestudent:
      return{
        count: state.count - 1,
        students: state.students.filter((student) => student.id !== action.payload.id)
      };
    case ACTION_TYPES.markstudent:
      return{
        count: state.count,
        students: state.students.map((student)=>{
          if(student.id === action.payload.id){
            return {...student, isHere: !student.isHere}
          }
          return student;
        })
      }
    default:
      return state;
  }
};

const initialState = {
  count: 0,
  students: []
}

function App() {
  const [name, setName] = useState('');
  const [studentsInfo, dispatch] = useReducer(reducer, initialState);

  return (
    <div>
      <h2>출석부</h2>
      <p>총 학생 수 : {studentsInfo.count}</p>
      <input
        type="text"
        value={name}
        onChange={(e)=> setName(e.target.value)}
      />
      <button onClick={()=>{
        dispatch({type: ACTION_TYPES.addstudent, payload: {name}});
        setName('');
      }}>추가</button>
      {studentsInfo.students.map((student) =>{
        return <Student 
          key={student.id} 
          name={student.name} 
          dispatch={dispatch} 
          id={student.id}
          isHere={student.isHere}
        />
      })}
    </div>
  );
}

export default App;
```

### ⛅ 설명 ⛅
<h4>
	
🔥 장점
- useReducer를 사용하면 컴포넌트 내에서 복잡한 상태 로직을 더 간결하게 관리할 수 있으며, 상태 관리 코드를 컴포넌트 외부로 분리하여 재사용성을 높일 수 있다. 

 
-  특히 상태 관리 로직이 복잡한 컴포넌트나 다수의 컴포넌트가 동일한 상태를 공유해야 하는 경우에 유용하다.


👉

- 하지만 간단한 state를 관리할 경우에는 그냥 간단하게 useState를 사용하는 것이 낫다.

- 예를 들면 모달 창이 열리고 닫히는 경우.

</h4>


