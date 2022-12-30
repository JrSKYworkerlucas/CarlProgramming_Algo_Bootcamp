# DAY3 | The Basic of Linked List
## 1. [203. Remove Linked List Elements](https://leetcode.com/problems/remove-linked-list-elements/)
### 1.1 Note
- Use a dummy head is a efficient to manipulate all the linked node in a same way.
- You can use only one pointer to solve this problem, be careful about the condition.

## 2. [707. Design Linked List](https://leetcode.com/problems/design-linked-list/)
### 2.1 Note
- Read the requirement carefully
- Keep in mind that the index may be equals to 0, coding the loop condition accordingly and accurately
- Use established built-in function again if needed

## 3. [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
### 3.1 Note
- Two solutions: 1)Two Pointers and 2) Recursion
- When using Two Pointer, note that the slower pointer should be `None` at first. If not, there will be a cycle in the LinkedList.(The first node will point to the second node, and then the second node will point to the first one. Here is the cycle.)
- When using Recursion, remember the three step to create a correct recursion: 1)the parameters; 2)the ending condition; 3)the execution inside the recursion.
