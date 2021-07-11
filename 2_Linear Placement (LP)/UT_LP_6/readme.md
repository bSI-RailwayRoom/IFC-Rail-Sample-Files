# Unit Test: Linear placement of drainage equipment (Span location)

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Linear placement of drainage equipment (Span location) |   UT_LP_6 | Florian HULIN| SNCF | xlsx + dwg + landxml|  |


## General
This unit test intend to experiment the use of IFC for representing the linear placement of drainage element. In the dataset, the placement is described as a set of parameters related to an alignment curve from the earth surface.

This data sets aims to test the scenario of positioning objects at span locations (from/to) with lateral and vertical offsets.

This data set aims to test the positioning of swept solids from a starting alignment station to an ending alignment Station, considering an horizontal offset from the rail alignment and different vertical constraints:

-  Vertical offset from a surface ( Case 1)
-  Start/End elevation in NGF ( Case 2)


## Data Description

### Alignment file (Landxml file)

The two linears placement cases defines below are using the same alignment.
The alignment file Dataset used for this Unit Test is in LandXML 1.2 format, produced by OpenRail Designer, which is a softaware developed by Bentley Systems, Inc.

To get more information about alignment in LandXML data Schema, you can visit the website : [http://www.landxml.org/schema/LandXML-1.2/documentation/LandXML-1.2Doc_Alignment.html](http://www.landxml.org/schema/LandXML-1.2/documentation/LandXML-1.2Doc_Alignment.html)

The file describes 3 alignements :

 -  VOIE DA
 -  VOIE 1X
 -  VOIE VAR
 
[Link to the file](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_6/Dataset/Alignment%20Cant_%20Test%20case%20subgrade.xml)
 ### Case 1 - Slotted Pipe profil positionning 
 
This object is composed of a slotted pipe and a draining trench. This kind of drainage is positioned with a lateral offset from the rail alignment and two verticals constraints (the upper trench and the flowline position). 

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_6/Dataset/slotted%20pipe1.png)

* Lateral positionning 

 The upper trench and the flowline are always positioned in the same horizontal offset. 

* Vertical positionning


The upper trench position will inherit the vertical position of the subgrade. 

The subgrade geometry should be generated in advance, please see subgrade placement data set provided.
The flowline vertical is positioned using a vertical offset from the first point. See image below. 

Notice : The two vertical constraints will defines the geometry (height) of the object.
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_6/Dataset/slotted%20pipe.png)

#### Dataset


- A  dwg file with the the drainage profile
- An xls table with the parameters below:
	- Referenced track
	- Side of the track where the object is positioned
	- Start Station (from alignment reference)
	- End Station (from alignment reference)
	- Horizontal offset: At starting and ending station
	- Vertical offset: At starting and ending station


|Profile type|Track reference| Side|Start Station | Ending Station| Horizontal Offset (Starting)|Horizontal Offset (Ending)|Vertical Offset(Starting)|Vertical Offset(Starting)|
|------------|---------------|-----|--------------|---------------|-----------------------------|--------------------------|-------------------------|-------------------------|
|Slotted pipe|       DA      |Right|   2325.978   |   2368.237    |             4.22            |            5.3           |           2.2           |           2.53          |




 ### Case 2 - Circular pipes profil positionning

This kind of drainage is positioned with a lateral offset from the rail alignment and has differents elevations (NGF) at the starting station and ending station.
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_6/Dataset/Circular%20pipe.png)

#### Dataset


- A dwg file with the two differents pipes profile
- An xls table with the parameters below:
	- Referenced track
	- Side of the track where the object is positioned
	- Start Station (from alignment reference)
	- End Station (from alignment reference)
	- Horizontal offset: At starting and ending station
	- Start elevation (NGF)
	- Stop elevation (NGF)
	- Pipe dimensions (mm)


|Profile type|Track reference| Side|Start Station | Ending Station| Horizontal Offset (Starting)|Horizontal Offset (Ending)|Z Start Elevation (NGF)| Z Stop Elevation (NGF)|Pipe Dimensions (mm)|
|------------|---------------|-----|--------------|---------------|-----------------------------|--------------------------|-----------------------|-----------------------|------------|
|Circular Pipe| DA|Left| 2479.98|2528.7| 3 |4.9|41.06|41.21|400|

