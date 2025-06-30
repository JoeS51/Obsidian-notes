*An API Gateway sits in front of your system and is responsible for routing incoming requests to the appropriate backend service*
- For example, if the system receives a request to `GET /users/123`, the API gateway would route that request to the `users` service and return the response to the client
- The gateway is also typically responsible for handling authentication, rate limiting, and logging

Most common API Gateways are [[AWS API Gateway]], [[Kong]], [[Ngnix]], [[Apache webserver]]

==In nearly all product design system design interviews, it is a good idea to include an API gateway as the first point of contact for your clients==

![[Pasted image 20250629203125.png|700]]