The Objects table is a container that describes general metadata for nodes and links (e.g., reservoir and canal). Each object can be associated with one or more attributes. For example, a reservoir can have attributes like capacity, dam height, and inflow. The use of node and link object names is controlled by a set of vocabularies like “Reservoir” and “Canal”. Finally, the Attributes table defines one or more parameters or variables like elevation and storage for an Object.  


#### Node Objects ####
Node objects represnet a generic abstract of a node like reservoir. A node instance inherits all the properties of a node object.   

**Node Objects Category**
Node objects that are similar and belong to a large group of objects can be organized in categories under a hierarchical order. For example, urban water management objects like culvert, wastewater treatment plant, and manhole can be organized in one category called wastewater. In the meanwhile, culverts and manholes can belong to the wastewater treatment plant object as of their parent   

#### Link Objects ####



#### Link Objects Category ####



#### Attributes ####


#### Node Object Attributes ####



#### Link Object Attributes ####


Here is the reason why attributes are categorized based on their association with an object and not on their own: one or more attribute can belong to a category in a spesfic object but more attributes might belong to another category for another object. For example, a pipe link object can have a category called physical that have three attributes: roughness cooeffienc, capacity, and lenght while a reserovir node object might have a category called physical and it has four attributes: capacity, MaxHydrualic flow, and StroageAreaElevation curve. Although the capacity attribute is common between the Reservoir and the pipe objects, they mean different things. The pipe capacity is the maximum flowrate that can go through the pipe while the reservoir capacity is the maximum volume that can hold. Anyways, the category of attributes makes more sesne when its linked to node or link and then to spesfic kind of object (e.g., reservoir and demand site for a node object, or river and pipe for a link object)







#### Node Attribute Category ####


#### Node Attribute Category ####


#### Link Attribute Category ####


