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

<h2><a href = "https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup">challenge 3 </a></h2>
<p>
  // Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line
  for(var i=0;i<contacts.length;i++){
    if(contacts[i].firstName===name){
      return contacts[i][prop] || "No such property" ; 
    }
  }
  return "No such contact";

  // Only change code above this line
}

lookUpProfile("Akira", "likes");
</p> </br>

<h2> <a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/write-reusable-javascript-with-functions">challenge 4 </a></h2>
<p>
  function reusableFunction() {  </br>
  console.log("Hi World");  </br>
}  </br>
reusableFunction();  </br>
</p> </br>

<h2> <a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understanding-undefined-value-returned-from-a-function">challenge 5 </a></h2>
<p>
  // Setup
let sum = 0;  </br>

function addThree() { </br>
  sum = sum + 3; </br>
} </br>
function addFive() { </br>
  sum = sum + 5; </br>
} </br>

// Only change code below this line </br>


// Only change code above this line </br>

addThree(); </br>
addFive(); </br>
</p> </br>

<h2><a href = "https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return">challenge 6</a></h2>
<p>
  function timesFive(num) { </br>
  return num * 5; </br>
} </br>

const answer = timesFive(5); </br>
</p> </br>






