<h1>Deep JavaScript Foundations, V3</h1>
<h2>What did I learn today?</h2>
<h2>Scope</h2>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/6f9bcb9b-f83b-4fcc-909b-532027e3c747">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/a3cb5b2e-c989-41c2-8f8a-da9f1d3d753b">
<p><strong>Compilation & Scope</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/cebac686-b8bc-4628-b047-87f1c01ab986">
<p><strong>Nested Scope</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/9a759d35-d092-4722-bef6-92ae2e1059d6">
<h2>Scope & Function Expressions</h2>
<p><strong>Function Expressions</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/879c8085-040b-41a0-8e08-e9115db5fe61">
<p><strong>Naming Function Expressions</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/d776b651-5499-49e5-bf60-cd0cfe43da70">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/8c1f2dcd-5915-4219-b18f-cd380cf1fa54">
<p><strong>Arrow Functions</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/c85fc20d-73f3-44c4-9dc5-a4dc753d149f">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/8fd07b8a-6f4d-4eca-afe1-6f0e1128471c">
<p><strong>Function Types Hierarchy</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/a15fb681-1ca6-4b53-85e4-17b0b7f54093">
</br>
<h2><a href="https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%203/tasks.md">Challenges</a></h2>
<h3>QUESTION #1</h3>
<div>
  const arrowHOF = (normalFunc) => { </br>
  return (...args) => { </br>
    return (times) => { </br>
      let result = normalFunc(...args); </br>
      for (let i = 0; i < times; i++) { </br>
        console.log(result); </br>
      } </br>
    }; </br>
  }; </br>
}; </br>

const exampleNormalFunc1 = (a, b, c) => { </br>
  return a * (b + c); </br>
} </br>

const exampleNormalFunc2 = (x, y) => { </br>
  return x * y; </br>
} </br>

const exampleNormalFunc3 = (string) => { </br>
  return string + " " + string + " " + string + "!"; </br>
} </br>

const hofNormalFunc1 = arrowHOF(exampleNormalFunc1); </br>
const hofNormalFunc2 = arrowHOF(exampleNormalFunc2);</br>
const hofNormalFunc3 = arrowHOF(exampleNormalFunc3); </br>

console.log(hofNormalFunc1(3, 4, 5)(2)); // logs 60 twice </br>
console.log(hofNormalFunc2(20, 35)(4)); // logs 700 four times </br>
console.log(hofNormalFunc3("Meow")()); // logs "Meow Meow Meow!" once </br>
</div> </br>
<h3>QUESTION #2</h3>
<div>
  const preserveThis = (func) => { </br>
  return func.bind(func); </br>
}; </br>

// Example object </br>
const obj = { </br>
  name: 'John', </br>
  greet: function (greeting) { </br>
    console.log(`${greeting}, ${this.name}!`); </br>
  } </br>
}; </br>

// Wrap the greet function using preserveThis </br>
const preservedGreet = preserveThis(obj.greet); </br>

// Call the wrapped function as a method of the object </br>
preservedGreet('Hello'); // Output: "Hello, John!" </br>
</div> </br>
<h3>QUESTION #3</h3>
<div>
  <p>
    Reasoning for Example 1's Output:
In this example, the variable x is declared in the scope of the outer1 function. The inner function inner1 is defined within the scope of outer1, so it has access to the variables in the outer scope. When inner1 is invoked using inner1(), it logs the value of x, which is 10, because it's accessing the x variable from its outer scope.
  </p>
  </br>
  <p>
    Reasoning for Example 2's Output:
In this example, the variable x is declared in the scope of the outer2 function. Inside the inner2 function, a new variable x is declared with a value of 20. This inner variable x shadows the outer variable x. When inner2 is invoked using inner2(), it logs the value of the inner x, which is 20, because it's accessing the inner variable.

In the second example, the inner variable x within the inner2 function's scope takes precedence over the outer variable x. This is due to variable shadowing, where a variable with the same name in an inner scope overrides a variable with the same name in an outer scope.
  </p>
</div>
