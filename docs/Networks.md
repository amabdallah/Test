Networks
========

A networks in WaM-DaM defiens the topolog "connectivity" between nodes and links of a water system. The networks table contain the node and link instances within a project, their connectivity, and scenarios that in which they appear. 

An instance is a specific implementation of an object defined in the project metadata table. For example an instance of the object “Reservoir” is Hyrum reservoir in Utah. A node instance can stand by itself but a link instance references a start and end node. The connectivity between node and links instances represents the spatial topology of networks. The instances are connected to their parent objects through the attribute “ObjectName” in the tables of NodeInstances and LinkInstances. The Node and Link Instances tables contain metadata about instances like name and location. The Networks table contains a collection of node and link instances and their data and metadata. The Scenarios table contains metadata that describe a scenario like its name, description, and time horizon. 

WaM-DaM supprts that concept that a network has zero or many instances BUT WaM-DaM doesnt support the concept where one instance might belong to zero or many networks. The reason of not supporting this many to many relation is just to keep things as simple as possible and because it not as common to have one instance belongs to multiple networks. An example of where one instance belongs to many networks is like a pump station that pumps water to two seprate water distribution networks. We still could create a dublicate pump station node instance that serve the second network. The question is whether there is a seprate pump system inside the pump station that serves the second network. OR whether the same exapct pump system is being used but on different timings. Lets suppose that the same pump system is being used for the two networks, then there would be attributes that can describe the pumping sytems while working on both networks like the pump effeciecity. BUT there would be attributes that are different like time series pumped water.In this case we cant use the exact node instance (e.g., pump station) for the two networks. I think creating two seprate node instances that of the pump station which prusmibly would share the exact attributes as both of instances share the same Object Type. 

**COOL**
Can instances can share the same data values for attributes with other instances?***

* Networks can belong to other networks in a hierarchical order. The recursive relation in the network table organizes this order. For example, the Little Bear River network is part of or belongs to the Lower Bear River. Also ther Lower Bear River network is part of or belongs to the Bear River Network.
* 
Can two node instances then have the exact same name? YES what matters is the primary key number in the NodeInstances table which will be different for each NodInstance. 
* 

***Important***
A network contains the union of all the node and link instances for all scenarios. For example, if a scenario adds a new node, then this node gets refrenced in the network. If a scenario deletes a node or link, its still stay in the network but the new scenario doesnt reference the node anymore. So to query the nodes and links in a network, the user needs to spesify the scenario.


***Scenarios***<p>
A Scenario tracks the changes in the network, connectivity and the data and metadata from a state to another one like existing case to climate change case. Also, adding the scenario as another attribute to the AttributeMatadata allows to reference multiple scenarios to attributes and thier data values. Thus, we dont need to duplicate the similar data among scenarios.


***Do I need to add a bridge table between scenarios and networks to map out the many to many relations. I will add more complexity but whats the real benift and application to this addition?***
A network can have zero or many scenarios apply to it. Now, the case where a scenario applies to many networks is not supported and offers little benifit. 



***Scenarios Table:***<p>
This table captures metadata like the scenario name, time horizon, description, and the reference to the network ID that applies to. 

***ScenarioNodeInstanceAttributeData Table:***<p>
This table is like the centeral table that captures all the metadata and data about an attribute that belongs to a node instance within a network and a scenario. 

***ScenatiosNodeBridge***<p>
This table maps out the many to many relationship between a scenarios and attriute data and metadata. For example, one scenario can have zero or many attributes data and metadata that are attached to it. Also one attribute data and metadata can belong to one or many scenarios.   

***Question:*** Do we need to relate scenarios to each other? for example, is there a need to say that scenario x belongs to scenario y? I'm doing this relation with networks where a samall network could belong to a larger network. Anyways, it should be easy to add this recursive relation to the scenarios table


***Importance of maping data through scenarios***<p>
 A Scenario represents the topological (network configuration of node and link instances) and the data and metadata changes in a network from a state to another state like existing case to climate change case. The Scenarios table contains metadata that describe a scenario like its name, description, and time horizon. 
A scenario addition in WaM-DaM helps:

1. References multiple scenarios to similar data. Thus avoid redunduncy and save space. For example, a time series data if inflow to a reservoir could be the same in two scenarios. Then we store one time sereis and then reference it to two senarios instead of storing two time sereis data for two scenarios <p>

2. A user could run a query to find out the data differences between two scenarios. The differences could be in topology (network configuration of instances), data values for attributes, and metadata (e.g., source and method)?  For example, what is the difference between the base case and climate change scenarios? The scenario concept helps other people who did not develop the scenarios learn about how similar or different these sceanrios are <p>
The key table that maps out these similraties and differences is the ScenariosNodeORLinkBridge table. 


**Need to consider**
I need to allows one instance to belong to many networks. Give a demonestration example where we want to merge two networks together using one or many connections (i., links).

I need to think about deleting the Project and connecting the user to the Instance Table.<p>
I need to workout examples of networks merging with each other <p>
Add this key question. What are the MasterNetworks that WaM-DaM has and what are their types?<p>
Delete the political Jursdication tables <p>
Consider deleting the recursive relation in the networks. Maybe I should keep it. <p>
What is uniqe about networks other than their name and type? maybe purpose?


**Master Netowrks purpsoes** <p>
Simulation (what if?)
Optimization (how?)
allocaton (where?)
evaluation (??)




*Types MasterNetworks:**<p> 
Question: can a network has many types? Obvioulsy a type can apply to many networks. 

Drinking water distribution networks <p>
Wastewater distribution networks <p>
river networks <p>
stromwater netwokrs <p>
regional water conveyance networks <p>
Secondary water distribution system <p>
Water trade networks <p>
Water and Energy networks <p>
Water Planning networks <p>
Hydrologic networks <p>
Ecological networks <p>
Aggreculture water distribution neworks <p>
Economic netowrks <p>
Hydro-economic networks <p>
Engineered <p>
Natural <p>


**Question**<p>
How can I keep track of the source of the instance, not the attribute only? because it has to do with one instance coming from multiple sources where each source has a different latitide and longitude???


