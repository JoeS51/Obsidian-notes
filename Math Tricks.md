```python
for j in range(1, int(num ** 0.5) + 1):
```
When you're finding divisors you dont have to loop up until the number you can loop up until it's square value plus one and check the two pairs in this loop

When finding divisors:
- if j is the divisor of num, then num // j is the paired divisor
- Example: if `12 % 3 == 0`, then `12 // 3 == 4`, so both `3` and `4` are divisors.
The largest smaller factor you ever need to check is **√num** because:
- Past that, you’re just flipping the pair (you already checked the smaller half).