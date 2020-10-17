## Morning learning

### Exercise: Track the scalpel

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

