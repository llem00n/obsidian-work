- Move VirtualNodeManager from the ConfigurationControl project to a new one (NodeRuntime, for instance).
	***Reason***
	- ConfigurationControl depends on Infragistics DLLs, which are not required for VirtualNodeManager
	**Solution***
	- Create a new project with the minimal set of dependencies (the Information project is the only one required)
- 