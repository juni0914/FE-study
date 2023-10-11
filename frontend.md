# Front-End CS

<br>

<h1> 1. Promise</h1>

### 🌟 정의 🌟
<h4>
	
- Promise 객체는 JavaScript에서 비동기 작업을 처리하기 위한 내장 객체로, 비동기 작업의 완료 여부와 결과를 나타내는 객체다. <br><br>

1. 대기(Pending): 초기 상태로, 작업이 완료되지 않았을 때의 상태다.<br><br>

2. 이행(Fulfilled): 비동기 작업이 성공적으로 완료되었을 때의 상태다. 이때 Promise가 성공 상태로 전환되며 작업의 결과를 가지고 있다.<br><br>

3. 거부(Rejected): 비동기 작업이 실패했을 때의 상태다. Promise가 실패 상태로 전환되며 에러 정보를 가지고 있다.<br><br>
</h4>
<br>

### 🌈 예시 코드 🌈

```
// Promise를 생성합니다.
const myPromise = new Promise((resolve, reject) => {
  // 비동기 작업을 수행합니다. (예: 네트워크 요청)
  const success = true; // 비동기 작업의 결과 (성공 여부)

  if (success) {
    // 작업이 성공한 경우
    resolve("성공했습니다."); // resolve 함수를 호출하여 Promise를 이행합니다.
  } else {
    // 작업이 실패한 경우
    reject("실패했습니다."); // reject 함수를 호출하여 Promise를 거부합니다.
  }
});

// Promise를 사용합니다.
myPromise
  .then((result) => {
    console.log("성공:", result); // 작업이 성공한 경우
  })
  .catch((error) => {
    console.error("실패:", error); // 작업이 실패한 경우
  });

```
### ⛅ 설명 ⛅
<h4>
	
1. Promise 객체는 new Promise()를 사용하여 생성된다. 이 객체는 콜백 함수를 인자로 받으며, 비동기 작업을 수행하고 결과를 resolve 또는 reject 함수를 호출하여 처리한다.<br><br>
2. then 메서드는 Promise가 성공적으로 완료됐을 때 실행할 콜백 함수를 등록한다.<br><br>
3. catch 메서드는 Promise가 거부됐을 때 실행할 콜백 함수를 등록한다.<br><br><br><br>

🔥 Promise를 사용하면 비동기 작업을 보다 효율적으로 처리하고, 더 직관적으로 코드를 작성할 수 있다. <br><br>이를 통해 콜백 지옥과 같은 문제를 해결하고 코드를 더 읽기 쉽게 만들 수 있다.
</h4>
<br>
<br>
