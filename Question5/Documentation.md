# Custom Filter Function in JavaScript

## 📝 Problem
Given an integer array `arr` and a filtering function `fn`, return a new array containing only elements that satisfy the condition specified in `fn`.  

The returned array should include only elements for which `fn(arr[i], i)` returns `true`.

⚠️ **Do not use the built-in `Array.filter` method.**

---

## ❓ Why
- The `.filter()` method is commonly used to extract elements from an array based on a condition.  
- Implementing it manually helps **understand iteration, conditions, and array manipulation**.  
- Useful for **learning JavaScript fundamentals and problem-solving**.

---

## ⚙️ How
1. **Create an empty array** called `newArr` to store filtered elements.  
2. **Loop through each element** of the input array `arr`.  
3. For each element, **call the filtering function** `fn(arr[i], i)`:
   - If it returns `true`, **push the element** into `newArr`.  
   - Otherwise, skip the element.  
4. **Return** `newArr` after completing the loop.

---

## 📌 What (Solution)
```js
/**
 * Custom filter function without using Array.filter
 * @param {number[]} arr - Input array
 * @param {Function} fn - Filtering function
 * @return {number[]} - Filtered array
 */
var filter = function(arr, fn) {
    let newArr = [];
    
    for (let i = 0; i < arr.length; i++) {
        if (fn(arr[i], i)) {  // pass both element and index
            newArr.push(arr[i]);
        }
    }
    
    return newArr;
};
```


## 📖 Explanation

1. **Initialize an empty array** `newArr` to hold filtered elements.  

2. **Loop through each element** of `arr`.  

3. **Apply the filtering function** `fn` to each element and its index:  
   - If the function returns `true`, **push the element** into `newArr`.  
   - If the function returns `false`, **skip the element**.  

4. After looping through all elements, **return `newArr`** containing only elements that passed the condition.
