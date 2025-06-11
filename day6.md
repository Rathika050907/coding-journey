Refined Problem Statement:
Given an array arr[], find all elements that appear more than n//3 times and return them in sorted order.

Approach (Hash Map):
Initialize:

count → an empty dictionary to store frequency of each number.

res → an empty list to store result.

Count Frequencies:

For each number num in arr, update the count:

python
Copy
Edit
count[num] = count.get(num, 0) + 1
Find Majority Elements:

Set majority = len(arr) // 3

For every num in the dictionary, if count[num] > majority add it to res
link:

https://www.geeksforgeeks.org/problems/majority-vote/0/
