# Day4 | Linked List Intermediate 

## 1. [24. Swap Nodes in Pairs](https://leetcode.com/problems/swap-nodes-in-pairs/)
### 1.1 Note:
- I use three pointers at the begining (pre, cur, rear), but a problem occurs after the interchange. The `rear` will point to `None.next`. So DON'T USE THREE POINTERS.
- The merit of using only one pointer is that you can simplfy the logic condition.
- Remeber to reset `head` of the linked list.

## 2. [19. Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)
### 2.1 Note:
- A classic problem of Two Pointers.
- 1) Move the fast pointer to the n podition; 2) Then move the fast and slow pointers together, 3) owing to the dummy head, the slow pointer will stop on the previous position of n, link the `slow` node and the `slow.next.next` node.

## 3. [160. Intersection of Two Linked Lists](https://leetcode.com/problems/intersection-of-two-linked-lists/)
### 3.1 Note:
- You can eliminate some `if` loop by exchanging two headers: 
```
a_cur, b_cur = headA, headB
if len_a < len_b: # assign the longer one to a_cur and len_a
    len_b, len_a = len_a, len_b
    b_cur, a_cur = a_cur, b_cur
# now the "a" is the longer one 
```

## 4. [142. Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)
### 4.1 Note:
- [Deduct the process by yourself.](https://programmercarl.com/0142.%E7%8E%AF%E5%BD%A2%E9%93%BE%E8%A1%A8II.html#_142-%E7%8E%AF%E5%BD%A2%E9%93%BE%E8%A1%A8ii)
- Once you understand the deduction of entrance, coding will be easy.

