Networks
========

A networks in WaM-DaM defiens the topolog "connectivity" between nodes and links of a water system. The networks table contain the node and link instances within a project, their connectivity, and scenarios that in which they appear. 

An instance is a specific implementation of an object defined in the project metadata table. For example an instance of the object “Reservoir” is Hyrum reservoir in Utah. A node instance can stand by itself but a link instance references a start and end node. The connectivity between node and links instances represents the spatial topology of networks. The instances are connected to their parent objects through the attribute “ObjectName” in the tables of NodeInstances and LinkInstances. The Node and Link Instances tables contain metadata about instances like name and location. The Networks table contains a collection of node and link instances and their data and metadata. The Scenarios table contains metadata that describe a scenario like its name, description, and time horizon. 


* Networks can belong to other networks in a hierarchical order. The recursive relation in the network table organizes this order. For example, the Little Bear River network is part of or belongs to the Lower Bear River. Also ther Lower Bear River network is part of or belongs to the Bear River Network.


***Scenarios*** 
A Scenario tracks the changes in the network, connectivity and the data and metadata from a state to another one like existing case to climate change case. Also, adding the scenario as another attribute to the AttributeMatadata allows to reference multiple scenarios to attributes and thier data values. Thus, we dont need to duplicate the similar data among scenarios.


***Scenarios Table:*** <p>
This table captures metadata like the scenario name, time horizon, description, and the reference to the network ID that applies to. 

***ScenarioNodeInstanceAttributeData Table:*** <p>
This table is like the centeral table that captures all the metadata and data about an attribute that belongs to a node instance within a network and a scenario. 

***ScenatiosNodeBridge*** <p>
This table maps out the many to many relationship between a scenarios and attriute data and metadata. For example, one scenario can have zero or many attributes data and metadata that are attached to it. Also one attribute data and metadata can belong to one or many scenarios.   

***Importance of maping data through scenarios***
A user could run a query to find out the data differences between two scenarios. For example, what is the difference between the base case and climate change scenarios?





