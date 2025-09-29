
⚠️ **Do not use the built-in `Array.map` method.**

---

## ❓ Why
- The `.map()` method is very useful for transforming arrays.  
- Sometimes you may want to **understand how it works internally** or implement it manually for learning purposes.  
- This helps improve **JavaScript fundamentals** and **problem-solving skills**.

---

## ⚙️ How
- Create an **empty array** to store results.  
- **Loop through** each element of the input array.  
- For every element, **call the mapping function** with the element and its index.  
- **Push the returned value** into the result array.  
- **Return** the transformed array after the loop completes.

---

## 📌 What (Solution)
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
