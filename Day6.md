# Day6 | The Basic of Hash Table 

## 1. [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
### Note
- If we need to solve a problem that requires a totally reversed sequence, hash table does not hold the water.
- The reason we can use hash table for this problem is because the order of the letters doesn't matter.

## 2. [349. Intersection of Two Arrays](https://leetcode.com/problems/intersection-of-two-arrays/)
### Note
- `if nums1[i] in nums2` can put in the first loop when taking down the record of nums1, so that we don't have to loop the nums2 again.
```
for i in range(len(nums1)):
	if nums1[i] in nums2:
		record[nums1[i]] = record.get(nums1[i], 0) + 1
```
instead of 
```
# problematic code
for i in range(len(nums1)):
	record[nums1[i]] = record.get(nums1[i], 0) + 1
for j in range(len(nums2)):
	if nums2[j] in record.keys() and nums2[j] not in ans:
		ans.append(nums2[j])
```

## 3. [202. Happy Number](https://leetcode.com/problems/happy-number/)
### Note:
- The key is to find out how to solve the cycle, or repetative answer.
- At first, I though if a num in the `record`, that means a cycle is formed, so all I need to do is just set a condition to jump out the loop when  a num in the `record`: `while add_up not in record:`. However, the code below will jump out at the first round. It cannot record anything! 
```
# problematic code
while add_up not in record:
	tmp_add_up = 0
	while add_up:
		tmp_add_up += (add_up % 10) ** 2
		add_up //= 10
	add_up = tmp_add_up
	record.append(add_up) 
```
- Then I change the code
```
while add_up != 1:
	tmp_add_up = 0
	while add_up:
		tmp_add_up += (add_up % 10) ** 2
		add_up //= 10
	add_up = tmp_add_up
	if add_up != 1 and add_up in record:
		break
	record.append(add_up)
```

## 4. [1. Two Sum](https://leetcode.com/problems/two-sum/)
### Note
- Remember what are keys and values in side the record dictionary.
- Keys in dictionary should be the scanned numbers in the list `nums`
- Values should be the index of the scanned numbers.
- Kind of like the kmp.

