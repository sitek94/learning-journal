## Morning learning

### Exercise: [Track the scalpel](https://eloquentjavascript.net/code/#11.1)

I managed to solve the exercise but the author's doesn't stop to amaze me with his solutions.
They're so clean, consise and easy to understand. After looking at them I've got this feeling: 
*Man... it was so obvious.*

```javascript
async function locateScalpel(nest) {
  let current = nest.name;
  for (;;) {
    let next = await anyStorage(nest, current, "scalpel");
    if (next == current) return current;
    current = next;
  }
}

function locateScalpel2(nest) {
  function loop(current) {
    return anyStorage(nest, current, "scalpel").then(next => {
      if (next == current) return current;
      else return loop(next);
    });
  }
  return loop(nest.name);
}
```

### Exercise: [Building Promise.all](https://eloquentjavascript.net/code/#11.2)

I thought that I've corectly solved this one but when I checked the solution I realized that there was
a bug in my code. A bug that not always would show itself. 

```javascript
function Promise_all(promises) {
  return new Promise((resolve, reject) => {
    if (!promises.length) resolve([]);
    
    let results = [];
    
    // Iterate through each of the promises passed
    for (let i = 0; i < promises.length; i++) {
      
      // Store result of the promise in correct position
      promises[i]
        .then(result => {
          results[i] = result;
        })
      
        // When catches an error in one of the promises,
        // immediately rejects
        .catch(reject)
      
        // If haven't catched any errors and length of results
        // equals length of the promises then resolve with results
        .then(() => {
        
          /* --- HERE --- */
          if (results.length === promises.length) resolve(results);
        });
    }  	
  });
}
```
The problem was when I tried to compare results length with promises length. If the promises resolved in the order they were called, everything was fine but the problem was one for example 3 promise resolved first.
```javascript
// i=2 is the first promise that resolves
results[2] = value;

// results = [undefined, undefined, value]
```
Because `results[2]` is the only item in the array, `results[0]` and `results[1]` are set to `undefined`
and the length of results is `3`, so in the final `.then()` call it passes the if statement and resolves the promise
even though other promises haven't finished.

After fixing
```javascript
function Promise_all(promises) {
  return new Promise((resolve, reject) => {
    if (!promises.length) resolve([]);
    
    let results = [];
    let pending = promises.length;
    
    for (let i = 0; i < promises.length; i++) {
      
      promises[i]
        .then(result => {
          results[i] = result;
          pending--;
        })
        .catch(reject)
        .then(() => !pending && resolve(results));
    }  	
  });
}
```

And finally author's solution
```javascript
function Promise_all(promises) {
  return new Promise((resolve, reject) => {
    let results = [];
    let pending = promises.length;
    for (let i = 0; i < promises.length; i++) {
      promises[i].then(result => {
        results[i] = result;
        pending--;
        if (pending == 0) resolve(results);
      }).catch(reject);
    }
    if (promises.length == 0) resolve(results);
  });
}
```

## Pocket globe app

A lot of progress today. Some of the things that I've been working on:
* keyboard events 
* navbar buttons
* media queries
* transitions for widgets

I also tested production build and it's amazing because its blazing fast comparing to development build.

<hr>
Total: 8.5hrs
