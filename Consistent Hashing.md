==*this is a technique that arranges both data and machines in a circular space called a "hash ring", allowing you to add or remove machines with minimal data redistribution.*==

A really interesting concept to fix the problem with hashing with the amount of servers you have. When you remove a server or add a new server, the hashing function all of a sudden becomes different so all the data in all the servers needs to be moved around. Consistent hashing fixes this by using a ring (the implementation details are not here but probably not important for sys design)

- Redis, Cassandra, DynamoDB, Many CDNs all use consistent hashing


![[Pasted image 20250625221913.png|700]]
![[Pasted image 20250625221850.png|700]]