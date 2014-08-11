AttributeMetadata
=================


The AttributeMetadata table in WaM-DaM maps out the metadata of sources, units, samples, models, methods and datatype attribute formate to a specific attribute. 

This table allows the user to define an attribute with its metadata and then reuse it for all the instances that share this attribute and its metadata. For example, the US. Army Corps of Engineers database for Dams has over 70,000 dams that have 15 attributes. Once an attribute is defined like the dam drainage area with its metadata, then the user could use this attribute for the 70,000 dams, only and only if all these dams have simmilar metadata like the unit, the souurce and method. If a group of dams use different unit to report the dam drainage area, then the user either converts their unit to match the other group's unit or the user has to define a new AttributeMetadata instance that has similar metadata to the prevuios instance but it has a different unit.  


### Levels of Metadata for an instance (e.g., Hyrum Reserovir) <p>
1. common accross objects: Project, scenarion, user, and network names that this instance belongs to 
2. Comoon across instances: Object name, color, shape, description, and attribute names 
3. spesfic for the instance: like logitude, latitide, name, local x, and local y



***Types of water management data*** <p>
i) observations of water supply and demand quantity and quality, economic, and ecological data <p>
ii) connectivity (topology) between supply and demand elements, and <p>
iii) factual or descriptive information about system components like dam owner and release rules. 

***Data sources***
There are different sources (types) that a piece of data can originate from in WaM-DaM:<p>
1. Observations data (e.g., flowrate and water elevation in a reservoir). <p>
2. Factual data (e.g., dam ownder, reservoir maximum capacity, and reservour purpose).<p>
3. Opinion or experiance data (e.g., reservoir release rules and prefered water depth in a wetland unit).<p>
4. Simulation model results (e.g., recommended water releases from a reservoir based on a simulation model).<p>

All of these sources come from people affiliated with organizations 


**Attribute with Multiple values from Sources, methods, and models**

Once attribute might have multiple values that come from different sources and various methods. For example, maximum reservoir capacity might be reported by three entities like the US Army Corps of Engineers dataset and the State or County databases. Each of these source might use a different method. Besides, an attribute value might come from the simulation/optimization model that recommends expanding the reservoir capacity to a certain limit to handle future climate change drought scenarions.  


**Method and Source**
An attribute like a reservoir watershed area can be measured using a method described and specified by an organization like the US Army Corps of Engineers. However, the source for that data value might come from a different organization like Utah State University. So Utah State University estimated a reservoir watershed area based on the method by the US Army Corps of Engineers. A source reports what or where and the methods reports how!

**Samples, Methods, and Sources**
A data value could be collected using a sample accoroding to a method by a source who collects the sample

**Method, Source and models**
Data values in WaM-DaM can come from model simulation results, in this case the user enters exta metadata about the used model. The source of data can be reported through the sources table. The method will be picked in the methods table.   


**Simulations/Optimizations**
Stores metadata about simulation and optimization modeling results. One model can have zero or many simulation or optimization results. If the model parameters are changed then they will be tracked through the scenarios table. However, the same scenario can have multiple simulation results. In this case the results could be differenct because of the uncertinity or stochatic nature of the model.

**QUESTIONS**

1. How would I make the user go to a bridge table which ecesntialy mean they go to the other side of the bridge table and populate it with data. For example, the peoples table has basic data. But how do I make the user to populate the Orgnizations table which goes through the affiliation bridge tabel???

2. In the Time Sereis Metadata table, What would be the spatil reference for the Long. and Lat. coordinates of the site? Should I connect this table with the Spatial referene table???

