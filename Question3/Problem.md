## 📝 Problem
We need to **implement a memoization function**.

- Given a function `fn`, return a **memoized version** of it.  
- A memoized function:
  - **Caches results** for inputs so the same input is never recomputed.
  - Returns the **cached value** if called again with the same arguments.

### Constraints
1. **sum(a, b)**  
   - Returns `a + b`.  
   - `(a, b)` and `(b, a)` are treated as **different inputs**.  
     Example: `sum(2,3)` and `sum(3,2)` should both compute separately.  

2. **fib(n)**  
   - Fibonacci function.  
   - `fib(n) = 1` if `n <= 1`.  
   - Otherwise, `fib(n) = fib(n-1) + fib(n-2)`.  

3. **factorial(n)**  
   - Factorial function.  
   - `factorial(n) = 1` if `n <= 1`.  
   - Otherwise, `factorial(n) = n * factorial(n-1)`.  