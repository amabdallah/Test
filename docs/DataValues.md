Data Values
============

Physically store data values for a specific attribute of a particular object instance.


***WaM-DaM supports these multiple data formats:*** <p>
***1. TimeSereis*** <p>
The TimeSeries table stores data values and their time stamp. It also captures metadata like CensorCode which indicates whether the observation is censored (i.e., below or above a detection limit). 
The TimeSeriesMetadata table captures metadata for the whole block of time series like the site the data was collected at (see Horsburgh et al. (2008)).   

***2. MultiColums***<p>
 The MultiColumns (tabular) table stores arrays that have multiple paired columns.

***3. Parameters*** <p>
The Parameter table stores values of single numeric parameter like an elevation of 45.5 m. 

***4. Seasonal Parameter*** <p>
a seasonal parameter stores values that have seasonal patterns (e.g., water rights that are 20 acre-feet in winter and 5 acre-feet in summer OR "open gate" at night and close gate at day). The season value can be time series, numeric or text parameter, and binary. The seasonal attribute must have only one unit that applies to all the seasons, it has one data source, and one method. Also A season's data value should only take one formate like Binary or parameter. So if the data value for one season is binary, then the rest of the seasons should be binary too and they cant be numeric or text paramters. This Buissness rule is not enforced in the data model so I will enforce it in the database. The seasonal parameter cannot be a Muti-column formate because it gets tricky. The Multi-column format can be composed of three different attributes which have three different units, sources, and methods. However, the seasonal Parameter takes only one unit and metadata. The data value of the seaosnal Parameter is then stored at the one of the storage tables (time series, binary, fileBased, text, and parameter. 

**Use cases:**
1.Seasonal parameter attribute= Agriculture water demand
Season1 name=Summer, Season2 name=Winter, Season3 name=Spring, Season4 name = Fall
We can assign a start and end date and description for each season
Each season then gets connected to one of the data storage tables like the ParamerData one. 

2. Seasonal Parameter attribute =Reservoir Pool zones 
Seaosn 1= inactive, season2= conservation, season3= flood
***5. Binary***<p>
The Binary table stores binary data values (i.e., 0, 1) and reports the meaning of these values. For example, status of gates as open=1 or closed=0.

***6. File based***<p> 
 The FileBased table stores references for data stored in files like maps and images.

***7. Text controlled***<p>
The Text table stores text data values for an attribute (e.g., names of reservoir zones like dead, conservation, and flood pools).

***8. Text Free*** <p>
Stores text values with no enforcment. For example, the release rule could be described in text where the dam operator narrates his/her experiance of how they release water from the dam

***9. Equations (to be added soon)***<p>
This table could reference attributes at a partcicular node or link instance to other attributes at the same instance or other instances. For example, a reservoir release might be a function of inflow and evapotrasnpitation at the same reservoir. Or a reservoir release can be a function of another reservoir release.

***Tricky ***
The seasonal Parameter is the most complex kind of data formate becasue its data can be stored in the other kinds of data formats.For example, a seasonal parameter like Holiday and non-holiday seasons of water demand are simple. They can be stored as numerica parameters values like 20 cfs and 5 cfs. Or the same seasonal parameter data values can be soted in time sereis on an hour time step water demand during each season (holiday and non-holiday). The most complicated seasonal or step wise data format would be stored in a multi-comuns Array. An example would be the Reservoir pool zone elevation durig the months of the year. So the conservation pool "season name" can be the headline of one of the columns in the array. Then "months" could be another headline of the second column. Now the data values for the Months column would be the months of the year as seasons like July and September. The values of the "conseration" season would be the elevation of the pool or the volume of the reservoir. The elevation attribute gets its metadata though its foreign key and must be combined with the season name in this case. Summary:
MultiColumnArray name which is an attribute to a reservoir instance: Pools
ColumnsHeadline: 1) Months (from seasonsCV), 2) Elevation (reservoir attribute) and Inactive zone (from seasonCV), 3) Elevation and conservation zone, 4) elevation and flood zone.
The values would be like this:

Reservoir Pools
Months | InactiveElevation/|Conservation/Elevation|Flood/Elevation
------------ | -------------|----------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

