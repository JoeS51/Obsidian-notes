Ant to compile code and run tests for simpleDB


- ==ant test ==
	- runs all unit tests
- ==ant runtest -Dtest=TupleTest==
	- runs a specific unit test
- ==ant -projectHelp==
	- list all the targets in build.xml with descriptions
- ==ant dist==
	- compile the code in src and package it in dist/simpledb.jar
- ==ant systemtest==
	- compile and run all the system tests