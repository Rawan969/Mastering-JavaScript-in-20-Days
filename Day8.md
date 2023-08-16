<h1>JavaScript the Hard Parts</h1>
<h2>What did I learn today?</h2>
<h3>Closure</h3>
<p>closure is the most esoteric of javaScript concepts</p>
<p>Enables powerful pro-level functions like 'once' and 'memoize'</p>
<p>many javaScript design patterns including the module pattern use closure</p>
<p>Build iterators, handle partial application and maintain state in an asynchronous world</p>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/6abe7a52-829e-4e38-bf22-3c5c0e6dc0c4">
<h4>Functions get a new memory every run/invocation</h4>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/f5b77404-0a12-4e16-9fe3-6efc1238b66d">
<h4>Functions can be returned from other functions in javaScript</h4>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/664b28f6-6c67-4a17-8366-c3e87aee421a">
<h4>Nested function scope</h4>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/cfe2b26e-47a6-4dc3-84f7-322c0a543ea2">
<h4>Retaining function memory</h4>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/7dfc15c9-42dc-4b19-b320-26d84171a04f">
<h4>BackPack is also called ==> close over variable environment</h4>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/caea39da-9f75-499e-894e-8295582fe7cd">
<h4>Multiple closure instances</h4>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/5cc44750-0d5e-4bd7-a2bb-1de810e44c68">
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/d970137b-4f4b-4393-af07-0b68b1a67e98">

<h2><a href ="https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%202/tasks.md">Exercises </a></h2>
<h4>Question 1:</h4>
<div>
  function createCounter(num) { </br>
  let counter = num;  </br>

  return function() {  </br>
    counter++;  </br>
    return counter;  </br>
  };  </br>
}  </br>

const counter1 = createCounter(0);  </br>
console.log(counter1()); // Output: 1  </br>
console.log(counter1()); // Output: 2  </br>
</div>  </br>
<h4>Question 2:</h4>
<div>
  function calculateAverage(nums) { </br>
  const sum = nums.reduce((acc, num) => acc + num, 0); </br>
  const count = nums.length; </br>

  return function() { </br>
    return sum / count; </br>
  }; </br>
} </br>

const numbers = [10, 20, 30, 40, 50]; </br>
const averageCalculator = calculateAverage(numbers); </br>

console.log(averageCalculator()); // Output: 30 </br>
</div> </br>
<h4>Question 3:</h4>
<div>
  function powerOf(base) { </br>
  return function(exp) { </br>
    return Math.pow(base, exp); </br>
  }; </br>
} </br>

const square = powerOf(2); </br>
console.log(square(3)); // Output: 8 (2^3) </br>
</div> </br>
<h4>Question 4:</h4>
<div>
  function compose(...functions) { </br>
  return function(arg) { </br>
    return functions.reduceRight((result, func) => func(result), arg); </br>
  }; </br>
} </br>

// Example usage </br>
function add2(x) { </br>
  return x + 2; </br>
} </br>

function multiply3(x) { </br>
  return x * 3; </br>
} </br>

function subtract5(x) { </br>
  return x - 5; </br>
} </br>

const composedFunction = compose(subtract5, multiply3, add2); </br>
console.log(composedFunction(10)); // Output: 31 </br>
</div> </br>

