#### 🍎 Typescript


## union 

union 타입이란 여러종류의 값을 가질 수 있는 변수를 정의하고 싶을때 사용할 수 있다.
10킬로를 어떤 사람은  숫자 10으로  또는 10kg로 표현할 수도 있는 것이다.  
이럴때 사용하면 좋은 타입이다.   

[ts]
```js
function kgToLbs (weight: number | string):number {
     if(typeof weight ==='number')
          return weight* 2.2
     else 
          return parseInt(weight) *2.2
}

console.log(kgToLbs(10))
console.log(kgToLbs('10kg'))

```

