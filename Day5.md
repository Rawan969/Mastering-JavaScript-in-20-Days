<h1>What did I learn today?</h1>
<h3>conditionals </h3>
<p>if statement let us execute code under a certain condition.</p>
<p>code in the if block only runs if the (condition) is true.</p>
<p>we can use else to run other code if (condition) is false.</p>
<p>we can chain else and if blocks to account for multiple conditions.</p>
<p>the (condition) is usually an expression that evaluates to a boolean0</p>
<p>if its given some other value ,js will convert it to a boolean and decide based on its "truthiness".</p>
<h3>Boolean (logical) operators (! , && , ||)</h3>
<h3>conditional ternary operator , it needs 3 values to work</h3>
<h3>Loops let us run the same chunk of code multiple times.</h3>
<p>for loops require us to:
1.declare and initialize a loop counter
2. give a condition for the loop to keep running.</p>
<p>we can use for ... of to iterate over characters in a string or items in an array because strings and arrays are "iterables".</p>
<p>while loops : let us run a chunk of code over & over if a (condition) is true .</p>
<h3>map & filter </h3>
<p>the map and filter methods also let us process all the items in an array.</p>
<p>map calls a function on each item in an array to create a new array.</p>
<p>filter calls a true/false function on each item and creates a new array with only the items where function return true.</p>
<h3>Spread (...)</h3>
<p>is another neat trick for iterating over arrays, it lets us take all the items in an array and spread 'em around.</p>
<h3>A synchronous code </h3>

<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators">Challenge 1</a></h2>
<div>
  function checkSign(num) { </br>
  return (num >0) ? "positive" </br>
    : (num < 0) ? "negative"  </br>
    : "zero"; </br>

}</br>

checkSign(10); </br>
</div> </br>
<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array">Challenge 2</a></h2>
<div>
  const ratings = watchList.map(item => ({ </br>
  title: item["Title"],</br>
  rating: item["imdbRating"] </br>
})); </br>
console.log(JSON.stringify(ratings)); </br>
</div> </br>

<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-filter-method-to-extract-data-from-an-array">Challenge 3</a></h2>
<div>
  const filteredList = watchList </br>
  .filter(movie => { </br>
    // return true it will keep the item </br>
    // return false it will reject the item</br>
    return parseFloat(movie.imdbRating) >= 8.0;</br>
  })</br>
  .map(movie => {</br>
    return {</br>
      title: movie.Title,</br>
      rating: movie.imdbRating</br>
    };</br>
  });</br>

// Only change code above this line

console.log(filteredList);</br>
</div> </br>

<h2><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code">Challenge 4</a></h2>
<div>
  const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"]; </br>

function golfScore(par, strokes) { </br>
  // Only change code below this line </br>
if (strokes == 1) { </br>
    return names[0]; </br>
  } else if (strokes <= par - 2) { </br>
    return names[1]; </br>
  } else if (strokes === par - 1) { </br>
    return names[2]; </br>
  } else if (strokes === par) { </br>
    return names[3]; </br>
  } else if (strokes === par + 1) { </br>
    return names[4]; </br>
  } else if (strokes === par + 2) { </br>
    return names[5]; </br>
  } else { </br>
    return names[6]; </br>
  } </br>

  return "Change Me"; </br>
  // Only change code above this line </br>
} </br>

golfScore(5, 4); </br>
</div> </br>
