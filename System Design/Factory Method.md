###### Also known as Virtual Constructor
## Intent
Factory Method is a creational design pattern that provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created*
## Problem
Imagine that you are creating a logistics management app, and the first version of your app can only handle transportation by trucks, so the bulk of your code lives in the `Truck` class.

After a while, your app becomes popular, and you receive requests from sea transportation companies to incorporate them into your app. 

At present, most of your code is coupled to the `Truck` class so adding `Ships` into the app will require making changes to the entire codebase. As a result, your code will end up being riddled with conditionals that switch the app's behavior based on which vehicle it is.

## Solution
The factory method pattern replaces direct object construction calls with calls to a special factory method. 
- The objects are still created via the `new` operator, but it's being called from within the factory method. 
	- Objects returned by the Factory method are often called *products*

![[Screenshot 2025-05-16 at 12.48.24 PM.png|400]]

Limitation: subclasses may return different types of products only if these products have a common base class or interface

The code that uses the factory method (client code) doesn't see a difference between the actual products returned by various subclasses. The client treats all the products as abstract `Transport`. The client knows that all transport objects are supposed to have a `deliver` method, but exactly how it works isn't important to the client.

![[Screenshot 2025-05-16 at 1.03.25 PM.png|700]]

Reference: https://refactoring.guru/design-patterns/factory-method