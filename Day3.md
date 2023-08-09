<h1>What did I learn today?</h1>
<h3>1.Arrays</h3>
<p>*grouping values into larger collections.</p> </br>
<p>*arrays can hold any type of items or mix of them. </p></br>
<p>*arrays are objects.</p> </br>
<p>*arrays can do lots of useful tricks like : sort , join and concat methods.</p> </br>
<p>2.methods we use with array like : pop and push</p> </br>
<p>3.mutable data can be edited like arrays.</p></br>
<p>4.immutable data always stay the same like srings and other primitives.</p> </br>
<p>5.variables themselves can also be immutable like: const. </p> </br>
<p>6.objects --> type of data it collects multiple values together to describe more complex data and its mutable</p> </br>
<p>7.We've talked about methods , nestead objects , Built in objects and finally we did quiz project.</p> </br>

<h2><a href = "https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice">challenge 1</a></h2>
<p>
  function forecast(arr) {  </br>
  // Only change code below this line </br>
  let forecast = ['cold', 'rainy', 'warm', 'sunny',       'cool', 'thunderstorms']; </br>
  arr = forecast.slice(2, 4); </br>

  return arr; </br>
} </br>

// Only change code above this line </br>
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms'])); </br>
</p> </br>

<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator">challenge 2</a></h2>
<p>
  function spreadOut() {  </br>
  let fragment = ['to', 'code'];  </br>
  let sentence =['learning',...fragment,'is', 'fun']; // Change this line  </br>
  return sentence;  </br>
}  </br>

console.log(spreadOut());  </br>
</p>  </br>

<h2><a href = " ">challenge 3 </a></h2>




