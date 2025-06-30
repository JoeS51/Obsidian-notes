**Definition:**
The transport layer is where we establish end-to-end communication between applications. They give us some guarantees instead of handing us a jumbled mess of packets. 

==The three primary protocols at this layer are [[TCP]], [[UDP]], and QUIC==

*UDP:*
- Fast but unreliable
- *Spray and pray*
- It provides a simpler, connectionless service with no guarantees of delivery, ordering or duplicate protection
- All you can see are:
	- where they came from (the source IP address and port)
	- where they're going (the destination IP address and port)

