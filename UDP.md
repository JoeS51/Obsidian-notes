**Key characteristics of UDP**:
1. Connectionless: No handshake or connection setup
2. No guarantee of delivery: Packets may be lost without notification
3. No ordering: packets may arrive in a different order than sent
4. Lower latency: less overhead means faster transmission 

*Perfect for applications where speed is more important than reliability, such as live video streaming, online gaming, etc.*
- In these cases, the application is equipped to handle the occasional packet loss

*Note: browsers don't have widespread support for UDP yet outside of WebRTC, so web apps might need slower, batched HTTP stream over mobile app*