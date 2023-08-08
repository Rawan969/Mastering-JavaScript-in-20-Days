<h1>What did I learn today?</h1>
<h3>*values & Data types </h3>
<p><strong>js has two kinds of data </strong></p> 
<p>1.primitive types(strings,numbers,boolean,null,undefiend)</p> </br>
<p>2.objects(document)</p> </br>
<h4>*working with strings</h4>
<h3>*operaters</h3>
<h4>-Arithmetic operators (+ - / *)</h4>
<h4>-comparison operators (< > <= >=)</h4>
<h4>-Equality operators (strict: ===  loosey-goosy: ==) , the strict compare the type of two values but loosey-goosey does more one step which is trying to convert the value</h4>
<h3>*Expressions</h3>
<h3>*how to declare variable using let or const and assigning value to it </h3>
<p>cnost:the value of the variable that iam creating cant ever be changed </p> </br>
<h3>*variables names </h3>
<p>Variables point to values </p>
<h3>*Evaluating code:try to run some codes and see what happen</h3> </br>
<h3>*statements vs Expressions </h3>
<p>an expression "asks" js for a value</p> </br>
<p>a statement "tells" js to do something(declare/assign)</p> </br>
<h2>challenges</h2>
<div>
<strong>QUESTION #1</strong>
Consider the following JavaScript code:

let a = 0;  </br>
let b = "0";  </br>
let c = false;  </br>
let d = "false";  </br>

console.log(a == b);  ---> return true (it will convert the type of variable b to number then compare it)  </br>
console.log(b === c); ---> return false (compare the types of two variables )  </br>
console.log(!!d);     ---> return true  </br>
What will be the output of each console.log statement? You MUST explain WHY. </br>
</div>

<div>
<strong>QUESTION #2:</strong>
Consider the following JavaScript expression:
console.log(4 + 5 * "7"); ---> return 39 (first it will convert the string to number then multiply it by 5 and add to it 4 ) </br>
What will be the output of this expression? You MUST explain the steps of evaluation taken by JS. </br>
</div>

<div>
<strong>QUESTION #3:</strong>
Evaluate the following expression:
let result = 5 + 2 * 3 - 1; ---> the output will be : 10 (in order of arithmetic operations)  </br>
What will be the output of this expression? You MUST explain the steps of evaluation taken by JS.  </br>
</div>

<div>
<strong>QUESTION #4:</strong>
Consider the following code:

let x = 10;
let y = '10';
console.log(x == y); ---> return true (it will convert the type of variable y to number then compare it )  </br>
console.log(x === y); ---> return false (compare the types of two variables )  </br>
What will be the output of each console.log statement? You MUST explain WHY. </br>
</div>

<div>
<strong>QUESTION #5:</strong>
Given the code below:

let num = "15"; </br>
let isPositive = true; </br>
let result = (num > 10 && isPositive) || num < 0; </br>
console.log(result);  ----> return true  </br>
What is the value of result? You MUST explain the steps of evaluation taken by JS </br>
</div>


