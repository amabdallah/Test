###Key Features of WaM-DaM###


The following are the key features of WaM-DaM that contributes to the exisitng state of the art data models:


**1. [Concept of Object and instances] Define objects and attributes for physical objects with their ontology that share similar and common attributes, then create instances of them that inhirt them and thus enforce homoginity of data and matadarta among them**

**2. [Connectivity] Define the connectivity between instancs like sites through links For example, WaM-DaM allows you to organize data that comprise a network of nodes and links**

**3. [Multiple Data Types] Organize multiple data formats like time series, text, multi-column, and parameters from different sources WaM-DaM adopts the principles of representing time series data as in the Observation Data Model. WaM-DaM organizes multi-columns data in a relational format that allows users to query pieces of data inside each multi-columns table.**

**4. [Scenarios] Reference multiple data values and meatadata to the same objects and instance through scenarios**

**5. [Semantic Homogniety] Overcome semantic heterogeneity in water management data WaM-DaM uses controlled vocabularies to enforce the homogeneity of object (nodes and links) names throughout the network**

**6. [Conditioanl Data Query] Allows direct conditional data queries WaM-DaM is a relational data model that allows users to access samll pieces of data with sophisticated conditions.**




####How Does WaM-DaM differ in storing time series data than the Observation Data Model 1.0 (ODM)?####
 
WaM-DaM mostly adapted the method of organizing time series data that ODM uses. However, WaM-DaM organizes time series data differentky than ODM. WaM-DaM mostly captures metadata for the entire blook of a time series rather than on every time step data value. The reason for that is to reduce the burden of entering metadata that is required to populate a time series. These metadata are most likely not to change within a time series like (Site lat, ODM Site name, Site Long, UTC Offset, time unit, and Is Regular. However, WaM-DaM still captures metadata that goes along with each data values like LocalDate Time, DateTimeUTC, Value, and CensorCode. Generalizing metadata for a block of time series helps to maintain the homogeniety of data values and reduces the burden to enter less metadata. In case, a time series has two different time units, then the user either has to convert one of the units to the other one OR the user could define two seprate blocks of time series that reference the same attribute and object instance. Shall the user needs to use both time series data, then its their responsibility to convert one of the units and combine both timeseries with each other. 
  
  
This method includes: capturing metadata like sources, methods, samples, sites and variables. WaM-DaM uses the term object instances instead of sites as in ODM. ODM is spesfically designed to organize time sereis data and metadata for sites (stations) that have comon metadata attributes like  
 +site name, site, code, lat, lomg, and elevation_m. However, WaM-DaM organizes data and metadata for "sites" like reservoirs, canals, and demand sites that have different metadata. For example, a reservoir can have metadata that describes the  

Also WaM-DaM uses the term attributes instead of variables in ODM. The use of attributes sound more relent or accurate for WaM-DaM because, WaM-DaM captures data and metadata about the water resources infrasturcure like Dam owner and dam pool names. 
