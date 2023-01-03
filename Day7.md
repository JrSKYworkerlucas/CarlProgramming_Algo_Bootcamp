# DAY7 | Hash Table Part Two 
## 1. [454. 4Sum II](https://leetcode.com/problems/4sum-ii/)
### Note:
- Note that the sum of `nums1[i] + nums2[j] = - (nums3[k] + nums4[l])`.
- Use hash map to record the result and times of `nums1[i] + nums2[j]`

## 2. [383. Ransom Note](https://leetcode.com/problems/ransom-note/)
### Note:


## 3. [15. 3Sum](https://leetcode.com/problems/3sum/)
### Note:
- Be careful the solution list should be distinct. That means a certain combination only show up once in the answer.
- Missing incremental logic causes time exceeded:
```
j, k = i + 1, len(nums)-1
	while j < k:
		sum_up = nums[i] + nums[j] + nums[k]
		if sum_up ==  0:
			ans.append([nums[i], nums[j], nums[k]])  # append the value not the index
			while nums[k - 1] == nums[k] and j< k:
				k -= 1
			while nums[j + 1] == nums[j] and j < k:
				j += 1

			# j and k should move after doing above action 
			j += 1
			k -= 1
                        
```

## 4. [18. 4Sum](https://leetcode.com/problems/4sum/)
### Note:
- The condition for index `b` :
```
for b in range(a+1, len(nums)):
	if nums[a] + nums[b] > target and nums[a] + nums[b] > 0:
	# here "> 0" is because maybe nums[a] + nums[b] still is a negative number
			break
	if b > a + 1 and nums[b] == nums[b - 1]:
			continue
```
- Cannot add the code below since the nagative target test case
```
if nums[0] > target:
	return ans
```
