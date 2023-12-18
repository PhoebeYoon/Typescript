#### 🍎 Typescript


## enum 
[ts]
```js
enum Size {Samll='s', Medidum='m', Large='l'}
// const enum Size {Samll='s', Medidum='m', Large='l'}  (1)아래참조
const mysize : Size = Size.Samll;
console.log(mysize)

컴파일하면,

"use strict";
var Size;
(function (Size) {
    Size["Samll"] = "s";
    Size["Medidum"] = "m";
    Size["Large"] = "l";
})(Size || (Size = {}));
const mysize = Size.Samll;
console.log(mysize);
```
이렇게 복잡하게 되지만 enum 앞에 const 를 붙여서 변수로 선언해주면   
[js] 
```
(1)
"use strict";
const mysize = "s" /* Size.Samll */;
console.log(mysize);
```
간단히 컴파일된다.  
