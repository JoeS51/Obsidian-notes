![[Pasted image 20250625220754.png]]

- When horizontal scaling is the right solution, you'll need to think about how to distribute work across your machines. 
	- Most modern systems use a technique called [[Consistent Hashing]] to distribute work across a set of machines
	- A challenge of horizontal scaling is getting the work to the right machine. This is often done via a load balancer. (simple round robin allocation is often sufficient)
		- Work distribution needs to try to keep load on the system as even as possible