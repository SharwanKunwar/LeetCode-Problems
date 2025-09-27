# 🔢 Create Counter (LeetCode Problem)

## 📌 Problem Statement
Given an integer `n`, return a **counter function**.  
This counter function initially returns `n` and then returns **1 more than the previous value** every subsequent time it is called (`n, n + 1, n + 2, ...`).

### Example 1
**Input:**  
```
n = 10
["call","call","call"]
```
**OutPut**
```
[10,11,12]
```


**Explanation:**  
- `counter()` → 10 (first call returns `n`)  
- `counter()` → 11 (returns 1 more than previous)  
- `counter()` → 12 (and so on...)  

---

## ✅ Constraints
- `-1000 <= n <= 1000`  
- `0 <= calls.length <= 1000`  
- `calls[i] === "call"`  

---

## 💡 Solution (JavaScript)
```javascript
/**
 * @param {number} n
 * @return {Function} counter
 */
var createCounter = function(n) {
    let count = n;
    return function() {
        return count++;
    };
};

// Example usage
const counter = createCounter(10);
console.log(counter()); // 10
console.log(counter()); // 11
console.log(counter()); // 12
```