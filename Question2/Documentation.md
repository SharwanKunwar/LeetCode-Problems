# LeetCode Problem: Implement `expect` Function  

## 🟢 Why  
Testing is an essential part of software development. Developers often need a simple way to check if values behave as expected. Instead of writing long conditional checks, we can build a tiny utility function (`expect`) that mimics testing frameworks like **Jest** or **Mocha**.  

This helps:  
- Validate logic quickly  
- Catch unexpected results early  
- Build problem-solving habits aligned with industry practices  

---

## 🟡 What  
We implemented a custom `expect` function that allows developers to:  

1. **toBe(val)** → checks for strict equality (`===`).  
   - Throws `"Not Equal"` if they don’t match.  
2. **notToBe(val)** → checks for inequality (`!==`).  
   - Throws `"Equal"` if they are the same.  

This problem strengthens understanding of:  
- JavaScript **function design**  
- **Error handling**  
- **Closures** in JavaScript  

---

## 🔵 How  
We solved it by:  

1. Creating a higher-order function `expect(val)` that returns an object.  
2. Defining two methods inside that object:  
   - `toBe(value)` → compares using `===`.  
   - `notToBe(value)` → compares using `!==`.  
3. Using `throw new Error()` to handle the required error cases.  

### ✅ Example Usage  

```javascript
var expect = function(val) {
    return {
        toBe: function(value) {
            if (value === val) return true;
            throw new Error("Not Equal");
        },
        notToBe: function(value) {
            if (value !== val) return true;
            throw new Error("Equal");
        }
    }
};

// Test Cases
expect(5).toBe(5);       // true
expect(5).notToBe(5);    // throws "Equal"
expect(5).notToBe(null); // true
