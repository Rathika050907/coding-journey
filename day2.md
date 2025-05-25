# Day 25/05/2025

## 📘 Topic: Arrays – Continued

---

### ✅ Problem: Move All Zeroes to the End of the Array
🔗 [Problem Link – GFG](https://www.geeksforgeeks.org/problems/move-all-zeroes-to-end-of-array0751/0/)

#### 💡 Approach:
- Initialize a `count` variable to track the position where the next non-zero element should go.
- Traverse the array:
  - If the current element is **non-zero**, swap it with the element at `arr[count]` and increment `count`.
- This ensures all non-zero elements are moved to the front, and zeroes are shifted to the end.
- Finally, iterate through the array and print the updated values.

#### 🧠 Key Learnings:
- Efficient **in-place swapping** using a single pass.
- The `count` pointer acts as a tracker for the next position to place non-zero values.
- No need for extra space – optimized for time and space.

---

### 📅 Plan for Tomorrow:
- Continue practicing array-based problems.
- Try variations with sorting and rearranging elements.
