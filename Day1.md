# Day 1 | Binary Search and Two Pointers
## 1. Binary Search 
[Leetcode No.704 Binary Search](https://leetcode.com/problems/binary-search/) 


Note:
- Be careful of the condition of Binary Search: 1) a sorted list; 2) all the numbers are unique.
- Keep in mind that which search method you use, 1)left closed and right opened or 2)both sides are inclusive.
- Different method decides different loop: `while left < right` or `while left <= right`.
- The key to specify the search interval is making sure that the moved border should absolutely excludes the old elements. 

## 2. Two Pointers 
[Leetcode No.27 Remove Element](https://leetcode.com/problems/remove-element/)


Carl shows three way to solve this problem: 
  1) Rude method, double layers loops. 
  2) Two Pointers, normal solution. 
  3) Two face-to-face pointer, since this problem not require the result order as same as the original list.

Two pointer is a common method when decreasing the Time Complecity.
