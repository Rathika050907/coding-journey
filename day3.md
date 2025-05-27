📅 Date: 27/05/2025
📘 Topic: Arrays – Reverse an Array
🧠 Problem Statement:
Reverse a given array in-place (i.e., without using extra space for another array).

🔗 Problem Link:
https://www.geeksforgeeks.org/problems/reverse-an-array/0/

💡 Approach: Two-Pointer Method
Initialize two pointers:

left starting at index 0.

right starting at index len(arr) - 1.

Swap the elements at the left and right pointers.

Move:

left pointer towards the right (left += 1).

right pointer towards the left (right -= 1).

Repeat this process until left >= right.

Once the pointers cross, the array is fully reversed.

