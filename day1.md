# Day 24/05/2025

## 🚀 Started: 160 Days Coding Workshop by GeeksforGeeks (GFG)

### 📘 Topic: Working with Arrays

---

### ✅ Problem 1: Finding the Second Largest Element in an Array
🔗 [Problem Link – GFG](https://www.geeksforgeeks.org/problems/second-largest3735/0/)

#### 💡 Approach:
- Initialized `largest` and `second_largest` as negative infinity (`-inf`).
- Iterated through each element of the array:
  - If the element is greater than `largest`, then update `second_largest` as `largest`, and then `largest` as the current element.
  - If the element is not equal to `largest` and is greater than `second_largest`, update `second_largest`.
- This ensures both:
  - No duplicates in largest and second largest.
  - `second_largest` always remains below `largest`.

#### 🧠 Key Learning:
- Need to handle duplicate elements and ensure `second_largest` is not the same as `largest`.
- Edge cases like all elements being equal must be handled.

---

### 📅 Plan for Tomorrow:
- Continue with more array problems.
- Try edge cases and explore different test inputs.

