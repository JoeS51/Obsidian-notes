- some sliding window problems require you to increase right pointer until you meet the constraint like this [question](https://leetcode.com/problems/count-complete-subarrays-in-an-array/description/)

- Other questions like this [one](https://leetcode.com/problems/count-subarrays-with-score-less-than-k/description/) where the constraint becomes better as it becomes smaller usually require you to increment right pointer incrementally and left in a while loop. 
	- the while loop condition should increase until the condition is met not while the condition is not met
 	
![[Screenshot 2025-04-28 at 2.09.44 PM.png]]