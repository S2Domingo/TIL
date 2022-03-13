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

## function
dynamic typing, flexible parameter의 특성이 있기 때문에 함수를 작성할 때 타입을 명시하지 않는다. arguments에 전달되는 values에 의해 data types이 결정되며, 함수가 필요한 유형을 반환한다.

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

- object 안에 있는 instance를 변경하려고 할 때는 constant여도 변경이 가능하다. const로 선언한 object 전체의 값을 바꾸려고 할 때 에러가 발생함.

[source](http://www.tcpschool.com/javascript/js_object_create)

() -> parentheses

{} -> curly braket

[] -> square braket

## object properties

## Array

