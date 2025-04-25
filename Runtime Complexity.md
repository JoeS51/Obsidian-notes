- Graphs:
	- DFS is O(N+E)
		- where n is node and e is edges
		- there can be n^2 edges in a graph so that ends up being
			==- O(N+N^2) = O(N^2) worst case== 

- Recursion: the spacetime complexity is calculated by how far down the stack goes

**Recursion runtime complexity**:
1. How many times does the recursive function get called?
	1. in DFS it is O(n) because each node is visited once
2. How much work is done per call?
	- constant work versus looping
then you multiply these two together






for DFS:
![[Screenshot 2025-04-11 at 1.01.23 AM.png]]