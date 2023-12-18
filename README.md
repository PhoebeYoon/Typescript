#### 🍎 Typescript


## 함수리턴시에 암묵적리턴를 주의하자
[ts]
```js
function calc(income:number){
     if(income <50_000)
          return income*1.2
}

let result = calc(51000)
console.log(result)
```
조건문에서 50000 이하이면 income*1.2를 하지만 50000이상일때는 딱히 어떻게 해야 하는 것이 명시되어 있지 않다.   
컴파일후에 콘솔창에서 결과를 확인해 보면 'undefined' 라고 나온다.   

즉 함수가 제대로 구현되지 않았음을 알수있다. 이런 현상을  이것을 검증할 수 있도록  
tsconfig.json 파일항목에서  **```   "noImplicitReturns": true,   ```** 로 바꿔서보자.   
그러면 ts 파일에 **calc 함수에 줄무늬가** 나오면서 에러가 있음을 알 수 있다.    


아래와 같이 내용을 추가해서 수정하자.  
[ts]
```js
function calc(income:number):number{
     if(income <50_000)
          return income*1.2
     return income * 1.3;
}

let result = calc(51000)
console.log(result)
```
이외에도,  

```
 "noUnusedLocals": true,   --> 사용하지 않는 지역변수
 "noUnusedParameters": true, --> 사용하지 않는 파라메터 
 "noImplicitReturns": true,  --> 암묵적인 return 값을 확인
```
위의 환경을 고려하여 다음과 같이 사용해보자.   
[ts]
```js
function calc(income:number , taxYear:number ):number{
     if( taxYear<2023 )
          return income*1.2
     return income * 1.3;
}
let result = calc(51000, 2022)
console.log(result)
```

### 만약 함수의 파라메터에 물음표를 추가하여 옵션으로 만들어보자   
[ts]
```js
function calc(income:number , taxYear?:number ):number{
     if( (taxYear || 2023)<2023 )
          return income*1.2
     return income * 1.3;
}
let result = calc(51_000, 2022)
console.log(result)
result = calc(10_1000);
console.log(result);   
```

calc(10_000)에서 2번째 옵션을 주지 않을경우에 함수 calc()의 2번째 인자에 ? 를 추가하고,   
if문에서 위와 같이 수정하여 taxYear가 없는경우를 대비할 수 있다.   
또는 아예 초기값을 지정해서 해결할 수도 있다.  
``` function calc(income:number , taxYear=2022 ):number{   ```  

