### CAP = **Consistency**, **Availability**, **Partition Tolerance**

It says:
> In a distributed system, **you can only guarantee two out of the three**.

##### Definitions:
- **Consistency (C)**: All nodes see the same data at the same time. (like a single source of truth)
- **Availability (A)**: Every request gets a (non-error) response, even if it's not the most recent.
- **Partition Tolerance (P)**: The system continues to operate even if network partitions (failures between nodes) occur.