 Concept: Next Permutation
This algorithm finds the next lexicographically greater permutation of a sequence of numbers (like how 1243 comes after 1234).

🔍 Steps (Cleaned-up version of your approach):
Find the Pivot:

Traverse the array from right to left.

Find the first index i where nums[i] < nums[i + 1].

This is the pivot (the point where the descending order breaks).

Find the Successor:

Again, traverse from the right and find the smallest element greater than the pivot (nums[i]), say at index j.

Swap:

Swap nums[i] and nums[j].

Reverse the Suffix:

Reverse the sub-array from i + 1 to the end. This ensures the smallest lexicographical order for that suffix.

🧠 Example
Input: [1, 2, 3]

Pivot: 2 (at index 1)

Successor: 3 (at index 2)

Swap → [1, 3, 2]

Reverse suffix (already in order) → [1, 3, 2]

✅ Output: [1, 3, 2]
link:
https://leetcode.com/problems/next-permutation/description/
