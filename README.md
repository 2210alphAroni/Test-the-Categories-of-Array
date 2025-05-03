# Test-the-Categories-of-Array

Memory Allocation Comparison: C++ vs JavaScript:

This project explores four major array memory allocation strategies using C++ and JavaScript.

Categories:

| Category            | Description                                                   |
|---------------------|---------------------------------------------------------------|
| Fixed Stack Dynamic | Size known at compile-time, stored on stack                   |
| Stack Dynamic       | Size determined at runtime, stored on stack (C++ only)        |
| Fixed Heap Dynamic  | Heap allocated but fixed size                                 |
| Heap Dynamic        | Fully dynamic in size and memory, heap-based storage          |

---

Language Differences:

C++:

- Provides both **stack** and **heap** allocation options explicitly.
- **Fixed Stack Dynamic**: `int arr[5];`
- **Stack Dynamic**: `int arr[size];` (Variable Length Arrays — compiler dependent)
- **Fixed Heap Dynamic**: `new int[size];` with manual `delete[]`.
- **Heap Dynamic**: `std::vector` grows/shrinks automatically.

JavaScript:

- Everything is heap allocated.
- Arrays are always dynamic in memory behavior.
- Size limits are logical; no stack-based arrays.
- **Mimicking stack behavior** is possible but not native.

---
Summary Table:

| Category            | C++ Example               | JS Equivalent Behavior        | Notes                         |
|---------------------|---------------------------|-------------------------------|-------------------------------|
| Fixed Stack Dynamic | `int arr[5];`             | `let arr = [1,2,3,4,5];`      | JS is not truly stack-based   |
| Stack Dynamic       | `int arr[size];`          | `new Array(size);`            | JS creates on heap            |
| Fixed Heap Dynamic  | `new int[5];`             | `new Array(5);`               | Both use heap                 |
| Heap Dynamic        | `std::vector<int>`        | `[] + push()`                 | Fully dynamic in both         |


Conclusion:
- **C++** gives fine-grained memory control via explicit stack/heap usage.
- **JavaScript** abstracts memory management but still offers dynamic allocation through its object model.
