## How

We solve this using closers in js

```js
var createCounter = function(n) {
    let count = n;   // store the initial value
    return function() {
        return count++;  // return current count, then increment
    };
};

```

## Breakdown:

1. let **count = n;**
We create a variable count that holds the starting value.

2. **Return function**
We return a function (the counter) that can be called later.

3. **count++**
Each time the returned function is called:

    * It first returns the current value of count.

    * Then, it increases count by 1 (post-increment).

4. **Closure magic**
The inner function “remembers” the variable count even after createCounter finishes running. This is possible because of closure in JavaScript.