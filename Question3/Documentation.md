## 📖 Documentation

### `memoize(fn)`

#### Parameters:
- `fn`: A function (`sum`, `fib`, or `factorial`).

#### Returns:
- A **memoized version** of `fn`.

#### How it works:
1. Converts arguments into a cache key.  
2. If the key exists → returns cached value.  
3. If not → computes result, caches it, and returns it.  

---

## 📊 Example Execution (Cache Table for `sum`)

| Call              | Computation  | Cache                         |
|-------------------|--------------|-------------------------------|
| `memoizedSum(2,3)` | computes `5` | `{ "2,3": 5 }`                |
| `memoizedSum(2,3)` | from cache   | `{ "2,3": 5 }`                |
| `memoizedSum(3,2)` | computes `5` | `{ "2,3": 5, "3,2": 5 }`      |