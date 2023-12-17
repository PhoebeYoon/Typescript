#### 🍎 Typescript

## 설치방법
1. node.js 를 설치한다
   ``` 
   > sudo npm i -g  typescript
   > tsc -v ( 설치버전 확인)
   ```
2. vs code 설치 
3. index.ts 라는 파일을 생성한다. 타입스크립트는 자바스크립트에서 사용하는 모든 내용을 사용할 수 있다.
   [index.ts]
   ```js
   console.log('Hello world! ')
   ```
4. 컴파일한다. 터미널로 이동하고 작성한 index.ts 파일이 있는지 확인 한 후 ``` > tsc index.ts ```  정상적으로 실행되었다면 index.js 파일이 따로 생성되어 있을 것이다.
5. index.js를 터미널에서 실행해 보자 터미널에서 ``` >node index.js ``` 실행결과로 터미널에 Hello world! 가 나온다.  index.js를 실행하기 위해 앞에 node라는 명령어를 주어야 한다. 현재 실행환경은 브라우저가 아니라 node.js에 있기 때문이다.
6. 이제 index.ts 로 돌어가서 아래와 같이 추가해 보면 age 변수아래로 빨간색 줄이 나타난다.   
 ```js
   let age:number =20;
   age ="a" 
```    
타입체크를 하기 때문에 에러가 발생한것을 즉시 발견할 수 있다.   
   
