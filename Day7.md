<h1>JavaScript the Hard Parts</h1>
<h2>What did I learn today?</h2>
<p><strong>JavaScript Principles:</strong> when javaScript code runs,it :
1. goes through the code line by line and runs/execute each line known as the thread of execution.
2. saves data like strings and arrays so we can use that data later in its memory.</p>
<p><strong>Execution context:</strong> created to run the code of a function - has to parts
1.thread of execution
2.memory</p>
<p><strong>Call stack</strong>
-js keeps track of what function is currently running.
-Run a function-add to call stack
-finish running the function - js removes it from call stack.</p>
<p><strong>DRY(DONT REPEAT YOURSELF).</strong></p>
<p><strong>we can generlize the function to make it reusable.</strong></p>
<p><strong>Generalizing functions:</strong> "parameters" mean we dont need to decide what data to run our functionality on until we run the function then we can provide an actual values ['arguments']when we run the function.</p>
<p><strong>which is our higher order function?</strong></p>
<p>the outer function that takes in a function is our higher-order function.</p>
<p><strong>which is our callback function?</strong></p>
<p>the function we insert is our callback function.</p>
<p>callbacks and higher order functions simplify our code and keep it DRY.</p>
<p><strong>pair programming</strong></p>

<h3><a href = "https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem">Challenge 1</a></h3>
<div>
  const squareList = (arr) => { </br>
  // Only change code below this line </br>
  return arr </br>
          .filter(num => num > 0 && num % parseInt(num) === 0)</br>
          .map(num => Math.pow(num, 2)); </br>
  // Only change code above this line </br>
}; </br>

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]); </br>
console.log(squaredIntegers); </br>
</div> </br>
<h3><a href = "https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs">Challenge 2</a></h3>
<div>
  // Only change code below this line </br>
function urlSlug(title) { </br>
  
let a = title.toLowerCase() </br>
a = a.split(" "); </br>
a = a.join(`-`) </br>
return a </br>
} </br>
// Only change code above this line</br>
console.log(urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone")); </br>
console.log(urlSlug("Winter Is Coming")) </br>
</div> </br>
<h3><a href = "https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%201/tasks.md">Challenge 3</a></h3>
<div>
  
</div>
