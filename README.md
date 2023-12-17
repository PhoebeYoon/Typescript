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
7. 컴파일된 index.js를 열어보면  ``` var age =20 ```    
    자바스크립트 es6 버전에서는 var는 지양하는 키워드이므로 컴파일시에 최신 es6로 컴파일하도록 해야 한다.   
     이를위해 터미널에서   
  ```
  > tsc --init ( tsconfig.json 파일이 만들어진다 이 파일을 연다 )
  내용중에서  "target": "es2016", 찾는다.  es2016 지운후에 'es'라는 글자를 입력하면
  여러종류의 버전 목록이 열리는데 여기서 변경할 수 있다.
  다만 es2016 버전은 현재 거의 모든 브라우저에서 사용되는 버전이므로 그대로 유지해도 좋다.
   ```
8. tsconfig.json 파일에서 "module":"common.js"라는 부분 아래에 있는   
   ```
   "rootDir": "./src",
   ...
    "outDir": "dist/",
   추가로
   "removeComments": true,
   "noEmitOnError": true,  변경한다 
    ```

   로 변경하고 주석을 해제한다.
   그리고 vs code에 있는 폴더를 정리해야 한다.    
   📁src (타입스크립트 파일일 있는 곳을 지정)    
   📁outDir ( 컴파일후 js 파일이 담길 폴더지정)   
   ```  
   \src \ index.ts
   tsconfig.json
   
   ```
9. tsconfig.json 이 변경되었으니 아래와 같이 실행해보자
    ```
   > tsc 엔터
    결과로 dist 폴더가 생성되고 그 안에 index.js 파일을 확인해보자 

    ```
