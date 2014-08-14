		Benefit of compiling data into WaM-DaM
Adel Abdallah
April 21, 2014

1.	Merge Global, US national, and regional data into one place so it’s possible to study overlapping data from different aspects (political, operational, and physical). See Figure 1, a schematic that shows the data sources into WaMDaM.
Table 1 below lists the unique attributes that each dataset has and doesn’t exist in the other data sources. Usually the Lakes data sets have more information about the lake while the Dams datasets have more information on dams and their structure. So integrating the Dams and lakes datasets helps us to get both of these data for our modeling needs. Models need data about the reservoir pool and they also need data about the release structures like the gates.

Table 1: Unique attributes from different data sources 

	Unique attributes |data	Source
	------------------| ----------
1	Dam Hazard, main and sub basins|	Global Dams
2	hydrologic unit code|	National Atlas of Lakes 
3	Maximum Discharge (spill way), Spillway Type, Spillway Width, Outlet Gates, |	US National Inventory of dams 
4	Resettlement, Irrigated areas, Electric installed capacity, Mean annual energy, Volume flood protection|	ICOLD Dams Dataset
5	Network connectivity, reservoir operation rules, supply and demand data for a the Lower Bear River|	Lower Bear River WEPA model
6	Network connectivity, reservoir operation rules, supply and demand data for Parleys Canyon|	GoldSim Parleys Canyon model
7	Inflow, release, weather data|	Time series data (CUAHSI)

2.	Report descriptive metadata (source, method, units, spatial reference) so it’s easier and possible to interpret the data values correctly. Existing data sources use different coded attributes with no clear meaning. The user has to look up a PDF file or a different webpage to understand what the coded attribute mean and what are the units and methods that describe it.

3.	Enforce controlled vocabulary by describing attributes and metadata consistently so it’s easier to query and compare data (e.g., Catch_skm, Drainage_Area, DRAIN_AREA enforce the term CatchmentArea)

4.	Overcome technology and platform challenges (shapfiles, web search engine, and membership) by using one source “WaM-DaM” database.
 

5.	Organize data in a consistent way for all data sources. For example, the reservoir purposes are organized in four different ways in the five sources of data as shown in the Table 2 below. 

**Table 2: The different methods of organizing reservoir purpose in existing datasets**

Source |	Attributes that organize reservoir purpose 
-------| ------------------------------------------------------
Global Dams Dataset| USE_IRRI, USE_ELEC, USE_SUPP, USE_FCON, USE_RECR, USE_NAVI, USE_FISH, USE_PCON, USE_LIVE, USE_OTHR, MAIN_USE
Global Lakes Dataset| USE_1 (main), USE_2 (secondary), USE_3 (third)
US National Inventory of Dams Dataset (NID)| Primary_Purpose, All_Purposes
US National Atlas of Dams| PURPOSES (coded purposes ordered in priority)
ICOLD Dams Dataset| Purpose(s) of reservoir (coded purposes ordered in priority)


6.	Manage network data, connectivity, and its metadata for two regional watersheds: Parleys Canyon and Lower Bear River networks.

 ![Image](https://github.com/amabdallah/WaMDaM/blob/master/Figures/adel10.png)
Figure 1: Global, US National, and regional data sources to WaM-DaM
