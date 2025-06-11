**“What choices does a distributed system have when there are no network partitions?”**
The PACELC theorem answers this question.

The PACELC theorem states the following about a system that replicates data:
- `if statement`: A distributed system can tradeoff between availability and consistency if there’s a partition.
- `else statement`: When the system normally runs without partitions, the system can tradeoff between latency and consistency.

![[Screenshot 2025-06-11 at 3.42.59 PM.png]]