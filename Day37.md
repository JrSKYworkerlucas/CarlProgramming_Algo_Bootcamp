# DAY37 | Greedy Part Three

## [1005. Maximize Sum Of Array After K Negations](https://leetcode.com/problems/maximize-sum-of-array-after-k-negations/description/)
### Note:
- Take two step to solve this problem. 
- The 1st step: How can we make the result as big as possible? Try to change negative nubmbers into positive as many as possible and also change the smaller negative numbers at fitst.
- The 2nd step: If 'the change time' less than `k`, which means we have `k - the change time` left to convert number. We need to convert the smallest number.

## [134. Gas Station](https://leetcode.com/problems/gas-station/description/)
### Note:
- Notice that the sum of `gas` must be greater than or equal to the sum of `cost`.

## [135. Candy](https://leetcode.com/problems/candy/description/)
### Note:
- Take two times iteration to solve this problem. 
- At the first iteration, make sure that the kid on the right get more candy than its left.
- At the second iteration, make sure that the kid on the left get more candy than its right.
- Don't combine this two situation within one iteration, it would be puzzling.
