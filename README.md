This is my first JS Project! So Excited~! 

1. `Basic Information`   
	자바스크립트는 브라우저에 내장되어있다!   
	Browser는 HTML을 불러오고 HTML은 CSS와 JS를 불러온다   
	HTML이 접착제 느낌

	* always const, sometimes let, never var  
	boolean -> true, false  ( 1, 0 )  
	null -> 아무것도 아닌 값이 채워져 있다.  
	undefined -> 변수는 정의 되어있지만 값이 정의되지 않았다.  
	NaN -> Not A Number  

	* const days [ ] -> array(list) 만들기  
	array.push() -> 배열에 데이터를 추가할 수 있다.

	* const player {} -> object 만들기  
	안에 항목들을 property라고한다.  
	const로 객체를 만들더라도 그 안의 property를 변경시킬 수 있다.  
	그러나 const 객체 자체를 바꾸는 것(boolean타입이라던가, int 타입이라던가)
	은 불가능하다.

	* function 함수이름(파라미터(그냥 변수 이름만)) { 원하는 기능 }  
	ex) function sayHello(name) {  
	&nbsp;	console.log("Hello! " + name);  
	}
	
	* 함수에서 값을 리턴 받을 수도 있다.  
	ex) function add(a, b) {  
	&nbsp;	return a + b;  
	}  
	return이 되는 순간 함수는 종료된다.

	* object안에 function 넣기  
	ex) const player = {  
	&nbsp;	name: "keunoh",  
	&nbsp;	sayHello: function () {  
	&nbsp;&nbsp;		console.log("Hello!");  
    &nbsp;	}  
	};

2. `JavaScript와 document`   
	f12에서 document(해당 페이지의 html의미)를 입력하면 html객체를 볼 수 있다.  

	* console.dir(document) 하면 객체를 좀더 상세히 볼 수 있다.  
	자바스크립트에서 html에 접근할 수 있는 방법  
	자바스크립트 관점에서 html객체를 바라보는 것이다.  
	
	* 해당 객체의 property에 값을 arrangement 할 수도 있다!!  
	ex) document.title = 'Hello from console' <- 웹페이지 탭 이름 변함   
	* document.location <- html path 알 수 있다.  
	
	* document.body <-  body부분 확인할 수 있다.  
	
	* document.getElementById("") <- 괄호안에 입력한 element id구간을 가져온	다.  
	
	* document.getElementsByClassName("") <- 클래스 네임으로 여러개 가져옴  
	
	* document.getElementsByTagName("h1") <- 태그네임으로 가져옴  
  
	* 노마드가 좋아하는 방법  
	ex) document.querySelector(".hello h1") -> className hello이고 h1가져옴
	querySelector는 element를 css방식으로 검색할 수 있다. 
	클래스 이름이 중복되는 경우 가장 첫 번째 element가져온다.

3. `결국 html에서 css와 js를 import하는 것이다!(* 매우 중요)`

4. `h1과 같은 element 메서드`  
	* h1.classList.contains("") -> 괄호 안에 해당 className이 있다면 true반환

	* h1.classList.remove("") -> 해당 className을 삭제

	* h1.classList.add("") -> 해당 className을 추가

	* h1.classList.toggle("") -> classList를 확인해서 클래스가 없으면 추가해주고 있다면 삭제한다.

5. `submit은 기본적으로 브라우저를 새로고침한다.`
	* function 안에 tomato.preventDefault();를 적어주면 새로고침을 막아준다.
	
	* addEventListener("submit", myFunction); <- 이 라인에서 myFunction에
	있는 parameter에 아무 변수명이나 적어준다음 
	
	* ex) console.log(tomato)를 하면 해당 function에 정보를 참조 할 수 있다.


6. `브라우저가 event를 대신 실행시켜준다. (* 중요)`
	* addEventListener에서 브라우저가 함수를 대신 실행시켜주는 것이다.

7. `방법(JS에서 innerText)`
	* 둘 다 같은 방법이지만 아래를 선호한다.
	
	* greeting.innerText = "Hello " + username;
    	greeting.innerText = `Hello ${username}`;
	
	* `` <- backticks

8. `interval` 
	* 매 순간 일어나야 하는 무언가
	
	* ex) setInterval(sayHello, 5000); -> sayHello함수를 5초마다 실행함.
	
	* setTimeout(sayHello, 5000); -> 5초 후에 단 한번만 함수 실행

9. `포맷`
	* '1'.padStart(2, '0'); -> 2문자의 길이이고, 해당 문자가 1자리이면 0을채워준다.
	
	* "hello".padStart(20, "x");
	
	* String(new Date().getHours()) -> number를 string으로 변환

10. `JS 함수`
	* Math.random() -> 0부터 1까지 실수를 랜덤하게 표현해줌
	* Math.round() -> 해당 실수를 반올림해준다.
	* Math.ceil() -> 실수를 올림
	* Math.floor() -> 실수를 내림

	* document.createElement("img") -> img태그를 생성해준다.
	* bgImage.src = `img/${chosenImage}`; -> 이미지 경로 설정해준다.
	* document.body.appendChild(bgImage); -> body에 해당 이미지 생성해서 추	가 해준다.
	* prependChild로 해주면 맨 위에 삽입할 수도 있다.

11. `TODOLIST Concept`
	1. toDoInput.value -> 사용자가 입력한 todolist의 value를 저장한다.
	
	2. span.innerText = newTodo -> 해당 value를 생성한 span element에 넣어	준다.
	동시에 삭제 버튼(X)도 생성시킨다. 

	3. event.target -> 어떤 버튼이 실행되었는가?  
	event.target.parentElement -> 해당 버튼의 부모 element는 무엇인가?  
	li.remove(); -> 해당 x버튼이 눌린 todolist를 삭제한다.

12. `JSON`
	* JSON.stringify() -> 괄호 안에 어떤 js객체가 있던 string 형태로 변환시켜준다.
	* JSON.parse() -> 괄호 안에 있는 string을 array로 만들어준다.

	* array(변수).forEach(메서드); -> 각각 변수마다 메서드를 실행해 준다.
	* ex) 변수 array안에 있는 아이템이 3개라면 메서드를 각각 실행하여 총 세번 반복한다.

	* (Arrow Function)
	* 위 메서드를 array.forEach((item) => 메서드); -> 화살표 함수로도 바꿀 수 있고, 위와 동일한 결과를 반환한다.
	
	* array.filter(sexyFilter) -> filter도 기본적으로 forEach와 같이 모든 item을 순환한다. 그러나sexyFilter가 true를 반환해야 해당 item이 유지된다.
	만약 false 반환 시 해당 item은 삭제된다.
	
	* ex) arr = [213, 2344, 5235, 234234, 1231]
	* function sexyFilter(item) { return > 1000} 
	* arr.filter(sexyFilter) -> item이 1000이상인 것만 true를 반환하므로 arr에서 1000이상 item만 값이 남게 된다. 즉, arr는 [2344, 5235, 234234, 1231]이 남게 된다.
	* `filter는 새로운 arr를 반환하는 것이다. 기존의 arr는 유지된다.`

13. navigator 함수
	* navigator.geolocation.getCurrentPosition(onGeoOk, onGeoError);
	* 성공 시 onGeoOk 함수 실행, 실패시 onGeoError 함수 실행

14. weather
	* https://openweathermap.org/current 에서 api를 이용해 불러올 수 있다.
	* fetch(url) -> url을 JavaScript가 실행한다.
