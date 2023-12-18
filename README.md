#### 🍎 Typescript

[ts]
```js
let employee:{
     id:number,
     name : string
} = { id:1, name : ''}

employee.name ="Mosh"

```
위의 내용중에서 name:'' 으로 초기화했다  나중에 name='Mosh'를 입력받는다.  

만약 name? : '' 처럼 name을 옵션으로 처리한다면 상식적이지 않다.   
id만 가지고는 별 의미가 없기 때문이다. 그리고 id는 주로 각 요소를 구별하는 경우에 사용하므로, 
id 앞에 readonly 를 붙여서  
```js  
readonly id:number,
... 
```
로 해도 좋다.  

#### 메소드를 추가해보자.
```js
let employee:{
      readonly id:number,
      name : string,
      retire : (date : Date) => void
 } = { 
      id:1, 
      name : '',
      retire : (date :Date) =>{
        date = new Date();
        console.log(date)
      }
 }
 
 employee.name ="Mosh"
 console.log(employee.retire)

```

이것을 type으로 바꿔보자.   
위의 let employee 부분을 반복해야 하는 경우에 type으로 정의해서 사용할 수 있다.   


```js
type Employee ={
     readonly id:number,
      name : string,
      retire : (date : Date) => void
}

let employee: Employee= {
      id:1, 
      name : 'Mosh',
      retire : (date :Date) =>{
          console.log(date)
      }
 }
 console.log(employee.retire)

```










참조: https://www.youtube.com/watch?v=d56mG7DezGs


