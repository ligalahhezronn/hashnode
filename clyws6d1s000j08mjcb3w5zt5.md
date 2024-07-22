---
title: "JavaScript Promises"
seoTitle: "JavaScript Promises"
seoDescription: "JavaScript Promises"
datePublished: Mon Jul 22 2024 09:24:49 GMT+0000 (Coordinated Universal Time)
cuid: clyws6d1s000j08mjcb3w5zt5
slug: javascript-promises
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1721640101628/f7784019-d0b2-439c-9634-fd55be04485d.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1721640200991/f84ee3f5-dcfc-4d63-a1b2-d5db2b2e7fc6.png
tags: javascript

---

### What are JavaScript Promises

A JavaScript promise is an object representing the eventual completion of or failure of an asynchronous operation.

### Key Features of Promises

1. Pending: The initial state, neither fulfilled nor rejected.
    
2. Fulfilled: The operation completed successfully.
    
3. Rejected: The operation failed.
    

### How promises work

Promises are created using the **promise** constructor, which takes a function with **resolve** and **reject** parameters. These parameters determine the outcome of the promise.

Let’s create a general example involving a simple operation like fetching data from a database or an API. For simplicity, we’ll simulate this with a function that returns a promise, which resolves or rejects based on a random condition.

```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    // Simulate network delay
    setTimeout(() => {
      let success = Math.random() > 0.3; // 70% chance of success
      if (success) {
        resolve({
          data: ["item1", "item2", "item3"],
          message: "Data fetched successfully!"
        });
      } else {
        reject("Failed to fetch data.");
      }
    }, 1500); // 1.5 second delay
  });
}

// Using the fetchData function
fetchData()
  .then((response) => {
    console.log(response.message); // Logs success message
    console.log("Fetched Data:", response.data); // Logs fetched data
  })
  .catch((error) => {
    console.error(error); // Logs error message if rejected
  });
```

### Handling Promises with .then and .catch

```javascript
fetchData()
  .then((response) => {
    console.log(response.message); // Logs success message
    console.log("Fetched Data:", response.data); // Logs fetched data
  })
  .catch((error) => {
    console.error(error); // Logs error message if rejected
  });
```

# Chaining Promises

Promises can be chained to handle multiple asynchronous tasks sequentially:

```javascript
// Simulates an asynchronous operation that fetches data
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      let success = Math.random() > 0.2; // 80% chance of success
      if (success) {
        resolve("Fetched data");
      } else {
        reject("Failed to fetch data");
      }
    }, 1000); // 1 second delay
  });
}

// Simulates an asynchronous operation that processes the data
function processData(data) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      let success = Math.random() > 0.3; // 70% chance of success
      if (success) {
        resolve(`Processed ${data}`);
      } else {
        reject("Failed to process data");
      }
    }, 1000); // 1 second delay
  });
}

// Simulates an asynchronous operation that saves the result
function saveResult(result) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      let success = Math.random() > 0.1; // 90% chance of success
      if (success) {
        resolve(`Saved result: ${result}`);
      } else {
        reject("Failed to save result");
      }
    }, 1000); // 1 second delay
  });
}

// Chaining the promises
fetchData()
  .then((data) => {
    console.log(data); // Logs "Fetched data"
    return processData(data); // Passes the data to the next promise
  })
  .then((processedResult) => {
    console.log(processedResult); // Logs "Processed Fetched data"
    return saveResult(processedResult); // Passes the processed result to the next promise
  })
  .then((savedMessage) => {
    console.log(savedMessage); // Logs "Saved result: Processed Fetched data"
  })
  .catch((error) => {
    console.error(error); // Logs any error encountered in the chain
  });
```

This approach ensures that each operation is performed in sequence and only if the previous operation is successful. If any operation fails, the ‘catch()’ block will handle the error.

### Promise Utilities: Promise.all **and** Promise.race

These are two useful methods for working with multiple promises concurrently.

### Promise.all

Takes an array of promises and returns a single promise that resolves when all of the input promises have resolved. If any of the input promises reject, the returned promise will immediately reject with that error.

```javascript
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Fetched data"), 1000);
  });
}

function processData() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Processed data"), 1500);
  });
}

function saveResult() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Saved result"), 2000);
  });
}

Promise.all([fetchData(), processData(), saveResult()])
  .then((results) => {
    console.log(results); // Logs ["Fetched data", "Processed data", "Saved result"] when all promises resolve
  })
  .catch((error) => {
    console.error(error); // Logs the error if any promise rejects
  });
```

## Promise.race

Takes an array of promises and returns a single promise that resolves or rejects as soon as one of the input promises resolves or rejects.

```javascript
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Fetched data"), 1000);
  });
}

function processData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => reject("Processing error"), 500); // This will reject first
  });
}

function saveResult() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Saved result"), 2000);
  });
}

Promise.race([fetchData(), processData(), saveResult()])
  .then((result) => {
    console.log(result); // Logs "Processing error" because the second promise rejects first
  })
  .catch((error) => {
    console.error(error); // Handles the first rejection or resolution
  });
```

# Async/Await

With Async/Await, handling promises feels more like writing synchronous code, making it cleaner and easier to understand.

```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      let success = Math.random() > 0.2; // 80% chance of success
      if (success) {
        resolve("Fetched data");
      } else {
        reject("Failed to fetch data");
      }
    }, 1000); // 1 second delay
  });
}

async function getData() {
  try {
    const data = await fetchData();
    console.log(data); // Logs "Fetched data"
  } catch (error) {
    console.error(error); // Logs "Failed to fetch data"
  }
}

getData();
```