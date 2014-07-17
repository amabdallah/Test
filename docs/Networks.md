Networks
========

A networks in WaM-DaM defiens the topolog "connectivity" between nodes and links of a water system. The networks table contain the node and link instances within a project, their connectivity, and scenarios that in which they appear. 

An instance is a specific implementation of an object defined in the project metadata table. For example an instance of the object “Reservoir” is Hyrum reservoir in Utah. A node instance can stand by itself but a link instance references a start and end node. The connectivity between node and links instances represents the spatial topology of networks. The instances are connected to their parent objects through the attribute “ObjectName” in the tables of NodeInstances and LinkInstances. The Node and Link Instances tables contain metadata about instances like name and location. The Networks table contains a collection of node and link instances and their data and metadata. The Scenarios table contains metadata that describe a scenario like its name, description, and time horizon. A Scenario represents the topological and the data changes in a network from a state to another state like existing case to climate change case. The ScenarioData table serves as a bridge to map out the relation where a scenario can apply to many data attributes and vice versa. 


* Networks can belong to other networks in a hierarchical order. The recursive relation in the network table organizes this order. For example, the Little Bear River network is part of or belongs to the Lower Bear River. Also ther Lower Bear River network is part of or belongs to the Bear River Network.
