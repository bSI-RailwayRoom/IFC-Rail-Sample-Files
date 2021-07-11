# Unit Test: Alignment with Cant 1

|              Unit Test title                  | ID| Author | Data Owner | Format | Software Vendors | 
|:-----------------------------------------:|:------:|:------:| :------:| :------:| :------:|
|  Alignment with Cant 1 |   UT_AWC_1 | Chi Zhang | SBB | XTR |  |

 

## General
This Unit Test Scenario considers one alignment that is defined by three layouts: Horizontal, Vertical and Cant. 

The horizontal alignment consists of straight line segments, circular segments and transition curve (Clothoid), vertical alignment consists of straight line and circular segments, and cant alignment consists of straight line segments. 

The vertical alignment is measured from center line.

The input dataset is provided by SBB in XTR format, which is an open format defined by SBB for data exchange between TopoRail, a software developed by SBB, and other vendors.
It expected that an IFC file will be created by a software vendor who joins the process.

## Prerequisites
This scenario builds upon following scenarios:
- None

## Data Description

This dataset is in XTR format, produced by TopoRail, which is a software developed by SBB. 

This files describes an alignment of a single track of 2.5 km between two nodal points. 

The test data is captured in *.XTR format, which is an exchange format used by TopoRail to communicate with external software packages. The *.XTR file is a text file with ANSI encoding. 

The data for alignment is listed in a tabular format. The first part is the horizontal alignment, followed by the vertical alignment and cant. 

### Horizontal Alignment
The columns for the horizontal alignment are (from left to right):
Geometry Type, Easting (meter), Northing (meter), Azimuth (Gon), Element Length (meter), Start Radius (meter), End Radius (meter).
1. Geometry Type: 
- D = straight line
- C = arc
- R = transition curve, in this case it is clothoid (transition curve is always clothoid in Switzerland)
2. Easting: Start coordinate east in meter
3. Northing: Start coordinate North in meter
4. Azimuth: It defines the start direction. It is measured in Gon.
5. Element Length: It defines the length to the horizontal projection. The unit is meter.
6. Start Radius: It defines the start Radius at the beginning of the segment. The unit is meter.
7. End Radius: It defines the end Radius at the end of the segment. The unit is meter.

#### Data snippet
```
D	2723135.63807	1213636.85116	197.26170	18.11881	0.000	0.000
C	2723136.41718	1213618.74911	197.26190	10.43075	30000.000	30000.000
D	2723136.86385	1213608.32793	197.28403	488.58960	0.000	0.000
R	2723157.70188	1213120.18290	197.28403	72.00000	0.000	-467.000
C	2723162.61845	1213048.37002	192.37647	157.77472	-467.000	-467.000
R	2723207.32062	1212897.84194	170.86844	72.00000	-467.000	0.000
```
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_1/Dataset/RWR-Rail-Phase2_UT_AWC_1_1.jpg)

### Vertical Alignment
The columns for the vertical alignment are: (from left to right)
Geometry Type, Metraege (meter), Element Length (meter), Gradient (per mill), Radius (meter), Altitude (meter).
1.	Geometry Type: In Switzerland, there are straight line and arc used for vertical alignment. Transition curve is not used.
- d = straight line
- c = arc
2. Metraege: Cumulation of length in meter from beginning of the alignment to the start point of this segment. It is measured along horizontal alignment.
3. Element Length: Projected horizontal length in meter.
4. Gradient: Gradient in ‰ (per mill) at the beginning of the element.
5. Radius: Vertical Radius. If the segment is a straight line, then Radius is 0. If the segment is a arc, then the Radius is the start radius and end radius. 
6. Altitude: Height at the beginning of the segment in meter.

#### Data snippet
```
d	0.00000	61.67186	6.65013	0.000	459.1209
c	61.67185	0.75008	6.65012	1000.000	459.5310
d	62.42194	462.76333	5.90000	0.000	459.5357
c	525.18527	0.59997	5.90000	1500.000	462.2660
d	525.78524	107.84169	5.50000	0.000	462.2694
c	633.62692	0.64997	5.50000	-1000.000	462.8626
```

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_1/Dataset/RWR-Rail-Phase2_UT_AWC_1_2.jpg)

### Cant Alignment

The columns for the cant are: (from left to right)
Q, Metraege (meter), Element Length (meter), Start Cant (millimeter), End Cant (millimeter), Speed (km/h)
1. Q: Q is used to indicate cant segment. In Switzerland, only straight line is used for cant segment. 
2. Metraege: Cumulation of length in meter from beginning of the alignment to the start point of this segment. It is measured along horizontal alignment.
3. Element Length: Projected horizontal length in meter.
4. Start Cant: The start cant measured in millimeter. It is the height of left rail minus right rail.
5. End Cant: The end cant measured in millimeter. It is the height of left rail minus right rail.
6. Speed: Speed measured in km/h. 

#### Data snippet
```
Q	0.00000	0.00263	0.0	0.0	120
Q	0.00262	517.13653	0.0	0.0	95
Q	517.13915	72.00000	0.0	-126.0	95
Q	589.13915	157.77472	-126.0	-126.0	95
Q	746.91387	72.00000	-126.0	0.0	95
Q	818.91387	191.97447	0.0	0.0	95
```

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_1/Dataset/RWR-Rail-Phase2_UT_AWC_1_3.jpg)

## Execution Log

