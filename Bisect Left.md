``` python
def bisect_left(arr, target):
	l, r = 0, len(arr)
	while l < r:
		mid = (l + r) // 2
		if arr[mid] < target:
			l = mid + 1
		else:
			r = mid
	return l
```
This finds the left most index where you can insert target or if target is in arr then the leftmost occurrence of target

- the condition ends when l == r
- you want to make r = len(arr) because you could be inserting it at the end of the array