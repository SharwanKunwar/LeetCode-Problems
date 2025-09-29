# 💡 Solution

```js
/**
 * Custom map function without using Array.map
 * @param {number[]} arr - Input array
 * @param {Function} fn - Mapping function
 * @return {number[]} - Transformed array
 */
var map = function(arr, fn) {
    const result = [];
    for (let i = 0; i < arr.length; i++) {
        result.push(fn(arr[i], i));
    }
    return result;
};
```

## 📖 Explanation

1. **Create an empty array** called `result` to store transformed values.

2. **Loop through each element** of the input array `arr`.

3. For every element `arr[i]`, **call the mapping function** `fn(arr[i], i)`:
   - `arr[i]` is the element value.
   - `i` is the element index.

4. **Push the returned value** into the `result` array.

5. **Return** the `result` array after the loop completes.

This mimics the behavior of JavaScript’s built-in `.map()` method without actually using it.
