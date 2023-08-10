<h1>What did I learn today?</h1>
<p>1.We've talked about functions ===> do things </p>
<p>2.parameters we pass in function should be named like variables and behave like it</p>
<p>3.NAN(not a number):is a something you might find if things have gone wrong in your program like divide by 0 </p>
<p>4.return values : a return statement specifies the functions output value</p>
<p>5.We've discussed different situations in functions with return keyword and without it </p>
<p>6.Arrow function let us create unnamed function without much code </p>
<p>7.We've talked about different methods and how to deal with them like : seAtrribute, removeAtrribute,toString</p>
<p>8.We have learned about scope of variables (global and local scope)</p>
<p>9.var vs let  ===> how they behave inside the block {}</p>
<p>10.what are Events listeners and handler function and how to deal with them </p>

<h3><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions">Challeng 1 </a></h3>
<div>
  // Declare the myGlobal variable below this line </br>
let myGlobal = 10; </br>

function fun1() {</br>
  // Assign 5 to oopsGlobal here </br>
 oopsGlobal=5; </br>
} </br>

// Only change code above this line </br>

function fun2() { </br>
  let output = ""; </br>
  if (typeof myGlobal != "undefined") { </br>
    output += "myGlobal: " + myGlobal; </br>
  }  </br>
  if (typeof oopsGlobal != "undefined") { </br>
    output += " oopsGlobal: " + oopsGlobal; </br>
  } </br>
  console.log(output); </br>
} </br>
</div> </br>

<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions">Challenge 2 </a></h2>
<div>
  function myLocalScope() { </br>
  // Only change code below this line </br>
let myVar = 10;  </br>
  console.log('inside myLocalScope', myVar); </br>
} </br>
myLocalScope(); </br>

// Run and check the console </br>
// myVar is not defined outside of myLocalScope  </br>
console.log('outside myLocalScope', myVar); </br>
</div> </br>

<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions">Challenge 3 </a></h2>
<div>// Setup </br>
const outerWear = "T-Shirt"; </br>

function myOutfit() { </br>
  // Only change code below this line </br>
 const outerWear = "sweater"; </br>
  // Only change code above this line </br>
  return outerWear; </br>
} </br>

myOutfit(); </br>
</div> </br>

<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/stand-in-line">Challenge 4 </a></h2>
<div>
  function nextInLine(arr, item) { </br>
  // Only change code below this line </br>
  arr.push(item); </br>
  return arr.shift(); </br>
  // Only change code above this line </br>
} </br>

// Setup </br>
let testArr = [1, 2, 3, 4, 5]; </br>
 
// Display code </br>
console.log("Before: " + JSON.stringify(testArr)); </br>
console.log(nextInLine(testArr, 6)); </br>
console.log("After: " + JSON.stringify(testArr)); </br>
</div> </br>
