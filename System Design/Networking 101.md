Networking is about connecting devices and enabling them to communicate
- Networks are built on a layered architecture (the "OSI Model") 
	- Network layers are just abstractions that allow us to reason about the communication of devices in simpler terms

![[Pasted image 20250624124859.png|600]]

**Network layer:** this layer is IP, the protocol that handles routing and addressing. It is responsible for breaking the data into packets, handling packet forwarding between networks, and providing delivery to any destination IP address on the network 

**Transport layer:** At this layer, we have [[TCP]], [[QUIC]], and [[UDP]], which provide end-to-end communication services. Think of them like a layer that provides features like reliability, ordering, and flow control on top of the network layer

**Application layer:** At the final layer are the application protocols like [[DNS]], [[HTTP]], [[Websockets]], [[WebRTC]]. These are common protocols that build on top of TCP (or UDP for WebRTC)


==Example of a simple web request==
![[Pasted image 20250624125852.png|700]]

First, we use [[DNS]] to convert a human-readable domain name like `joesluis.com` into an IP address like `32.42.52.62`. 