With long-polling, the client requests information from the server, but the server may not respond immediately. This technique is sometimes called **hanging GET**. If the server doesn’t have any available data for the client, it’ll hold the request and wait until there is data available instead of sending an empty response. Once the data becomes available, a full response is sent to the client. The client immediately re-requests information from the server so that the server will almost always have an available waiting request that it can use to deliver data in response to an event.

![[Screenshot 2025-06-11 at 3.52.08 PM.png]]


[[AJAX Polling]]
[[Websockets]]
[[Polling vs Server-sent events]]