Instances and connectivity
=========
An instance is a specific implementation of an object defined in the project metadata table. For example an instance of the object “Reservoir” is Hyrum reservoir in Utah. A node instance can stand by itself but a link instance references a start and end node. The connectivity between node and links instances represents the spatial topology of networks. The instances are connected to their parent objects through the attribute “ObjectName” in the tables of NodeInstances and LinkInstances. The Node and Link Instances tables contain metadata about instances like name and location. The Networks table contains a collection of node and link instances and their data and metadata. The Scenarios table contains metadata that describe a scenario like its name, description, and time horizon, and vice versa. 


Node: Vertix, Junction,	Node, Station

Link: edge, relationsship, connection, transmission link, Channel	Reach 	Creek	tributary	fork	branch	Element

***Homogenous vs heterogeneous instances in their attributes*** <p>
Should all the instances be identical of their attributes? or should every have its own collectiion of attributes?


***Connectivity rules :***<p>
These rules maintain the integrity of the network connectivity <p>
1. a Node can exist or stand by itself and a node can theoretically connect with zero to an infinite number of links <p>
2. a link must reference both a start and end node and cannot stand by itself. A link is meaningful by defining the connectivity of two nods and the direction of the connection (start and end nodes) <p>
3. a node cannot connect with itself or with another node without a link <p>
4. a link cannot connect with itself or with other links without a node <p>
5. Some link objects cannot connect with particular node objects due to connectivity limitation in the real world. For example, a river link object cannot connect between a pump station and household node objects. This business rule cannot be enforced in the WaM-DaM data model and it could be enforced in the database physical implementation as triggers. <p>
6. Some link objects (e.g., pipe) cannot have an illogical flow direction (i.e., start and end nodes). For example, a wastewater pipe link object cannot have a direction that flows from the manhole up to the houses. Or the same pipe direction cannot be flowing from a manhole to a drinking water pump station. This business rule cannot be enforced in the WaM-DaM data model and it could be enforced at the database level through triggers. It is the user responsibility to define this connection restriction. So far there is no exhaustive list of these restrictions

***Review ArcGIS connectivity rule and matrix*** Very Important  

ArcGIS uses a connectivity matrix to define which node is connected to another one


![NodeLinkConnectDemo](https://github.com/amabdallah/WaMDaM/blob/master/Figures/NodeLinkConnectDemo.jpg)
