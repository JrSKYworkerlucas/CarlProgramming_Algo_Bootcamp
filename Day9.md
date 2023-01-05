# DAY9 | KMP Searching Method
## 1. [28. Find the Index of the First Occurrence in a String](https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/)
### Note
- Be careful that the pointer you used when searching the `needle` string cannot be the same as the index of `prefix` array.
```
# Wrong code. Always start matching at the same place, no meaning 
prefix, i, j =[-1]*len(needle), -1, 0
while j < len(needle):
    if needle[j] == needle[i+1]: # The problem is over here. j should start from 1 here
        prefix[j] = i  
        i += 1
        j += 1
```
- Make clear that what are `i`, `j`, and the `prefix` array indicate;
- The value in `prefix` array shows that if you mismatch at the `k` position of the`needle`, you should restart your process from `prefix[k]`. That's to say, the value indicates a "restart matching position" .
- I should review this problem every day until I can fluently instruct others. May be I can put two steps into one. 


## 2. [459. Repeated Substring Pattern](https://leetcode.com/problems/repeated-substring-pattern/description/)
### Note
- Also use KMP. There is another method I should try.
