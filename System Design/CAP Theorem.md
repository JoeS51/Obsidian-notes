### CAP = **Consistency**, **Availability**, **Partition Tolerance**

It says:
> In a distributed system, **you can only guarantee two out of the three**.

##### Definitions:
- **Consistency (C)**: All nodes see the same data at the same time. (like a single source of truth)
- **Availability (A)**: Every request gets a (non-error) response, even if it's not the most recent.
- **Partition Tolerance (P)**: The system continues to operate even if network partitions (failures between nodes) occur.

In a system design interview, availability should be your default choice. You only need strong consistency in systems where reading stale data is unacceptable.

Examples of systems that require strong consistency include:

- Inventory management systems, where stock levels need to be precisely tracked to avoid overselling products
    
- Booking systems for limited resources (airline seats, event tickets, hotel rooms) where you need to prevent double-booking
    
- Banking systems where the balance of an account must be consistent across all nodes to prevent fraud