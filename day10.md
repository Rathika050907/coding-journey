📌 Problem: Maximum Subarray Sum
link:
https://www.geeksforgeeks.org/problems/kadanes-algorithm-1587115620/0/
🔗 Description:
You are given an integer array arr[].
Your task is to find the maximum sum of a contiguous subarray within arr[].

🧾 What is a Subarray?
A subarray is a sequence of consecutive elements from the array.
Example: For arr = [-2, 1, -3, 4, -1, 2, 1], subarrays include [4, -1, 2, 1], [-2, 1], etc.

🧠 Goal:
Find a subarray (contiguous) that has the maximum sum, and return that sum.

✅ Approach: Kadane’s Algorithm
Kadane’s Algorithm is an efficient way to solve this in O(n) time using a single pass through the array.

📌 Intuition:
As we go through each element:

We keep adding elements to a running sum (maxend).

If the current element is better on its own than continuing the current subarray, we start fresh from it.

At each step, we update a global result (res) if the current subarray sum is the best seen so far.

🔁 Step-by-Step:
Initialize:

maxend = arr[0] → current subarray sum

res = arr[0] → overall maximum found so far

Loop from index 1 to end:

Update current subarray: maxend = max(arr[i], maxend + arr[i])

Update result: res = max(res, maxend)

Return res

⏱ Time Complexity: O(n)
Single traversal of the array.

🧠 Space Complexity: O(1)
Only constant extra space used.

📥 Example:
Input:
arr = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
Output:
6
Explanation:
The subarray [4, -1, 2, 1] has the maximum sum 6.
