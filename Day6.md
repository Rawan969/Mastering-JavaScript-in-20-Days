<h1>What did I learn today?</h1>
<p><strong>1.API</strong>provides URLS that point at data we care about</p>
<p><strong>fetch()</strong>lets us use js to load data from APIs , it is a built in function and its return promise.</p>
<p>it takes time to fetch data from the network.</p>
<p><strong>promisses</strong> can be in 3 possible states: 1-pending 2-fullfilled 3-rejected</p>
<p><strong>await</strong> lets us tell js to stop and wait for an asynchronous operation to finish.</p>
<p>the promise we get from fetch() resolves to a response object.</p>
<p>the <strong>body</strong> of the promise contains the data we care about. </p>
<p>calling the .json() method on the response parses its body as a json object.</p>
<p><strong>2.Destructing objects & arrays</strong> is a fancy wayof declaring multiple variables at once.</p>
<p><strong>.split()</strong> it returns an array of substrings by splitting a string at a certain character</p>
<p><strong>.trim()</strong> removes spaces</p>
<p><strong>3.Async function</strong> is we try to await something in regular function js doesnt allow it, we need to make it an async function ,this tells js to expect to await async operations inside the function.</p>
<p><strong>4.Modules</strong> let us split big codebases across multiple files and they create their own scope.</p>
<p><strong>export</strong> lets us expose variables from our module's scope to outside world.</p>
<p><strong>import</strong> lets us use an exposed variable from another module.</p>
<p><strong>5.Debugging</strong> a certainty of coding stuff will go wrong.</p>
<p>console.log() (or .warn() or .error() is one way to understand whats happening when your program runs).</p>
<p>you can also use the browser's debbuger to pause js and inspect whats happening. </p>
<p>the <strong>debbuger statement</strong> creates to breakpoint where js will pause and let you look around.</p>
<p><strong>Error Handling</strong>once we've discovered where in our program an error is likely , we can do something about it.</p>
<p>usually errors will cause js to stop running our code but sometimes we might to try again or try a differnet way or if it was optional just skip it and move on with our program's lives.</p>
<p><strong>try</strong> lets us "watch out" for potential errors.</p>
<p>its friend <strong>catch</strong> lets us manage errors when they occur.</p>

<h3><a href ="https://github.com/Rawan969/API">Challenge</a></h3>



