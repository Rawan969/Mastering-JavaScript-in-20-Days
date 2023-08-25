![image](https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/5cce8ca9-1e24-43c5-876a-d0a491615ee3)<h1>Deep JavaScript Foundations, V3</h1>
<h2>What did I learn today?</h2>
<h2>Advanced Scope</h2>
<p><strong>Lexical Scope</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/8ce2ebe3-317b-4f39-9cab-2795c8f84ef8">
<p><strong>Dynamic Scope</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/7507b7a0-171a-4aa8-b4eb-8a7fd477491f">
<p><strong>Function Scoping</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/8c349c33-7ec0-4345-9401-e5da25b2bd59">
<p><strong>IIFE Pattern</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/854f7e06-1d1e-4847-b4f8-67187f9f920a">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/eaaecfa0-a324-4b47-9197-b23f26460ebc">
<p><strong>Block Scoping</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/9ba4032d-4e5a-4a0c-bb87-4093af07af90">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/990f192f-520c-4437-8772-a6943098f043">
<p><strong>Choosing let or var</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/b7d27f09-595a-4689-b042-6ff69e7bd089">
<p><strong>Explict Block</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/8adafa19-4596-447d-850d-e123c2cdab17">
<p><strong>Const</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/6e8628cf-908f-4fcd-9f1c-5496f165157d">
<p><strong>Hoisting</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/276fe10c-9242-45ce-a6ae-602aa21cd0c3">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/9ee7202f-1b1c-4fcf-a271-0b3157f977d2">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/1a31576c-721c-4ad9-8317-014188ebf695">
<p><strong>let doesn't hoist</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/36596579-664f-48e5-a819-b68922bb9bad">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/8cc0315d-d69f-4eb2-82cb-57aee7c7dd6a">
<h2><a href="https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%204/tasks.md">Challenges</a></h2>
<h3>QUESTION #1</h3>
<div>
  for (var i = 0; i < 5; i++) { </br>
  (function (index) { </br>
    setTimeout(function () { </br>
      console.log("value of [i] is: ", index); </br>
    }, 100); </br>
  })(i);</br>
} </br>
In this code, the IIFE is immediately invoked with the current value of i as an argument (index). Inside the IIFE, the index parameter holds the value of i for that iteration, and it is captured by the setTimeout callback function, ensuring that each callback logs the correct value of i.
</div> </br>
<h3>QUESTION #2</h3>
<div>
  In the given code snippet, the variable array is defined inside the loop. Therefore, in each iteration of the loop, a new empty array is created and assigned to the array variable. As a result, the push operation only affects the array within the current iteration, leading to the observed output.

To achieve the desired behavior of accumulating all the values of i in a single array, you need to define the array variable outside the loop, so it maintains its state across iterations.</br>
let array = []; </br>

for (let i = 0; i < 5; i++) { </br>
   array.push(i); </br>
   console.log("Current array is: ", array); </br>
} </br>
</div> </br>
<h3>QUESTION #3</h3>
<div>
  In the given code snippet, the issue is related to the closure behavior of JavaScript. The arrow function within the loop captures the variable i, but it captures the reference to i, not its value at the time the arrow function is created. Since the loop has already finished executing by the time the arrow functions are invoked, all of them reference the final value of i, which is 5.

To achieve the desired behavior and have each arrow function capture the value of i at the time it was created, you can create a new scope for each iteration of the loop using an IIFE (Immediately Invoked Function Expression). This way, each arrow function will capture a different reference to i, maintaining the correct value for each iteration.

Here's the modified code:</br>
let functions = []; </br>

for (var i = 0; i < 5; i++) { </br>
  (function (index) { </br>
    functions.push(() => { </br>
      console.log("Current value of i is:", index); </br>
    }); </br>
  })(i); </br>
} </br>

functions.forEach((func) => func()); </br>
In this code, the IIFE is used to create a new scope for each iteration of the loop. Inside the IIFE, the index parameter captures the value of i at the time the IIFE is invoked. The arrow function then captures this unique value of index, resulting in the desired output:
</div></br>
