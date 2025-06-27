

## 📌 Problem: **Minimize the Height Difference After Modifying Towers**

link:https://www.geeksforgeeks.org/problems/minimize-the-heights3351/0/

🔗 **Description:**
You are given an array `arr[]` of size `N` where each element represents the height of a tower.
You are also given a positive integer `K`.

🧾 For **each tower**, you **must perform exactly one operation**:

* Either **increase** its height by `K`, or
* **Decrease** its height by `K`

Your task is to **minimize the difference** between the **tallest and shortest** towers after all operations are applied.

---

## 🧠 Problem Insight

* You cannot leave any tower unchanged — **each must be either increased or decreased by `K` exactly once**.
* Heights cannot become **negative**, so decreasing a height that is `< K` is **invalid** and should be skipped.
* We're aiming to make the **range (max - min)** of the final array **as small as possible**.

---

## ✅ Approach: **Greedy + Sorting**

This is a classic greedy problem solved efficiently by **sorting** the array and checking various possible split points.

---

### 📌 Key Idea:

After sorting, try to decide for each index `i`:

* Towers **before or at i-1** will be increased by `K`
* Towers **from i onward** will be decreased by `K`

Then calculate:

* The **new minimum height** (`minH`) and
* The **new maximum height** (`maxH`)

Update the result as the **minimum difference** found so far.

---

### 📌 Step-by-Step:

1. **Sort** the array.
2. Initialize `res = arr[n-1] - arr[0]` — the original max difference.
3. Loop through `i = 1` to `n-1`:

   * Skip if `arr[i] - K < 0` (can't reduce below 0).
   * Compute:

     * `minH = min(arr[0] + K, arr[i] - K)`
     * `maxH = max(arr[i - 1] + K, arr[n - 1] - K)`
   * Update `res = min(res, maxH - minH)`
4. Return `res`.

---

### ⏱ Time Complexity: **O(n log n)**

(Due to sorting)

### 🧠 Space Complexity: **O(1)**

(Only variables used, no extra space)

---

## 📥 Example:

**Input:**
`arr = [1, 5, 15, 10]`, `K = 3`
**Output:**
`8`
**Explanation:**

* Modified array could be: `[4, 8, 12, 7]`
* Max = 12, Min = 4 → Difference = **8**

---

## ⚠️ Edge Cases:

* If `n == 1`, return 0.
* Skip any reduction that leads to negative height.
* Consider all valid partitions while minimizing the difference.


