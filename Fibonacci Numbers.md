Recurrence relation: $F_n = F_{n-1} + F_{n-2}$ for $n \geq 2$ and $F_0 = 0$, $F_1 = 1$

Basic:
```
F(n) {
	if n = 0 return (0)
	else if n = 1 return (1)
	else return F(n-1) + F(n-2)
}
```

Tabulation:

![[Screenshot 2025-05-22 at 1.24.02 PM.png|500]]

[[Recurrence Relation]]
