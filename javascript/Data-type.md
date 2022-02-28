# Data types of javascript


## Primitive Type
boolean, null, undefined, number, string, symbol(ES6부터 제공)

## Reference Type
array, function, object

설명이 필요하지 않은 데이터 -> array
안에 담겨있는 데이터가 무엇인지 설명이 필요한 데이터 -> object

## null, undefined
undefined: 아직 타입이 정해지지 않음. 초기화되지 않은 변수나 존재하지 않는 값
null: object 타입, 아직 값이 정해지지 않음

```javascript
null ==  undefined; // true

null === undefined; // false
```

## object
Primitive Type을 제외한 자바스크립트의 기본 타입 
(But Primitive Type 또한 값이 정해진 객체로 취급하기 때문에 객체의 특징도 가지게 된다.)
property와 method를 같은 이름으로 묶어놓은 집합체
== attribute와 behavior, state와 behavior
원시 타입이 아닌 Reference Type은 객체이다. 

자바스크립트에서 객체 생성하는 방법
1. literal notation
2. constructor function
3. Object.create() Method

이와 같은 방법으로 생성되어 메모리에 대입된 객체를 인스턴스 (instance)라고 한다.

[source](http://www.tcpschool.com/javascript/js_object_create)

() -> parentheses
{} -> curly braket
[] -> square braket