# DAY8 | The String
## 1. [344. Reverse String](https://leetcode.com/problems/reverse-string/description/)
### Note
- This is not meaningful if you use `str.reverse` to solve this problem.
- Think about `len(s)` is odd or even, would it affect your code? 

## 2. [541. Reverse String II](https://leetcode.com/problems/reverse-string-ii/)
### Note
- The right way to use `[::-1]`
```
ts = 'happy'
# the wrong code
ts[1:4:-1] # return a empty string: ''
# correct code
ts[1:4][::-1] # return 'ppa'
```
- An important feature: If you use `str[i:j]`, even `j` exceede the length of string, there is no any problems.
```
ts = 'happy'
ts[1:60] 
# return 'appy'
```

## 3.[剑指 Offer 05. 替换空格](https://leetcode.cn/problems/ti-huan-kong-ge-lcof/)
### Note
- The length of the string may change!!
- When using two pointers, notice that the movement of `new_tail`. Move it carefully 

## 4.[151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)
### Note
- When reversing the word in the middle, be careful about the redundant space between the words.
```
# forget to eliminate the redundant space inside the str(s)
elif s[j+1] == ' ':# reverse the word, and then both i and j jump into next word
    s = s[:i] + s[i:j+1][::-1] + s[j+1:]
    i = j
    '''
    # didn't skip the extra space
    i += 2
    j += 2
    '''
    '''
    # comes a problem that the length of string will change !!!! the biggest problem of this question
    while s[j+1] == ' ': # eliminate the redundant space 
            j += 1
    s = s[:i+1] + s[j:]
    i = j 
    '''
```
```
# a more succinct and correct code 
elif s[j+1] == ' ':# reverse the word, and then both i and j jump into next word
    s = s[:i] + s[i:j+1][::-1] + s[j+1:]

    j += 1 # now s[j] is a ' ' space
    while s[j + 1] == ' ': # bridge the gap between two words
        s = s[:j] + s[j+1:]

    # reset i and j 
    j += 1
    i = j
```

## 5.[剑指 Offer 58 - II. 左旋转字符串](https://leetcode.cn/problems/zuo-xuan-zhuan-zi-fu-chuan-lcof/submissions/)
### Note
- A funny way to subtract the string
```
def reverseLeftWords(self, s: str, n: int) -> str:
    new_str = ''
    for i in range(len(s)):
        j = (i+n) % len(s)  # Using mod is a new method to me. I should remember this. 
        new_str += s[j]

return new_str
```
