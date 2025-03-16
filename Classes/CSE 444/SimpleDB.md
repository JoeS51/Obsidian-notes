SImpleDB consists of:
- classes that represent fields, tuples, and tuples schemas
- classes that apply predicates and conditions to tuples
- one or more access methods that store relations on disk and provide a way to iterate through tuples of those relations
- a collection of operator classes (e.g. select, join, insert, delete, etc.) that process tuples
- a buffer pool that caches active tuples and pages in memory and handles concurrency control and transactions
- a catalog that stores information about available tables and their schemas
- Don't have to order relations as that's expensive

- only has strings and ints
- SimpleDB not designed to be bullet-proof software

Tuple = row


**[[BufferPool]]**
- bridge between operators and data files

**[[OpIterator]]**
- Ancestor class for all operators

**[[HeapFile]]**
- Main class that organizes the physical storage of tables
- Collection of HeapPages
	- one HeapFile per table

**[[HeapPage]]**
- Chunk of data that resides in BufferPool
- Format:
	- Header + Tuples
	- Header: # of 1 bits in Bitmap = # of active tuples on page

Types:
- int 
	- Type.INT_TYPE
	- 4 bytes
- Strings
	- Type.STRING_TYPE
	- 128 bytes


![[Pasted image 20250110104516.png]]