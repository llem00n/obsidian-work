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
	- Limited support of .NET Framework ([Use gRPC client with .NET Standard 2.0 | Microsoft Learn](https://learn.microsoft.com/en-us/aspnet/core/grpc/netstandard?view=aspnetcore-8.0#net-framework))
- Use CoreWCF library.
	Pros:
	- Minimal code update
	- Full support of both .NET and .NET Framework
	Cons:
	- Does not have the ServiceHost class implementation, so, rewrite is still required
###### ❓Application Domains are not supported in .NET5+

###### ❓Check if workflows start ServiceHost

## notes

#### required DLLs
- savigent.platform.workflow.dll

#### TODO comments
- ***NET8-Upgrade*** - all comments, created during .NET 8 upgrade initiative
- ***NET8-Upgrade-TODO*** - todo items, created during .NET 8 upgrade initiative
- ***NET8-Upgrade-NOTE*** - notes, created during .NET 8 upgrade initiative
- ***WCF-NET8-Upgrade*** - all comments related to WCF -> CoreWCF upgrade, created during .NET 8 upgrade initiative
- ***WCF-NET8-Upgrade-TODO*** - todo items related to WCF -> CoreWCF upgrade, created during .NET 8 upgrade initiative
- ***WCF-NET8-Upgrade-NOTE*** - notes related to WCF -> CoreWCF upgrade, created during .NET 8 upgrade initiative
- ***AD-NET8-Upgrade*** - all comments related to Active Directory, created during .NET 8 upgrade initiative
- ***AD-NET8-Upgrade-NOTE*** - notes related to Active Directory, created during .NET 8 upgrade initiative
- ***AD-NET8-Upgrade*** - all comments related to Active Directory, created during .NET 8 upgrade initiative
- ***Olek-...*** my comments / todo items / notes
- ***NET8-Upgrade-TODO: Uncomment this once ...*** - TODO's that should be automatically resolved my upgrading projects to .NET 8