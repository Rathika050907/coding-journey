📌 Problem: Stock Buy and Sell
🔗 Link: https://www.geeksforgeeks.org/problems/stock-buy-and-sell2615/0/

🚨 Problem Statement
You are given an array prices[] where prices[i] represents the price of a stock on the i-th day.
You can buy and sell the stock multiple times, but cannot hold more than one stock at a time.

🔹 Your task is to find all intervals where buying and selling would yield maximum profit.

📥 Input:
prices = [100, 180, 260, 310, 40, 535, 695]

📤 Output:
(0 3) (4 6)

✅ Approach 1: Greedy - Increasing Segments
🔍 Concept:

Buy at local minima (where price starts rising)

Sell at local maxima (just before price drops)

📌 Steps:
Start from the first day, loop till the last day:

Find the local minima (buy point): where next day's price is higher.

Then find the local maxima (sell point): where price stops increasing.

Save the (buy, sell) pair.

⏱️ Time Complexity: O(n)
🧠 Space Complexity: O(1) (excluding result list)
