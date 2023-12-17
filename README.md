#### 🍎 Typescript

## About Typscript

#### Staticaly-typed | Dynamically-typed
- Staticaly-typed  (C++, C#, Java)    
예를들면,   

  ```js
  int num=10;
  num="a" // 허용안됨
  ```
  
  
- Dynamically-typed ( Javascript, python, Ruby)     
예를들면,   
  ```js
  int num=10;
  num="a" // 코드를 실행하기 전까지는 아무 이상없는 것처럼 진행됨
  ```
실제로 버그가 발생했지만 프로그램을 테스트를 하긴 전까지는 그 사실을 알지 못하고 넘어간다. 그래서 typescript라는 것은 결국 javascript with Type Checking 이다.
그래서 Staticaly-typed 로 지정된 언어로 코딩하는 것처럼 선언시에 변수의 유형을 명시적으로 설정하도록 하고 있다.   
typescript로 코드를 작성하고  typescript컴파일를 통해 js로 코드로 변환시키는 것이다. 
## typescript 실행환경
- 자바스크립트는 브라우저에서 실행되는데 브라우저는 이미 자바스크립트를 실행할 수 있는 런타임을 갖고 있다. 그래서 typescript로 코드를 작성하고 이를 컴파일해서 자바스크립트로 변환해야 브라우저에서 문제없이 실행될 수 있다.  현재까지 브라우저에서는 타입스크립트를 인식하지 못하기 때문이다.
- 타입스크립트를 실행하려면 node.js를 설치해야 한다.  node.js는 브라우저없이 자바스크립트를 실행할 수 있는 환경을 제공하는데 이 환경에 타입스크립트를 추가하여 사용하는 것이다.
  
  ```
  > sudo npm install typescript --save--dev  ( 설치환경)
  > tsc 파일이름.ts  ( 실행시 / tsc 는 컴파일하라는 의미 )
  ```
  

