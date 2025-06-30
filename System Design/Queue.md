*Queues serve as buffers for traffic or as a means of distributing work across a system.*
- A compute resource sends messages to a queue and forgets about them. On the other end, a pool of workers processes the messages at their own pace. 

==The Queue's function is smooth out the load on the system. If I get a spike of 1000 requests but can only handle 200 request per second, 800 requests will wait in the queue before being processed.==
- This also decouples the producer and consumer of a system, allowing you to scale them independently 

### Two Common Use Cases:
1. **Buffer for Bursty Traffic** - in a ride-sharing application like Uber, queues can be used to manage sudden surges in ride requests. During peak hours, ride requests can spike massively. A queue buffers these incoming requests, allowing the system to process them at a manageable rate without overloading the server
2. **Distribute Work Across a System** 

#### Most Common Queueing Tech:
- [[Kafka]] and [[SQS]] 