Data Values
============

***WaM-DaM supports these multiple data formats:*** <p>
1. TimeSereis 
2. MultiColums
3. Parameters 
4. Binary
5. File based 
6. Text controlled 
7. Text Free 
8. Equations (to be added soon)




physically store data values for a specific attribute of a particular object instance. The TimeSeries table stores data values and their time stamp. It also captures metadata like CensorCode which indicates whether the observation is censored (i.e., below or above a detection limit). The TimeSeriesMetadata table captures metadata for the whole block of time series like the site the data was collected at (see Horsburgh et al. (2008)). The Text table stores text data values for an attribute (e.g., names of reservoir zones like dead, conservation, and flood pools). The Binary table stores binary data values (i.e., 0, 1) and reports the meaning of these values. For example, status of gates as open=1 or closed=0. The Parameter table stores values of single numeric parameter like an elevation of 45.5 m. The SeasonalParameter table stores sets of numeric parameters that have seasonal patterns (e.g., water rights that are 20 acre-feet in winter and 5 acre-feet in summer). The seasons here are not necessarily the four seasons but they can be other user-defined periods such as holiday vs non-holiday seasons. The FileBased table stores references for data stored in files like maps and images. The MultiColumns (tabular) table stores arrays that have multiple paired columns. The next section provides an example of how the MultiColumns data can be stored in a relation way in WaM-DaM. 
