# 타입스크립트 학습 정리

<br>

![image](https://github.com/juni0914/FE-study/assets/100837725/4c3624af-800e-4f69-8906-16208a21f4d6)

<br><br>
## 🌟 정의 🌟
<h4>
	
- 타입스크립트는 자바스크립트의 기본적인 틀을 가져가되, 거기에 타입 지정이라는 옵션을 얹은 것이라고 생각하면 된다.<br><br><br>

- 초창기의 웹페이지는 지금의 웹페이지처럼 사용자와 인터랙티브한 기능이 많지 않았고,<br><br> 도서관에서 책을 꺼내보듯이 인터넷 생태계에 많은 양의 정보를 저장해두고 꺼내보는 형식이었다.<br><br>
그래서 자바스크립트는 견고한 구조를 짜기보다는 빠르게 어떤 기능을 만들기 위해 개발된 언어였다.<br><br><br>

- 그러나 복잡한 웹앱들이 등장하고 프론트 쪽에서 할 일이 많아짐에 따라 견고한 프로그램이 만들어질 필요성이 요구되자<br><br>
다른 정적 타입 언어들처럼 자바스크립트에도 견고하게 만들 수 있는 언어의 기능이 필요해졌다. <br><br>
- 그래서 등장한 것이 타입스크립트이다. <br><br><br>

![image](https://github.com/juni0914/FE-study/assets/100837725/9b6c2f3a-9642-4425-9b9a-347b3baff1be)
<br><br>

- 자바스크립트와 타입스크립트의 가장 큰 차이점은 타입을 지정 여부 말고도 한 가지가 더 있다.<br><br>
바로 자바스크립트는 인터프리터 언어이고, 타입스크립트는 컴파일 언어라는 것이다. <br><br>
- 인터프리터 언어는 웹 브라우저 혹은 런타임 환경에서 코드를 한 줄 한 줄 읽어내려가 해석하도록 만들어진 언어고, <br><br>
컴파일 언어는 컴파일링(컴퓨터가 해석할 수 있는 언어로 변환하는 작업) 과정을 거쳐서 실행되어지는 언어다.<br><br>

- 타입스크립트는 결국 컴파일링을 거쳐 자바스크립트로 변환된다. 
</h4>
<br>

## 🌈 타입스크립트를 사용해야 하는 이유 🌈

<h3> 1. 버그 예방</h3>
<h4>
  
- 자바스크립트의 버그 중 15%를 타입스크립트의 사용으로 미리 예방할 수 있다는 연구가 있다고 한다. <br><br>
- 자바스크립트는 선언할 때 타입을 지정해주지 않기 때문에 동작하면서 언제 나도 모르게 형변환이 되어 있을 수도 있고,<br><br>
  그런 부분으로 인해 예기치 않은 버그가 발생할 수도 있다. 심지어 인터프립터 언어 특성상 그런 버그들을 찾는 것 조차 쉽지 않다. <br><br>
  컴파일 과정이 없기 때문에 에러를 출력하지 않고 실행되기 때문이다. <br><br>
-  타입스크립트를 사용한다고해서 모든 버그를 완전히 막을 수 있는 것은 아니지만 적어도 컴파일단계에서 타입관련 에러는 막을 수 있다. <br><br>
  예를 들어, strictNullCheck 옵션을 true로 해놨다면 객체/null/undefined가 할당될 수 있는 변수가 있을 때, <br><br>null이나 undefined가 아닌지 체크하지 않고서는 객체의 속성을 가져올 수 없다.
  
</h4>
<h3> 2. 더 나은 개발자 경험과 코드 퀄리티 향상</h3>
<h4>
  
- 자바스크립트로 코드를 작성할 때, 객체의 필드나 함수의 매개변수로 들어오는 값이 무엇인지 알기 위해<br><br> 여러 파일들을 살펴봐야했던 경험이 있을 것이다.<br><br>
- 하지만 타입스크립트를 제대로 사용함으로써 얻을 수 있는 가장 큰 장점 중 하나는 변수의 이름뿐만 아니라<br><br> 그 데이터의 "type"까지 알 수 있게 해준다는 것이다.<br><br>
그래서 코드 작성이 좀 더 쉽고 직관적이게 만들어준다. 개발자는 로직과 같은 큰 구조들에만 집중할 수 있게 해주는 것이다. <br><br>
- 또한 오브젝트 안의 속성값을 하나하나 기억할 필요없이 IDE가 자동으로 리스트업 해주기 때문에 개발자 입장에서는 훨신 편해진다.  <br><br>
  
</h4>

<h3> 3. 크로스브라우징(브라우저 호환성) 해결</h3>
<h4>
  
- 모든 브라우저의 지원을 걱정해야하는 프론트개발자 입장에서는 ES6+을 써도 될지 고민이 많을 것이다. <br><br>
- 하지만 타입스크립트는 컴파일 과정에서 ES6+ 문법들을 ES5(또는 ES3)로 바꿔주기 때문에<br><br> Babel의 도움 없이 크로스브라우징 문제를 해결할 수 있다. <br><br>
</h4>

<br>
<br>

## ⚡ 기본 타입 ⚡

<h3> 1. 문자열</h3>
<h4>
	
```
let car : string = 'string';
```
</h4>
<h3> 2. 숫자</h3>
<h4>
	
```
let age : number = 25;
```
</h4>
<h3> 3. boolean</h3>
<h4>
	
```
let isAdult : boolean = true;
```
</h4>
<h3> 4. 숫자 배열</h3>
<h4>
	
```
let num : number[] = [1,2,3];
let num : Array<number> = [1,2,3];
```
</h4>
<h3> 4. 문자열 배열</h3>
<h4>
	
```
let week : string[] = ['mon','tue','wed'];
let num : Array<string> = ['mon','tue','wed'];
```
</h4>
<h3> 5. 튜플</h3>
<h4>
	
```
let tup : [string, number];
```
</h4>
<h3> 6. void, never</h3>
<h4>
	
```
function sayHello() : void{
	console.log('Hello');
}

function showError() : never{
	throw new Error();
}

function infLoop() : never{
	while(true){
		
	}
}
```
</h4>
<h3> 7. enum</h3>
<h4>
	
```
enum OS {
	Window,		// 0
	Ios,		// 1
	Android		// 2
}
```
</h4>
<h3> 8. null, undefined</h3>
<h4>
	
```
let a : null = null;
let b : undefined = undefined;
```
</h4>

## 🍀 인터페이스 🍀
<h3> 1. 형식</h3>
<h4>
	
```
type Score = 'A' | 'B' | 'C' | 'F';

interface User{
	name : string;
	age : number;
	gender? : string;			// 옵셔널 부분이라 있어도 되고 없어도 됨. 다만, 있으면 string으로
	readonly birthYear : number;		// 읽기 전용이기에 수정은 불가능
	[grade:number] : Score;			// 지정한 타입만 사용이 가능
}

let user : User = {
	name : 'lee',
	age : 25,
	birthYear : 1999,
	1 : 'A',
	2 : 'B'
}
```
</h4>
<h3> 2. 인터페이스 함수</h3>
<h4>
	
```
interface Add {
	(num1 : number, num2 : number) : number;
}

const add : Add = function(x,y) {
	return x + y;
}

add(10, 20);		// 30

interface IsAdult {
	(age : number) : boolean;
}

const a : IsAdult = (age) => {
	return age > 19;
}

a(25)		// true
```
</h4>
<h3> 3. 인터페이스 클래스</h3>
<h4>
	
```
interface Car {
	color : string;
	wheels : number;
	start() : void;
}

class Benz implements Car {
	color = 'red';
	wheels = 4;
	start(){
		console.log('go....');
	}
}
```
</h4>

## ⭐ 함수 ⭐
<h3> 1. 형식</h3>
<h4>
	
```
function hello(name: string, age?: number): string {
	if(age !== undefined) {
		return `Hello, ${name}. You are ${age}.`;
	}else{
		return `Hello, ${name}`;
	}
}

console.log(hello("Sam"));
console.log(hello("Sam",25));
```
</h4>

<h3> 2. 나머지 매개변수</h3>
<h4>
	
```
function add(...nums: number[]) {
	return nums.reduce((result, num) => result + num, 0);
}

add(1,2,3);
add(1,2,3,4,5,6,7,8,9,10);
```
</h4>

<h3> 3. this 함수</h3>
<h4>
	
```
interface User {
	name: string;
}

const Sam: User = {name: 'Sam'}

function showName(this:User, age:number, gender:'m'|'f'){
	console.log(this.name, age, gender)
}

const a = showName.bind(Sam);
a(30,'m');
```
</h4>

<h3> 4. 함수 오버로드</h3>
<h4>
	
```
interface User {
	name: string;
	age: number;
}

function join(name: string, age: string): string;
function join(name: string, age: number): User;
function join(name: string, age: number | string): User | string {
	if(typeof age === "number"){
		return{
			name,
			age,
		};
	}else{
		return "나이는 숫자로 입력하세요";
	}
}

const sam: User = join("Sam", 30);
const jane: string = join("jane", "30");
```
</h4>

## 🌙 리터럴, 유니온 / 교차 타입 🌙
<h3> 1. 리터럴</h3>

<h4>	
	
```
const userName1 = "Bob";
let userName2 : string | number = "Tom";

type Job = "police" | "developer" | "teacher";

interface User {
	name : string;
 	job : Job;
}

const user : User = {
	name : "Bob",
 	job : "developer"
}
```

</h4>
<h3> 2. 유니온</h3>
<h4>
	
```
interface Car {
	name: "car";
 	color: string;
  	start(): void;
}

interface Mobile {
	name: "mobile";
 	color: string;
  	call(): void;
}

function getGift(gift: Car | Mobile) {		// 식별 가능한 유니온 타입
	console.log(gift.color);
 	if(gift.name === "car"){
		gift.start();
  	}else{
		gift.call();
    	}
}
```

</h4>
<h3> 3. 교차 타입</h3>
<h4>
	
```
interface Car {
	name: string;
  	start(): void;
}

interface Toy {
	name: string;
 	color: string;
	price: number;
}

const toyCar: Toy & Car = {
	name : "타요",
 	start(){},
  	color: "blue",
   	price: 1000
}
```
</h4>

## 🌷 제네릭 🌷
<h3> 1. 일반적인 제네릭</h3>

<h4>	
	
```
function getSize<T>(arr: T[]) : number {
	return arr.length;
}

const arr1 = [1,2,3];
getSize(arr1); 		//3

const arr2 = ["a","b","c"];
getSize(arr2); 		//3

const arr3 = [false, true, true];
getSize(arr3); 		//3

```

</h4>
<h3> 2. 인터페이스에서의 제네릭</h3>
<h4>
	
```
interface Mobile {
	name: string;
 	price: number;
  	option: any;
}

interface Mobile<T> {
	name: "mobile";
 	color: string;
  	call(): void;
}

const m1: Mobile<{color: string, coupon: boolean}> = {
	name: "s22",
	price: 1000,
	option: {
		color: "red",
		coupon: false,
	}
}

const m2: Mobile<string> = {
	name: "s22",
	price: 1000,
	option: "good"
}

```

</h4>
<h3> 3. 제네릭 + 함수</h3>
<h4>
	
```
interface User {
	name: string;
  	age: number;
}

interface Car {
	name: string;
  	color: string;
}

interface Book {
	price: number;
}

const user: User = { name: "a", age: 10 };
const car: Car = { name: "benz", color: "red"};
const book: Book = { price: 3000 };

function showName<T extends { name: string}>(data:T): string {
	return data.name;
}

showName(user);
showName(car);
showName(book); 	// error

```
</h4>

## 🚀 유틸리티 타입 🚀
<h3> 1. keyof</h3>

<h4>	
	
```
interface User {
	id: number;
	name: string;
	age: number;
	gender: "m" | "f";
}

type UserKey = keyof User; 	// 'id' | 'name' | 'age' | 'gender'

const uk:UserKey = "age";
```

</h4>
<h3> 2. Partial<T></h3>
<h4>
	
```
interface User {
	id: number;
	name: string;
	age: number;
	gender: "m" | "f";
}

let admin: Partial<User> = {
	id: 1,
	name: "Bob"
};

```

</h4>
<h3> 3. Required<T></h3>
<h4>
	
```
interface User {
	id: number;
	name: string;
	age?: number;
}

let admin: Required<User> = {
	id: 1,
	name: "Bob",
	age: 30, 	// 모든 속성이 필수가 되어서 age속성이 필요함
};

```
</h4>

<h3> 4. Readonly<T></h3>
<h4>
	
```
interface User {
	id: number;
	name: string;
	age?: number;
}

let admin: Readonly<User> = {
	id: 1,
	name: "Bob",
};

admin.id = 4;	// error

```
</h4>

<h3> 5. Record<K,T></h3>
<h4>
	
```
interface User {
	id: number;
	name: string;
	age: number;
}

function isValid(user: User) {
	const result: Record<keyof User, boolean> = {
		id: user.id > 0,
		name: user.name !== "",
		age: user.age > 0,
	};
	return result;
}

```
</h4>
<h3> 6. Pick<K,T></h3>
<h4>
	
```
interface User {
	id: number;
	name: string;
	age: number;
	gender: "M" | "W";
}

const admin: Pick<User, "id" | "name"> = {
	id: 0,
	name: "Bob"
}

```
</h4>

<h3> 7. Omit<K,T></h3>
<h4>
	
```
interface User {
	id: number;
	name: string;
	age: number;
	gender: "M" | "W";
}

const admin: Omit<User, "age" | "gender"> = {
	id: 0,
	name: "Bob"
}

```
</h4>
<h3> 8. Exclude<T1, T2></h3>
<h4>
	
```
type T1 = string | number | boolean;
type T2 = Exclude<T1, number | string>;		// boolean만 남게 됨.

```
</h4>
<h3> 9. NonNullable<Type></h3>
<h4>
	
```
type T1 = string | null | undefined | void;
type T2 = NonNullable<T1>;		// string과 void만 남게 됨.

```
</h4>
