## people
###### Clint Myhre
A guy who converted all projects in the Platform to .NET SDK format

###### Ranjit Kancheria
No idea who that is, really

###### Jeremy Johnson
Product owner, the most important guy in symphony so far

## questions
###### ❓ Should I translate Class Libraries to .NET standard 2.0 instead of .NET 8? 
This way the library will stay compatible with both .NET framework 4.7.1 and .NET 8

###### ❓Platform uses WCF for Communication, which is not supported in .NET Core.
Possible solutions:
- Rewrite the communication with gRPC. 
	Pros:
	- Improved performance
	Cons:
	- It will take ages to implement
- Use CoreWCF library.
	Pros:
	- Minimal code update
	Cons:
	- Community-driven library (could be unstable)
	- 