# DAY2 | Still Two Pointers in Array
## 1. [Leetcode No.977 Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)

### 1.1 Note
- Use two face-to-face pointer can elimate the time of sorting in this problem. 
### 1.2 Mistake 
- When writing the reversed for loop `for i in range(xx,yy,-1)`, make sure that the number `xx` is the bigger one, and the `yy` is the small one.


## 2. [Leetcode No.209 Minimun Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/submissions/)
### 2.1 Note
- Make sure you are clear that how these two pointers move. In what situation you need to move the fast one? In what situation you need to move the slow one?
- Move the fast one: if the sum of numbers between faster pointer and slower pointer is not exceed the target.
- Move the slow one: if the sum of numbers between faster pointer and slower pointer is greater than the target.
