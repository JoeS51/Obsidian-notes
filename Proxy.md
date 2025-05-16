## Intent
*Proxy is a structural design pattern that lets you provide a substitute or placeholder for another object.  A proxy controls access to the original object, allowing you to perform something either before or after the request gets through to the original object.*

## Problem
Why would you want to control access to an object?
**One example:** you have a massive object that consumes a vast amount of system resources. You need it from time-to-time but not all the time. You could implement lazy initialization: create this object only when it’s actually needed. All of the object’s clients would need to execute some deferred initialization code. Unfortunately, this would probably cause a lot of code duplication.

## Solution
The proxy pattern suggests that you create a new proxy class with the same interface as an original service object. Then you update your app so it passes the proxy object to all of the original object's clients
![[Screenshot 2025-05-16 at 1.16.26 PM.png|500]]

If you need to execute something either before or after the primary logic of the class, the proxy lets you do this without changing that class. Since the proxy implements the same interface as the original class, it can be passed to any client that expects a real service object.

**Real-world analogy**:
- A credit card is a proxy for a bank account which is a proxy for a bundle of cash. Both implement the same interface: they can be used for making a payment. A consumer feels great because there’s no need to carry loads of cash around.

