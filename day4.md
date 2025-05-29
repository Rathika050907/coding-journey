📌 Problem: Rotate Array to the Left by d Positions
Date: 28/05/2025
Link: https://www.geeksforgeeks.org/problems/rotate-array-by-n-elements-1587115621/0/

🚨 Problem Statement
Rotate an array of size n to the left by d positions.

Example:
Input:  arr[] = [1, 2, 3, 4, 5], d = 2  
Output: [3, 4, 5, 1, 2]
✅ Approach 1: Juggling Algorithm
Concept: Use the GCD of n and d to identify the number of sets.

Process:

Compute gcd(n, d)

For each cycle, shift elements by d positions.

Time Complexity: O(n)

Space Complexity: O(1)

✅ Approach 2: Reversal Algorithm
Concept: Reverse parts of the array in three steps.

Steps:

Reverse the first d elements.

Reverse the remaining n - d elements.

Reverse the entire array.

Time Complexity: O(n)

Space Complexity: O(1)
