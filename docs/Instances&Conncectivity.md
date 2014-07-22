Instances
=========
Blue tables in Figure 1 contain the instances of objects that exist in the project, their connectivity, and scenarios that in which they appear. An instance is a specific implementation of an object defined in the project metadata table. For example an instance of the object “Reservoir” is Hyrum reservoir in Utah. A node instance can stand by itself but a link instance references a start and end node. The connectivity between node and links instances represents the spatial topology of networks. The instances are connected to their parent objects through the attribute “ObjectName” in the tables of NodeInstances and LinkInstances. The Node and Link Instances tables contain metadata about instances like name and location. The Networks table contains a collection of node and link instances and their data and metadata. The Scenarios table contains metadata that describe a scenario like its name, description, and time horizon.tes and vice versa. 


***Connectivity rules:***<p>
These rules maintain the intergrety of the network connectivity <p>
1. a Node can exist or stand by itself. A node can theoritically connect with zero to an infiniate number of links <p>
2. a link must reference both a start and end node and cannot stand by itself. A link is meaningful by defining the connectivity of two nods and the direction of the connection (start and end nodes) <p>
3. a node cannot connect with itself or with another node without a link <p>
4. a link cannot connect with itself or with other links without a node <p>
5. Some link objects cannot connect between particular node objects due to connectivity limitation in the real world. For example, a river link object cannont connect between a pump station and household node objects. This buiness rule cannot be enforced in the WaM-DaM data model and it could be enforeces in the database physical implemetation as triggers. <p>
6. Some link objects (pipe) cannot have a direction through start and end nodes that flow to an illogical way. For example, a Wastewater pipe link object cannot have a dirction that flows from the manhole up to the houses. Or the same piple direction cannot be flowing from a manhole to a drinking water pump station. This buiness rule cannot be enforced in the WaM-DaM data model and it could be enforced at the database level through triggers. 

***Review ArcGIS connectivity matrix*** Very Important  


![NodeLinkConnectDemo](https://github.com/amabdallah/WaMDaM/blob/master/Figures/NodeLinkConnectDemo.jpg)
