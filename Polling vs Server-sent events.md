==Polling==
- The client periodically sends requests to the server at regular intervals (e.g., every 5 seconds) to check if there's new data.
- simple to implement
- inefficient to implement

==Server-sent events==
- The client establishes a single, long-lived HTTP connection to the server and the server pushes new updates over this connection when available, in real-time
- Low latency: Updates are delivered as soon as they occur.