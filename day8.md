📌 Problem: Maximum Profit with At Most One Transaction
link:https://www.geeksforgeeks.org/problems/buy-stock-2/0/
🔗 Problem Description:
You are given an array prices[] of length n, where prices[i] represents the price of a stock on the i-th day.

🧾 Your goal is to find the maximum profit you can make from a single buy-sell transaction.
A valid transaction is:

Buy the stock on some day i

Sell the stock on a later day j (i < j)

If no profit is possible, return 0.

📥 Example:
Input:
prices = [7, 1, 5, 3, 6, 4]

Output:
5
Explanation:
Buy at 1 (day 1), sell at 6 (day 4) → profit = 6 - 1 = 5

✅ Approach: One Pass — Track Minimum Price So Far
This is an optimal greedy approach using a single pass through the array.

📌 Logic:
Keep track of the minimum price seen so far (MinSoFar).

At each day, calculate:

Profit if you sold today → prices[i] - MinSoFar

Update the maximum profit if it's higher than the previous best.

Also, update MinSoFar if the current price is lower.

🔁 Step-by-Step Process:
Initialize:

MinSoFar = prices[0]

maxProfit = 0

For every day from index 1 to n-1:

Update MinSoFar = min(MinSoFar, prices[i])

Calculate profit: prices[i] - MinSoFar

Update result: maxProfit = max(maxProfit, prices[i] - MinSoFar)

Return maxProfit

⏱ Time Complexity: O(n)
Only one loop through the array.

🧠 Space Complexity: O(1)
Only constant extra space used.

⚠️ Edge Cases:
If prices are in decreasing order → No profit possible → Return 0
Example: [9, 7, 4, 2] → Output: 0

Minimum length must be at least 2 to have a valid buy/sell.
