- [[SimpleDB]] uses the [[Ant Build Tool]] to compile the code and run tests
- For Lab1, we do not need to implement any operators (select, join) except sequential scan

- ==ant test ==
	- runs all unit tests
- ==ant runtest -Dtest=TupleTest==
	- runs a specific unit test

**Part 1**
- Implement the classes to manage tuples: Tuple.java and TypleDesc.java
	- Tuples consist of a collection of *Field* objects
	- *Field* is an interface that different data types implement
	- Tuples also have a type (or schema) called a *Tuple descriptor*
		- consists of a collection of Type objects, one per field in the tuple

**Part 2**


*Database class*
- provides access to a collection of static objects that are the global state of the database
- Includes methods to access:
	- the catalog (the list of all tables in the db)
	- the buffer pool (the collection of db file pages that are currently resident in memory)
	- log file