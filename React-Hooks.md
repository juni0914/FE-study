# GNU 스포츠 시설 예약 및 커뮤니티 플랫폼

### 경상국립대학교 체육시설 예약과 커뮤니티 통합 웹 사이트 제작
<br>

### 팀프로젝트 공유 레포지토리 : https://github.com/GNU-SPORTS
<br>

## 🌟 목차 🌟
- 기술스택
- 프론트엔드 개발 세부 내용
- 실행화면
<br>

## 📚 Tech Stack 📚
<br>
<div align=center>
	<h4>✨ Front-End ✨</h4>
</div>
<div align="center">
	<img src="https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB"/>
	<img src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E"/>
	<img src="https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white"/>
	<img src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white"/>
	<img src="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white"/>
	<br>
</div>
<br>
<br>

<div align=center>
	<h4>🚀 Distribute 🚀</h4>
</div>
<div align=center>
	<img src="https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white"/>
</div>
<br>

<div align=center>
	<h4>🛠 Environment 🛠</h4>
</div>
<div align=center>
	<img src="https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white"/>
	<img src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white"/>
	<img src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white"/>
</div>
<br>
<br>

## 🌈 Front-End Development Content 🌈
<br>
<h3>🌷 클라이언트 서버 배포 🌷</h3>
<h4>- AWS EC2 인스턴스 서비스를 이용하여 클라이언트 서버를 배포하였습니다.</h4>
👉 추가로 pm2를 이용하여 인스턴스가 꺼지지 않는 한 배포가 중단되지 않도록 서버를 구동하였습니다.
<br>
<br>

<br>
<br>
<h2>- 함수형 컴포넌트를 사용하여 </h2>
<h4> 1) 컴포넌트 간에 상태나 로직을 쉽게 공유하고 예약과 커뮤니티 기능을 구현할 때 같은 코드가
중복되지 않도록 재사용성을 확보하였습니다.<br><br>
2) 코드를 간결하고 직관적이고 가독성이 좋게끔 작성하였고, 불필요한 생명주기 메서드나 복잡한 클래스 구조를 사용하지 않았습니다.<br><br>
3) 효과적인 상태 관리와 라이프사이클 처리를 하였습니다.<br><br>
4) 렌더링 성능을 최적화하기 위해 최적화된 Hooks를 활용하여 불필요한 side effect를 방지하였습니다.<br><br></h4>


<h2>- React Hooks를 사용하여</h2>
<h3>1) useEffect</h3> 
<h4>- 렌더링 시 발생하는 side effect를 방지하였습니다.  <br><br>
- 데이터 가져오기, API 호출 등의 비동기 작업을 useEffect 내에서 처리하였습니다. <br><br>
- 또한, 메모리 누수를 방지하고 리소스를 효과적으로 관리하였습니다.</h4><br>
<h3>2) useState</h3>
<h4>- 간단하고 직관적인 상태 관리를 하였습니다. <br><br>
- 또한, 리액트의 렌더링 메커니즘을 활용하여 필요한 상태만 업데이트하여 불필요한 렌더링을 최소화하였습니다.</h4>
<br><br>

<h2>- React Router를 사용하여</h2>
<h4>
▪ Routes와 Route 컴포넌트를 사용하여 리액트 애플리케이션의 라우팅을 관리하였습니다.<br><br>
▪  애플리케이션의 페이지 간 전환을 관리하고, 각 경로에 맞는 컴포넌트를 렌더링하였습니다.<br><br>
▪ JSX 파일을 사용하여  가독성과 유지보수성을 높이고, 모듈화된 개발과 문법을 간소화하였습니다.<br><br>
▪ 사용자 상호작용에 따라 다양한 상태에 맞게 화면을 구성하고, 동적인 UI를 구현하기 위해 조건부 렌더링을 적극 활용하였습니다.<br><br>
</h4>

<br>
<h3> 🗺 서비스의 지도는 네이버 맵 API(react-naver-maps)를 활용하였습니다.</h3>
<br>
<h3> 🔑 사용자의 비밀번호는 JWT토큰(jsonwebtoken)을 사용하여 암호화하였습니다.</h3>
<br>
<h2>🎨  Style</h2>
<h4> 
- 스타일링은 react-bootstrap, JSX 내부 스타일링과 기본 CSS를 사용하였습니다.<br><br>
- 획일화된 디자인을 추구하였으며, 모바일 및 태블릿 환경에서의 사용성을 고려하기 위하여 반응형 웹 디자인을 적용하였습니다.
</h4>
<br>
