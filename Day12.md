<h1>Deep JavaScript Foundations, V3</h1>
<h2>What did I learn today?</h2>
<h2>Equality</h2>
<p><strong>Double & Triple Equals</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/36eb0711-db23-4989-a39a-1bde670f8c35">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/bb6e71ea-0d29-4741-95d5-2dca6d14d315">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/9deaf30d-cff2-441b-b90a-aac11f845823">
<p><strong>Coercive Equality</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/09e1c8e0-c164-473b-9afb-041890a5c5bd">
<p><strong>Double Equals Algorithm</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/dd46b300-a8e0-482b-b969-cd1c43eecc62">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/ed934912-b6fc-40ba-a6ea-617538c94fa2">
<p><strong>Corner cases</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/a56c78b0-c1c8-4e33-99f3-d00cd40f3e8a">
<p><strong>corner cases: Booleans</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/c7752fb0-af43-4aa9-9c12-598990bb1452">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/ed5ad124-9294-4ae5-84e2-3699b75ec810">
<p><strong>The case for double equals</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/04f6d6ab-da35-493d-96c1-317c4a9a5f1f">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/45bd8399-c7ba-4d8e-80a5-d65453404255">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/fbdbeae9-6668-4bc2-aacb-4bba8065501c">
<h2>Exercise</h2>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/730ee4f4-f8fb-4c4f-bd95-a17a44e0978c">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/906e3efc-ac38-484b-9b94-886e3d777773">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/30d78654-30c3-4b43-b997-7c9a055c3af0">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/73ceb3f3-dcc1-4b22-8d32-ff08cb8b0946">
</br>
<h2>Static Typing</h2>
<p><strong>TypeScript & flow</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/b305b6f0-ec24-4916-b38d-830ebfd8bd54">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/ac50bdd0-64dc-470e-a868-b19305223c2e">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/1d45984c-67c4-4609-ba8b-eceb0f5c3f86">
<p><strong>Custom Types</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/1bf4eab4-88ed-4fea-addf-a259b514ef85">
<p><strong>Validating operand types</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/3d77473c-de30-4e56-9807-1522ede68086">
<h2><a href="https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%202/tasks.md">Challenges</a></h2>
<h3>QUESTION #1</h3>
<div>
  interface HelloWorldPromise extends Promise<string> {} </br>

interface CheckBooleanPromise extends Promise<boolean> {} </br>

interface ReturnObjPromise extends Promise<{ x: string; y: number }> {} </br>

type PromisesArray = [HelloWorldPromise, CheckBooleanPromise, ReturnObjPromise]; </br>

const sayHelloWorld: HelloWorldPromise = new Promise((resolve, reject) => { </br>
  resolve("Hello world!"); </br>
}); </br>

const checkBoolean = (boolean: boolean): CheckBooleanPromise => </br>
  new Promise((resolve, reject) => { </br>
    if (boolean) { </br>
      resolve(boolean); </br>
    } else { </br>
      reject(`Input is false :(`); </br>
    } </br>
  }); </br>

const returnObj: ReturnObjPromise = new Promise((resolve, reject) => { </br>
  resolve({ </br>
    x: "meow", </br>
    y: 45, </br>
  }); </br>
}); </br>

const promisesArray: PromisesArray = [sayHelloWorld, checkBoolean, returnObj]; </br>

type PromisesResult = { </br>
  sayHelloWorld?: string; </br>
  checkBoolean?: boolean | string; </br>
  returnObj?: { x: string; y: number }; </br>
}; </br>

const convertToObj = async (array: PromisesArray): Promise<PromisesResult> => {</br>
  const result: PromisesResult = {}; </br>

  for (const promise of array) { </br>
    if (promise === sayHelloWorld) { </br>
      result.sayHelloWorld = await promise;</br>
    } else if (promise === checkBoolean) { </br>
      try { </br>
        result.checkBoolean = await promise(true); </br>
      } catch (error) { </br>
        result.checkBoolean = error; </br>
      }</br>
    } else if (promise === returnObj) { </br>
      result.returnObj = await promise; </br>
    } </br>
  }</br>

  return result;  </br>
}; </br>
 
convertToObj(promisesArray) </br>
  .then((obj) => console.log(obj))</br>
  .catch((error) => console.error(error)); </br>

</div></br>
<h3>QUESTION #2</h3>
<p>
  1, ReferenceError, ReferenceError </br>
  In JavaScript, variables declared with var have function-level scope, while variables declared with let and const have block-level scope. This means that var variables are accessible throughout the entire function in which they are defined, regardless of block scopes, while let and const variables are only accessible within the block they are defined in.
</p>
<h3>QUESTION #3</h3>
<div>
  undefined, ReferenceError, ReferenceError </br>
  In JavaScript, variables declared with var are hoisted to the top of their containing function or scope, which means they are declared before the code execution starts. However, their assignments are not hoisted, so they have an initial value of undefined.
</div>
<h3>QUESTION #4</h3>
<div>
  [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 1,100, 45 ] </br>
  Variables declared with var have function-level scope, so the re-declarations of var a within the if block affect the entire function's scope.
Variables declared with let and const have block-level scope, so the let b and const c declarations within the if block do not affect the outer scope.
</div>
