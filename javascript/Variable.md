# Variable

변수의 생성단계
1. Declaration (선언)
변수 객체에 변수를 등록한다. 이 변수 객체는 스코프가 참조하는 대상이 된다.
2. Initialization (초기화)
변수 객체에 등록된 변수를 메모리에 할당한다. 이 단계에서 변수는 undefined로 초기화된다.
3. Assignment (할당)
undefined로 초기화된 변수에 실제값을 할당한다.


4가지 방법이 있다.
- var
- const
- let
- 아무것도 쓰지 않기

자바스크립트에서 변수 선언은 `var`로만 가능했으나 EcmaScript2015부터 `let`과 `const`가 추가되었다. 보통은 `const`를 기본적으로 사용하고, 변수를 업데이트하고 싶으면 `let`을 쓴다. 만약 ES2015를 지원하지 않는 오래된 브라우저를 쓴다면 `var`을 써야한다. 그렇지 않으면 절대로 사용하지 마라.

|차이점|var|const|let|
|------|---|---|---|
|1. Redeclaring(재선언)|가능|불가능|불가능|
|2. Changing value(재할당)|가능|불가능|가능|
|3. Scope|함수 내부에서 선언 된 변수만 지역변수로 한정(function)|블록 내부에서 선언된 변수만||
|4. Hoisting|발생|발생|발생|
|5. Object Properties|전역객체의 properties이다.|전역객체의 properties가 아니다.|전역객체의 properties가 아니다.|


### 1. Redeclaring(재선언)
- var 
    - Var로 선언한 변수는 중복해서 선언 및 초기화(값 할당)가 가능하며, 마지막에 할당된 값이 변수에 저장된다. 
    - 초기화 없이 선언만 한 경우에는 선언문 자체가 무시된다. 
- const
이미 선언한 변수를 다시 선언할 경우 에러가 발생한다.
- let
이미 선언한 변수를 다시 선언할 경우 에러가 발생한다.

### 2. Changing value(재할당)
- var 
    - 값을 업데이트할 수 있다. 
    - 한 번 선언 및 초기화 후에는 var 키워드 없이 변수 이름만으로 재할당 가능
    - `var` 키워드는 선언시에도 생략이 가능하다. 하지만 생략하면 함수 안에서 선언하더라도 전역변수가 된다.
- const
    - constant(상수), 값이 바뀔 수 없다. `immutable`
    - 처음에 선언할 때 꼭 초기화를 해주어야 한다.
    - 선언과 동시에 초기화, 할당이 이루어져야한다. (선언 전 사용 불가능)
- let
    - 값을 업데이트할 수 있다. (메모리 주소가 변경된다.)
    - 한 번 선언 및 초기화 후에는 `let` 키워드 없이 변수 이름만으로 재할당 가능

### 3. Scope
Global Scope, Block Scope, Local Scope, Function Scope 존재함

Fuction Scope: 함수 내부에서 선언 된 변수만 지역변수로 한정, 함수를 제외한 영역에서 선언하면 전역변수(if문, for문, while문, try/catch문 등의 {}블록 또한 전역 변수가 된다.)

Block Scope: {} 블록 안에서 선언하면 지역변수가 된다. (함수 내부는 물론 if문, for문, while문, try/catch문 등의 {}블록 포함)
{} 블록 내부에서 선언된 변수는 블록 외부에서 액세스 할 수 없다. 선언과 동시에 임의의 값으로 초기화될 수 있음. 자신을 선언한 블록과 모든 하위 블록을 스스로의 스코프로 가진다. var과 유사하지만 var의 경우 스코프가 '자신을 선언한 블록'이 아니라 자신의 선언을 포함하는 함수

- var 
*Function Scope* 함수 내부에서 선언한 변수만 지역 변수로 간주한다. {} Block 내부에서 선언된 변수더라도 Block 밖에서 접근할 수 있다.

- const, let
*Block Scope*의 범위를 가지는 지역 변수를 선언한다. 

### 4. Hoisting
코드를 실행하기 전의 과정 중에 범위가 지정된 변수를 정의하는 Lexical Environment 과정이 포함되기 때문에, 뒷 줄에서 선언된 변수도 앞 줄의 코드에서 참조할 수 있게 된다.  
호이스팅에 대해 잘 이해하지 못하면 버그가 발생할 수 있으니 모른다면 맨 앞줄에 변수 선언하는 것이 좋음.

- var
    - 변수 호이스팅이 발생한다.
    - 하지만 초기화되기 전에 사용하면 기본 값인 `undefined`를 표시한다. (`undefined`로 초기화해놓은 것.)
- let, const
    - 호이스팅되지만, 코드 실행 전에 사용할 수 없다. 
    - `let`의 경우 코드 블럭은 변수로 선언은 된 상태지만, 초기화되기 전까지는 사용하면 `ReferenceError`가 뜬다. (선언 전 사용 불가능)
    - const의 경우에도 `ReferenceError`가 뜬다. 
    - 변수는 초기화되기 전까지 TDZ(Temporal Dead Zone)에 있다.



[source](https://www.w3schools.com/js/js_scope.asp)


