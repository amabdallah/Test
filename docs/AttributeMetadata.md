AttributeMetadata
=================


The AttributeMetadata table in WaM-DaM maps out the metadata of sources, units, samples, models, methods and datatype attribute formate to a specific attribute. 


There are three types of water management data that we need to capture in WaM-DaM: i) observations of water supply and demand quantity and quality, economic, and ecological data ii) connectivity (topology) between supply and demand elements, and iii) factual or descriptive information about system components like dam owner and release rules. 

***Data sources***
There are different sources (types) that a piece of data can originate from in WaM-DaM:
1. Observations data (e.g., flowrate and water elevation in a reservoir). 
2. Factual data (e.g., dam ownder, reservoir maximum capacity, and reservour purpose).
3. Opinion or experiance data (e.g., reservoir release rules and prefered water depth in a wetland unit).
4. Simulation model results (e.g., recommended water releases from a reservoir based on a simulation model).

All of these sources come from people affiliated with organizations 


**Attribute with Multiple values from Sources, methods, and models**

Once attribute might have multiple values that come from different sources and various methods. For example, maximum reservoir capacity might be reported by three entities like the US Army Corps of Engineers dataset and the State or County databases. Each of these source might use a different method. Besides, an attribute value might come from the simulation/optimization model that recommends expanding the reservoir capacity to a certain limit to handle future climate change drought scenarions.  


**Method and Source**
An attribute like a reservoir watershed area can be measured using a method described and specified by an organization like the US Army Corps of Engineers. However, the source for that data value might come from a different organization like Utah State University. So Utah State University estimated a reservoir watershed area based on the method by the US Army Corps of Engineers. A source reports what or where and the methods reports how!

**Samples, Methods, and Sources**
A data value could be collected using a sample accoroding to a method by a source who collects the sample

**Method, Source and models**
Data values in WaM-DaM can come from model simulation results, in this case the user enters exta metadata about the used model. The source of data can be reported through the sources table. The method will be picked in the methods table.   
