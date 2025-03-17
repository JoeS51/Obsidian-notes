for i in range(5):

my_list = ['a', 'b', 'c']  
for index, value in enumerate(my_list):  
	print(f"Index: {index}, Value: {value}")

lambda function in python is like an inline function

```
list = [3, 1, 2, 4]
sorted(list)
# list becomes 1 2 3 4
```

`sorted(list, key = lambda x: d[x], reverse = True`

**To sort on keys in a dict**
`sorted(map.keys())`

To return a string based off a list:
`"".join(list)`


`Counter()`
- this method counts the occurrences of elements in an iterable 
==Example==
```
s = "aabbbcc"
count = Counter(s)
print(count)

# { 'b': 3, 'a': 2, 'c': 2}
```