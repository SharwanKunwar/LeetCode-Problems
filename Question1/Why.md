## 💡 Why

* We use a closure so that count is private and not reset every time.
* If we just used a global variable, multiple counters would conflict with each other. Closures allow us to create independent counters.

```js
const counter1 = createCounter(5);
console.log(counter1()); // 5
console.log(counter1()); // 6

const counter2 = createCounter(100);
console.log(counter2()); // 100
console.log(counter2()); // 101
```
Here, counter1 and counter2 have separate internal states because of closures.