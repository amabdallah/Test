AttributeMetadata
=================


AttributeMetadata in WaM-DaM contain the instances of objects that exist in the project, their connectivity, and scenarios that in which they appear. An instance is a specific implementation of an object defined in the project metadata table. For example an instance of the object “Reservoir” is Hyrum reservoir in Utah. A node instance can stand by itself but a link instance references a start and end node. The connectivity between node and links instances represents the spatial topology of networks. The instances are connected to their parent objects through the attribute “ObjectName” in the tables of NodeInstances and LinkInstances. The Node and Link Instances tables contain metadata about instances like name and location. The Networks table contains a collection of node and link instances and their data and metadata. The Scenarios table contains metadata that describe a scenario like its name, description, and time horizon. A Scenario represents the topological and the data changes in a network from a state to another state like existing case to climate change case. The ScenarioData table serves as a bridge to map out the relation where a scenario can apply to many data attributes and vice versa. 


There are three types of water management data that we need to capture in WaM-DaM: i) observations of water supply and demand quantity and quality, economic, and ecological data ii) connectivity (topology) between supply and demand elements, and iii) factual or descriptive information about system components like dam owner and release rules. 

***Data sources***
There are different sources that a piece of data can originate from in WaM-DaM:
1. Observational data (e.g., flowrate and water elevation in a reservoir) 
2. Factual data (e.g., dam ownder and reservoir capacity)
3. Opinion or experiance data (e.g., reservoir release rules and  
