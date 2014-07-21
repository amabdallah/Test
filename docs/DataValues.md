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



