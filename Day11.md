<h1>Deep JavaScript Foundations, V3</h1>
<h2>What did I learn today?</h2>
<p><strong>Primitive types</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/e5c5a0fd-98df-44ff-9090-1e73dc431942">
<p><strong>types of operator</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/e3a74463-03f8-4726-ac0f-1a907f7bd6ef">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/66ae8b4b-385c-427b-9ae4-b34625d46124">
<p><strong>kinds of emptiness</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/1ae9e0f3-8f6d-41e4-890d-b762e2aef1f0">
<p><strong>NaN</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/b7ef9872-4f6d-4eb6-848e-1484f1389558">
<p><strong>Negative zero</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/7d29dd1f-6f37-4c57-a741-3723e2152028">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/9fe82a67-3836-4bf3-aa89-5a2a7f9f39de">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/4802412e-bbd5-4bd1-aadc-c8400dde2fd3">
<p><strong>Exercise</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/eb050d27-9287-4bfd-85e8-5bd3656a4098">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/53846efb-0168-44a7-a0c7-532c8414120b">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/65f7dbb5-3232-4324-bf72-05acf144a505">
<p><strong>Fundamental objects</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/c577a0af-49d4-4ece-aa71-4dc8a21d0fbe">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/ed2325bc-e3f4-4f1c-b1d4-9d8e6b1bd4c3">
<h2>Coercion</h2>
<p><strong>Abstract operations</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/bacf0e71-d6e1-4929-8e99-798327f9b098">
<p><strong>ToString</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/61940d02-7e0e-4ea3-801c-4283d8738aa9">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/2d6e6c21-3d56-4c8f-ad38-1c0a3b50185f">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/12e8505b-f1af-4018-b53f-3fcfa655a903">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/c06d79bf-35a2-41b4-b170-b3adbcd9f1c0">
<p><strong>ToNumber</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/6ba04350-64c2-416f-a043-c1d074b3ddaa">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/a6a4c987-0a83-48bc-8fa4-38f11e821f1c">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/b9026876-9dd6-402c-8230-e4c282ba7b18">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/af766ae1-6661-48b8-90c2-d5738461adeb">
<p><strong>ToBoolean</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/d579f5b1-a679-4fec-972a-63c8a38b4cb0">
<p><strong>Boxing</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/575b256f-6ca5-42b6-85bf-4e301e1f1bcc">
<p><strong>Coercion: corner cases</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/2e3ace60-5561-4091-b7ef-9927b0c2cdd9">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/72738ba0-b923-4789-a5ec-7e2f74d4afc3">
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/853accc9-5119-4d2c-b1de-f42649178d4e">
</br>
<h2><a href="https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%201/tasks.md"></a>Challenges</h2>
<h3>Question 1:</h3>
<div>
  function convertStringToNumber(input) {
  if (typeof input === 'string') {
    return +input;
  } else {
    return { value: input, type: typeof input };
  }
}
</div>
<h3>Question 2:</h3>
<div>
 function checkNaN(value) {
  return Number.isNaN(value);
} 
</div>
<h3>Question 3:</h3>
<div>
 function isEmptyValue(value) {
  return value === undefined || value === null || value === "";
} 
</div>
<h3>Question 4:</h3>
<div>
  function compareObjects(obj1, obj2) {
  if (typeof obj1 === 'object' && typeof obj2 === 'object') {
    return JSON.stringify(obj1) === JSON.stringify(obj2);
  } else {
    return [obj1, obj2];
  }
}
</div>
<h3>Question 5:</h3>
<div>
  function complexCoercion(input) {
  if (typeof input === 'number') {
    return Boolean(input.toString());
  } else if (typeof input === 'string') {
    return Boolean(input);
  } else if (input === null || input === undefined) {
    return false;
  } else {
    return input;
  }
}
</div>

