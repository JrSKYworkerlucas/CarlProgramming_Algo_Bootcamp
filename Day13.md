# DAY13 | Priority Queue
## [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
### Note
- Use min top heap to solve this quesiton. Why min top? If we use `heappop()`, the data structure will keep `K` numbers inside, the one deleted will have less frequency.
- Why heap? Heap is a priority queue in fact. In this problem, we need to maintain `K` numbers in the heap. So that we have no need to sort `n` numbers, which reducing the time complexity.

## [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/description/)
### Note
- Use priority queue to keep the largest and second largest numbers.
