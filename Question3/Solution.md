## 💡 Solution

We can solve this by writing a **higher-order function** `memoize(fn)` that:  
1. Uses a **cache object** to store results.  
2. Creates a **unique key** for arguments (like `"2,3"`).  
3. If the key exists in cache → return stored result.  
4. Otherwise → compute `fn(...args)`, store it, and return it.

---

## 🔧 Code

```js
// Memoize function
function memoize(fn) {
    const cache = {};

    return function(...args) {
        const key = args.join(","); // Create a unique key
        if (cache[key] !== undefined) {
            return cache[key]; // Return cached result
        }
        const result = fn(...args); // Compute normally
        cache[key] = result;        // Store in cache
        return result;
    };
}
