📌 Problem: Maximum Product Subarray

🔗 Description:
You are given an array arr[] containing positive, negative, and zero integers.

🧾 Your task is to find the maximum product that can be obtained from a contiguous subarray of arr[].

🧠 Key Insight:
Unlike the maximum sum problem, this one needs careful handling of negative numbers and zeros.

A negative number can turn a small product into a large one when multiplied with another negative.

A zero resets the product.

✅ Approach: Kadane’s Variant for Products
This is a modified Kadane's Algorithm. We keep track of both:

maxProdSoFar: The maximum product ending at current position.

minProdSoFar: The minimum product ending at current position (in case it becomes positive later due to another negative number).

📌 Logic:
At each index i:

If arr[i] is negative, swap max and min.

Update:

maxProdSoFar = max(arr[i], maxProdSoFar * arr[i])

minProdSoFar = min(arr[i], minProdSoFar * arr[i])

Track the overall maximum product.

🔁 Step-by-Step:
Initialize:

maxProdSoFar = arr[0]

minProdSoFar = arr[0]

result = arr[0]

Loop from index 1 to n-1:

If current element is negative → swap maxProdSoFar and minProdSoFar

Update maxProdSoFar and minProdSoFar

Update result = max(result, maxProdSoFar)

Return result

📥 Example:
Input:
arr = [2, 3, -2, 4]
Output:
6
Explanation:
Subarray [2, 3] has the maximum product: 2 * 3 = 6

📥 Example 2 (With Zero):
Input:
arr = [-2, 0, -1]
Output:
0
Explanation:
All subarrays including negatives result in a product <= 0. The max is just 0.

⏱ Time Complexity: O(n)
One pass through the array.

🧠 Space Complexity: O(1)
Only variables used for tracking.
