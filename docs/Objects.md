The Objects table is a container that describes general metadata for nodes and links (e.g., reservoir and canal). Each object can be associated with one or more attributes. For example, a reservoir can have attributes like capacity, dam height, and inflow. The use of node and link object names is controlled by a set of vocabularies like “Reservoir” and “Canal”. Finally, the Attributes table defines one or more parameters or variables like elevation and storage for an Object.  

**Why Objcects**

Objects in WaM-DaM serve as a library of water management objects with their common and shared attributes. 

There could be another way to capture the obect name within the Instances table by adding an attribute called "object name" to the "instance" table. Thus the user could query the instances that have an object name like Reservoir. In this case the user has to define an object name for each instance they create which might make it cumbersome. The use of Objects table allows the user to define generic attributes to an object "Reservoir" like Description, color, and shape that wil be inhirted to all the instances that share such an object.  

Also, by defining an object with its attributes then all the instances of that spesific object will inhert those attibutes and therefore the instance will be similar and homogenous. In ODM1, everysite could be different than another site by having different set of variables that are measured at each site. However, WaM-DaM wants to enforce homognity among "sites" that are similar and share a set of common attributes. For example, an abject called reservoir shares a set of attributes that are common among all reservoirs (e.g., capacity, elevation, and purpose). The enforcement of homoginiety saves the user time by defining an object once and then creating "copies" instance of it.


***Legit problem***
What if the user wants to create two different kinds of reservoirs where each of them has different set of attributes though both of them still share some common attributes? Both of them are reservoirs but they're different. For example, a reservoir that has hydropower generaton will have hydropower attributes compared to another reservoir that donest have hydropwer. <p> In this case there are two option:<p>
A) Use one generic reserovir object that has all the possible attributes that all kinds of reservoirs have. However, if a reservoir instance has and uses the basic attributes in the object, then most of the attributes will have "Null" values which is not preffered in databases and indicates poor design. Also, by generalizing all kinds of reserovirs into one object, then we loose the opportunity to query our database. For example, if we have different kinds of reservoirs, then we can run a query agaisnt the object type to find out all the reservoirs of a type of "Hydropower".


#### Node Objects ####
Node objects represnet a generic abstract of a node like reservoir. A node instance inherits all the properties of a node object.   

**Node Objects Category**
Node objects that are similar and belong to a large group of objects can be organized in categories under a hierarchical order. For example, urban water management objects like culvert, wastewater treatment plant, and manhole can be organized in one category called wastewater. In the meanwhile, culverts and manholes can belong to the wastewater treatment plant object as of their parent  

#### The purpose using category to group objects or attributes is for two reasons: <p>
1. Provide a spesfic meaning to an object as the object belongs to a set of categories that provide self description. For example, a node object called reservoir becomes more spesfic when it belongs to a set of hierarchial categories like Supply, Surafe Water, Fresh Water, and Man-mad. These categories narrow the meanining and use or reservoir within this context opposed to the groundwater reservoir context as an example. <p>
2. Help users to quiery objects or attributes that belong to one category of interest. For example, a user might need to know the about all the physical attributes of the piple object in a a city's water distribution system. These attributes could be like the pipleine materrial, roughness, diameter, and lenght. Or the user might want to quiery operational attributes of their pipline network like flowate, chlorine concentration, and water age. So categorizing these attributes helps to  query them in related groups. Also, categorizing objects helps in accesing their grouping like: what are all the fresh surface water supply sources in my river basin? What are the industrial demand sites in  my watershed.  


***Can we have two objects with the same exact name (e.g., Reservoir)? YES. Now the two objects of reservoirs would either belong to the same category or ontology and they would have the same set of attributes. OR they would be different in the ontology tree and the sets of attributes. For example, there could be a reservoir that generates hydropower while the other kind of reservoir doesnt generate hydropower. So then it would be confusing to have two objects that have the same name but they are different:(

One of the solutions is to add an attribute in the Object Table called like "Object flavoir". This flavoir attribute is like a metadta that gives a second title to the reserovir that comunicates its main difference than the other flavoir of reservoir. 

#### Link Objects ####



#### Link Objects Category ####



#### Attributes ####


#### Node Object Attributes ####



#### Link Object Attributes ####


Here is the reason why attributes are categorized based on their association with an object and not on their own: one or more attribute can belong to a category in a spesfic object but more attributes might belong to another category for another object. For example, a pipe link object can have a category called physical that have three attributes: roughness cooeffienc, capacity, and lenght while a reserovir node object might have a category called physical and it has four attributes: capacity, MaxHydrualic flow, and StroageAreaElevation curve. Although the capacity attribute is common between the Reservoir and the pipe objects, they mean different things. The pipe capacity is the maximum flowrate that can go through the pipe while the reservoir capacity is the maximum volume that can hold. Anyways, the category of attributes makes more sesne when its linked to node or link and then to spesfic kind of object (e.g., reservoir and demand site for a node object, or river and pipe for a link object)







#### Node Attribute Category ####


#### Node Attribute Category ####


#### Link Attribute Category ####


