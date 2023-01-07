# DAY11 | Stack and Array Part Two

## [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/submissions/)
### Note
- When meeting the left side of the parentheses `(, [, {`, append the right side of them `), ], }` into the recording list, can simplify the processing of matching judgement.

## [1047. Remove All Adjacent Duplicates In String](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string/description/)1047
### Note
-

## [150. Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/submissions/873136698/)
### Note
- Simplfy the processing through 
```stack.append(
      int(eval(f'{second_num} {item} {first_num}')))   # 第一个出来的在运算符后面
```


