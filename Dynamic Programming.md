





*General Notes:*
- don't use nonlocal variable if youre doing some count or keeping track of a value
	- @cache makes it so that you aren't performing side effects like `count += 1`
	- so you need to return a value instead and them together like this:
```python
class Solution:
    def climbStairs(self, n: int) -> int:
        @cache
        def dp(n):
            if n == 0:
                return 1
            if n < 0:
                return 0
            return dp(n-1) + dp(n-2)
        return dp(n)
```
