# 키워드 = 예약어
var = 예약어 
자바스크립트가 미리 예약해놓았기 때문
(Var 자체로 명령어이다) = 선언(이더정확) = 정의 


# 주석 
현시대에는 퍼포먼스보다는 가독성이 좋아야한다
읽기 쉬워야한다는 의미

* 코드를 잘 읽기 위해서는 남의 코드를 많이 읽는 연습을 꾸준히 해야한다
* 주석이 없어도 잘 읽히는 코드가 가장 좋은코드
* 코드는 바뀌었는데 , 주석은 안바꾸는 경우도 있기 때문에 ( 엄청난 혼란을 초래한다 )
* 카피하더라도 의미를 알아야 함 (왜 카피 했는지 설명할 수 있어야함)


# 프로그래밍

### 변수

메모리상의 주소 > 위치

메모리의 주소를 가르키는 것 > 변수
데이터를 가지고 있는 저장소 > 변수
어떤 값이 들어있는지 사람이 이해하기 쉽게 별칭을 주는 것 > 변수명
수많은 방(메모리) 중에 몇 호인지 찾아가는 행위 > 참조

변수 선언을 하면 > 자바스크립트 엔진이 기억함( 메모리의 주소를 기억하고 있다 )

변수를 선언하는 이유 : 어떤 연산을 하려면 , 값을 기억하고 있어야 함 (우리 뇌도 마찬가지 1+2를 하려면 뭐와 뭐를 더해야 하는지 알아야 연산을 해서 값을 도출 할 수 있음) 

ex)
var z = x + y ; > 또 쓰겠다는 의미
(x나 y에 다른 수를 대입할 수 있으므로)
var z = 1 + 2 ; > 한번 쓰고 말겠다는 의미
__이 둘의 차이는 재사용성__

변수 : 주소를 식별할 수 있다 

[자바스크립트 엔진이 하는 일중에]
변수에 값을 처음 넣는 것 > 초기화

아무도 쳐다보고 있지 않은 값을 대상으로 
지우는 행위를 하는 것 > garbage collection

### 동적 타이핑 

* 컴퓨터가 자료형의 종류를 아는 행위 > 타입추론

# Data Type [자료형]

* ES6 기준 data type 7개
* ES5 기준 data type 6개
* 기본자료(__Primitive__)형과 객체형은 서로 성격이 다름

### 기본 자료형

* undefined(변수 선언 이후 초기화하지 않은 상태)와 null(값이 없음을 명시적으로 표시)의 차이를 알아둬야함
* 스택 영역의 관리
* byte가 정해져 있음

<!—존재하지 않은 프로퍼티를 참조하면 undefined가 나온다 (자바스크립트에서는 이런 현상이 하나의 문법이다) —>

### 객체 

* 프로퍼티와 프로퍼티값으로 이루어진 것
    * ex) name: ‘lee’
* 힙 영역의 관리 ( 메모리가 늘었다 줄었다 하는 것 )


# 기본자료형

### Number

* 정수 : 소수점이 없는 것
* 실수 : 소수점이 있는 것
* __자바스크립트는 모든 숫자가 실수이다__(3은 3.0임)
* Infinity(상수) = 무한대 ( ex)-(253 -1) 와 253 -1를 넘는 수 를 무한대라고 칭함/ 무한대도+,-가 있음 )
* 숫자에 문자를 연산하면 에러대신 NaN이 출력됨 (자바스크립트 문법..ㅎ..)
* 

### String

* 원래 타언어(C,JAVA등)에서는 (기본자료형이 아닌 객체형으로 인지) 자바스크립트에서는 기본자료형임
* 자바스크립트는 ‘홀따옴표’를 사용하는게 일반적
* 홀따옴표 안에 홀따옴표는 중복되니까 밖을 큰따옴표로 묶음
* 값이 재할당 되었을 때 변경하지 않고 포인터로 재지목함

### 변경불가능성

기본자료형(이뮤터블) >
한 번 셋팅된 값을 바꿀 수 없다 = 객체 이외에는 변경할 수 없다 = 이뮤터블이다
ex)10을 지우지않고 새로운 공간에 1000이란 값을 재할당 받는 것

객체(뮤터블) >
한 번 셋팅된 값을 바꿀 수 있다 = 변경할 수 있다 = 뮤터블이다 
ex)10을 지우고 1000이란 값을 재할당 받는 것


# 객체형

* 극소수 빼고 거의 대부분이 객체형이다. 때문에 자바스크립트는 객체지향형 언어이다
* 기본자료형을 제외한 나머지 값들은 모두 객체이다
* 빈객체도 객체타입이라고 인식함
<!— 어떠한 특징들을 속성이라고 칭함 —>


# 변수

* 한번쓰고 버릴 때 가 아닌 유지할 필요가 있을 때 변수를 사용한다
* 다른 사용자가 변수의 존재 목적을 쉽게 알 수 있도록 의미있는 이름을 지정하여야한다
* 변수하나당 var하나씩 명시하여야 한다 (가동성을 좋게하기위함, 실수를 줄이기 위함)
* 값을 할당하지 않은 변수 즉 선언만 되어있는 변수는 undefined로 초기값을 갖게 된다
* 중복선언은 아주 안좋은 문법이므로 사용하지 않는 것이 좋다


### 전역변수

기본적으로 쓰지 않음
어플리케이션이 종료되기 전까지 계속 메모리를 확보하고있는 상태 

### 지역변수

함수내부에서 선언한 변수, 함수의 라이브러리가 종료되는순간 가비지컬렉션의 대상이 됨

<!-- ReferenceError : 참조에러 -->

# 동적타이핑

> 변수를 선언할 때 자료형(데이터타입)을 미리 선언하지 않는다, 값이 할당되는 시점에 변수의 타입이 추론된다
<!-- 타입:어떠한 값을 하나 가지고 있는 것
언디파인드는 언디파인드라는 하나의 값을 갖고 있는 타입이기때문에 언디파인드타입이라고 함 -->

* 자신이 가지고 있는 값이 타입이 되는 것이 동적타이핑 

# 정적타이핑

* 어떤 값인지 미리 선언하고 시작하는 타입

---

## var키워드로 선언된 변수의 문제점

> 자바스크립트는 함수 내에서만 선언한 변수만 인지하고 그외에것은 전역변수로 인지 <br>
> #####  *전역변수는 쓰면 안되는 것

>ES5는 변수선언이 var한가지 뿐이지만,
ES6에서는 다른 선언방법이 있기때문에
var는 쓰지 않는 것이 좋음 
그 이유는 문제점들이 많기 때문
(전역변수의 남발, 변수호이스팅등등의 문제들)


# etc

코딩 컨벤션을 잡아주는 툴 > ESLint
툴은 적극적으로 사용하는 것이 좋음

실수를 할 가능성이 있는 건 무조건 피해가는 게 좋음

