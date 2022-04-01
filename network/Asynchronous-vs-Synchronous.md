# Asynchronous vs Synchronous

기본적으로 프로그래밍 모델은 동기 방식이다. 하지만 비동기 방식의 프로그래밍은 컴퓨팅 리소스를 효율적으로 사용하는 데에 중요하다. 

APIs를 구축할때,  Event-Based Architecture를 만들 때와 serverless에서 매우 중요하다. 

example)
- Synchronous Processing
    - User Interfaces
    - HTTP APIs 

- Asynchronous Processing
    - Batch-processing
    - Long-running tasks


```javascript
let a = 1
let b = 2

setTimeout(function() {
    console.log('Async')
}, 1)


fetch('/').then(function(){
    console.log('Fetch')
})

console.log('Synchronous')

console.log(a)
console.log(b)
```

ex) dot Ben, Dot catch, dot fetch
