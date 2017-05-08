##Memory Management

### Java

Java does automatic memory management which is implemented via garbage collection.
- Garbage collection is the process of looking at heap memory, identifying unused object or unreferenced object, and deleting them.
	- Advantage
		- It removes the burden of manual memory allocation/deallocation.
	- Disadvatage
		- It effects the performance of the application.


### Swift

- Swift uses Automatic Reference Counting (ARC) to track and manage the memory usage. 
- In most cases, ARC allows users to not think about memory management, it automatically frees up the memory used by class instances when those instances are no longer needed.