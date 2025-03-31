basically you want to find the largest distance between arrays and it cant be within the same array

so like ((1,2), (3,4))

1 and 4 would make the largest distance

- greedy problem
- can also be a heap problem
	- there's a cool trick here: you add all the values to a min heap and max heap and at the end you don't want them to be a part of the same array so you check the index of min_heap and max_heap values and if they're the same then store them for now and get the next values. the max distance will either be the old min and the new max or old max and the new min
