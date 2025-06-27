📌 Problem: Find the Smallest Positive Missing Number
link:
https://www.geeksforgeeks.org/problems/smallest-positive-missing-number-1587115621/0/

🔗 Description:
You are given an array arr[] of integers, which can include positive, negative, and zero values.

Your task is to find the smallest positive number (≥ 1) that is not present in the array.

📥 Example:
Input:
arr = [0, -10, 1, 3, -20]
Output:
2
Explanation:

Positive numbers present: 1, 3

Smallest missing positive is 2.

✅ Approach: Sorting-Based Greedy Check
This solution uses sorting and incremental comparison to find the missing positive number.

📌 Logic:
Sort the array to bring positive numbers in increasing order.

Initialize a counter res = 1 → the first positive number we’re looking for.

Loop through the sorted array:

If current number == res, it means res is found, so increment res.

If current number > res, it means res is missing — so return it.

If current number < res, continue (since we ignore negatives or duplicates).

After the loop, return res.

🔁 Dry Run Example:
Input: arr = [3, 4, -1, 1]
Sorted: [-1, 1, 3, 4]

res = 1

-1 → skip

1 == res → res = 2

3 > res → return 2 ✅

⏱ Time Complexity:
Sorting: O(n log n)

Scan Loop: O(n)

Total: O(n log n)

🧠 Space Complexity:
O(1) (in-place sorting assumed, no extra data structures used)
