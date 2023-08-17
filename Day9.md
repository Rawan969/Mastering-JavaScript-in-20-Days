<h1>JavaScript the Hard Parts</h1>
<h2>What did I learn today?</h2>
<h3>Asynchronous javaScript</h3>
<p><strong>promises, Async & the Event loop</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/6532b2cc-209e-4f87-8bcb-b0c43e47793a">
<p><strong>Asynchronicity in javaScript</strong></p>
<img src = "https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/0e646e09-422d-47c6-bc12-f1ada6a0498a">
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/d085162c-8b32-47cd-8dff-c0f32a3dab80">
<p><strong>Asyncronous Browser features</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/0084b226-35b4-484f-a915-10d4f51f6b22">
<p><strong>Web API Example</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/f458e432-0f5e-44c0-a849-549fa0b5df65">
<p><strong>Callback Queue &Event loop</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/5860e047-38aa-4e7f-af95-928c7c4a2b37">
<p><strong>Callback Hell & Async</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/af5380e5-21c0-492f-a105-71abf56a5fd2">

<h3>Promises</h3>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/9bee5c89-a541-451e-ae58-ab9b154e74c6">
<p><strong>Promises Example: fetch</strong></p>
<img src="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/b0e97b49-e02b-4db0-a3d0-12e9d884113d">
<p><strong>then method</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/9f500773-b2a8-43fe-a1f0-9a91746e1952">
<p><strong>Web APIs & promises Example:</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/64e0c280-cb61-402a-9b47-f20948f2704d">
<p><strong>Promises Review</strong></p>
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/89030e7a-084a-4046-9d88-3d56be88930a">
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/03e35881-9a02-49d9-90cc-ee778497249e">
<img src ="https://github.com/Rawan969/Mastering-JavaScript-in-20-Days/assets/121896627/b9639d0f-62cb-4edc-8e4a-416462b6b211">

<h3><a href = "https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%203/tasks.md">Challenges</a></h3>
<h3>Question 1:</h3>
<div>
 const task1 = (cb) => setTimeout(() => {
    const message = "Task 1 has executed successfully!";
    cb(message);
}, 3000);

const task2 = (cb) => setTimeout(() => {
    const message = "Task 2 has executed successfully!";
    cb(message);
}, 0);

const task3 = (cb) => setTimeout(() => {
    const message = "Task 3 has executed successfully!";
    cb(message);
}, 1000);

const task4 = (cb) => setTimeout(() => {
    const message = "Task 4 has executed successfully!";
    cb(message);
}, 2000);

const task5 = (cb) => setTimeout(() => {
    const message = "Task 5 has executed successfully!";
    cb(message);
}, 4000);

const asyncTasks = [task1, task2, task3, task4, task5];

const executeInSequenceWithCBs = (tasks, callback) => {
    const results = [];

    function executeNextTask(index) {
        if (index >= tasks.length) {
            callback(results);
            return;
        }

        const currentTask = tasks[index];
        currentTask((message) => {
            results.push(message);
            executeNextTask(index + 1);
        });
    }

    executeNextTask(0);
};

executeInSequenceWithCBs(asyncTasks, (messages) => {
    console.log(messages);
});

</div> </br>
<h3>Question 2:</h3>
<div>
 const apis = [
  {
    apiName: "products",
    apiUrl: "https://dummyjson.com/products",
  },
  {
    apiName: "users",
    apiUrl: "https://dummyjson.com/users",
  },
  {
    apiName: "posts",
    apiUrl: "https://dummyjson.com/posts",
  },
  {
    apiName: "comments",
    apiUrl: "https://dummyjson.com/comments",
  }
];

const executeInParallelWithPromises = (apis) => {
  const promiseArray = apis.map(api => {
    return fetch(api.apiUrl)
      .then(response => response.json())
      .then(apiData => ({
        apiName: api.apiName,
        apiUrl: api.apiUrl,
        apiData: apiData,
      }))
      .catch(error => ({
        apiName: api.apiName,
        apiUrl: api.apiUrl,
        error: error.message,
      }));
  });

  return Promise.all(promiseArray);
};

// Usage
executeInParallelWithPromises(apis)
  .then(results => {
    console.log(results);
  })
  .catch(error => {
    console.error("Error:", error);
  });

</div> </br>
<h3>Question 3:</h3>
<div>
 const apis = [
  {
    apiName: "products",
    apiUrl: "https://dummyjson.com/products",
  },
  {
    apiName: "users",
    apiUrl: "https://dummyjson.com/users",
  },
  {
    apiName: "posts",
    apiUrl: "https://dummyjson.com/posts",
  },
  {
    apiName: "comments",
    apiUrl: "https://dummyjson.com/comments",
  }
];

const executeInSequenceWithPromises = (apis) => {
  const results = [];

  function fetchApiSequentially(index) {
    if (index >= apis.length) {
      return Promise.resolve(results);
    }

    const api = apis[index];
    return fetch(api.apiUrl)
      .then(response => response.json())
      .then(apiData => {
        results.push({
          apiName: api.apiName,
          apiUrl: api.apiUrl,
          apiData: apiData,
        });
        return fetchApiSequentially(index + 1);
      })
      .catch(error => {
        results.push({
          apiName: api.apiName,
          apiUrl: api.apiUrl,
          error: error.message,
        });
        return fetchApiSequentially(index + 1);
      });
  }

  return fetchApiSequentially(0);
};
</br>
executeInSequenceWithPromises(apis)
  .then(results => {
    console.log(results);
  })
  .catch(error => {
    console.error("Error:", error);
  });

</div>


