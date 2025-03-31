```python 
num = value you want
l, r = 0, len(arr)
while l < r:
	mid = (l + r) // 2
	if arr[mid]	== num:
		return mid
	elif arr[mid] > num:
		r = mid - 1
	else:
		l = mid + 1
return -1 #it was not present
```



