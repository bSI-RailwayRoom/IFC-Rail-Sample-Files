# Unit Test:Linear Placement of Base Transceiver Station(BTS)

|UnitTest title	 |ID |	Author	|Data Owner	|Format	|SWV|
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|Linear placement of base transceiver station(BTS)|UT_LP_10|Lihai Liu|CRBIM|DWG, IFC|  |

## 1. **General**

This unit test intends to experiment the use of IFC for the linear placement of the BTS (Base Transceiver Station) site. In the dataset, the placement is described as a set of parameters related to the alignment curve and the location information of BTS site.

This document describes in detail the data organization of the plane, profile, and broken chain of a railway line through a railway line example. The telecom domain expert provide the placement details of BTS site along the curve, so as to facilitate the software service manufacturer to test the placement of the BTS along the curve.

## 2. **Railway**  **Line**  **Plane**

### 2.1 Line plane drawing

![alt text](DataSet/Example%20of%20double%20track%20line%20plane%20drawing.png)

<p align="center">Figure 1 Example of double track line plane drawing</p>

Facing the direction of large mileage, the left side line is called &quot;left line&quot;, and the right side line is called &quot;right line&quot;. For double track parallel lines, the left line is generally taken as the reference line, and the right line is not set with mileage system.

### 2.2 Line plane data description

<p align="center">Table 1 Data description of each unit in line plane</p>

| **Type** | **StartDistAlong** | **StartRadius** | **StartDirection** | **StartPt.YN** | **StartPt.XE** | **IsCCW** |
| --- | --- | --- | --- | --- | --- | --- |
| Line | 0 | 0 | -3.12357701 | 3593277.389 | 613282.891 | 　 |
| Transition | 8541.628407 | 0 | -3.12357701 | 3593123.514 | 604742.6487 | T |
| Arc | 9131.628407 | 8000 | -3.16045201 | 3593120.137 | 604152.694 | T |
| Transition | 10849.21881 | 8000 | -3.37515081 | 3593335.922 | 602452.0357 | T |
| Line | 11439.21881 | 0 | -3.41202581 | 3593486.531 | 601881.6192 | 　 |
| Transition | 11977.33886 | 0 | -3.41202581 | 3593630.289 | 601363.057 | F |
| Arc | 12447.33886 | 10000 | -3.38852581 | 3593752.294 | 600909.1805 | F |
| Transition | 12807.1703 | 10000 | -3.35254267 | 3593833.953 | 600558.757 | F |
| Line | 13277.1703 | 0 | -3.32904267 | 3593925.151 | 600097.7017 | 　 |
| Transition | 19250.09777 | 0 | -3.32904267 | 3595038.231 | 594229.4042 | T |
| Arc | 19920.09777 | 7000 | -3.37689981 | 3595173.559 | 593573.2831 | T |
| Transition | 25116.44147 | 7000 | -4.11923462 | 3598067.803 | 589401.0038 | T |
| Line | 25786.44147 | 0 | -4.16709176 | 3598634.961 | 589044.4364 | 　 |
| Transition | 26073.16353 | 0 | -4.16709176 | 3598880.101 | 588895.7216 | F |
| Arc | 26743.16353 | 5500 | -4.10618267 | 3599445.667 | 588536.713 | F |
| Transition | 29334.79576 | 5500 | -3.63497681 | 3601156.064 | 586621.5786 | F |
| Line | 30004.79576 | 0 | -3.57406772 | 3601449.117 | 586019.1901 | 　 |
| Transition | 32038.49095 | 0 | -3.57406772 | 3602301.478 | 584172.7349 | T |
| Arc | 32708.49095 | 5500 | -3.63497681 | 3602594.531 | 583570.3464 | T |
| Transition | 35080.73642 | 5500 | -4.06629417 | 3604127.173 | 581783.7707 | T |
| Line | 35750.73642 | 0 | -4.12720326 | 3604677.973 | 581402.494 | 　 |
| Transition | 36032.03559 | 0 | -4.12720326 | 3604912.466 | 581247.1172 | F |
| Arc | 36622.03559 | 8000 | -4.09032826 | 3605400.224 | 580915.2277 | F |
| Transition | 37801.14345 | 8000 | -3.94293978 | 3606304.453 | 580160.1446 | F |
| Line | 38391.14345 | 0 | -3.90606478 | 3606718.003 | 579739.3904 | 　 |
| Transition | 42726.04198 | 0 | -3.90606478 | 3609718.429 | 576610.6868 | T |
| Arc | 43316.04198 | 8000 | -3.94293978 | 3610131.98 | 576189.9326 | T |
| Transition | 44313.92857 | 8000 | -4.06767561 | 3610890.142 | 575542.1081 | T |
| Line | 44903.92857 | 0 | -4.10455061 | 3611370.257 | 575199.2557 | 　 |
| Transition | 45190.52916 | 0 | -4.10455061 | 3611605.523 | 575035.5797 | F |
| Arc | 45780.52916 | 8000 | -4.06767561 | 3612085.638 | 574692.7273 | F |
| Transition | 47048.67201 | 8000 | -3.90915775 | 3613034.711 | 573853.632 | F |
| Line | 47638.67201 | 0 | -3.87228275 | 3613433.814 | 573419.1499 | 　 |
| Transition | 52417.38945 | 0 | -3.87228275 | 3616623.052 | 569860.372 | T |
| Arc | 52867.38945 | 6500 | -3.90689813 | 3616927.206 | 569528.7558 | T |
| Transition | 55716.96762 | 6500 | -4.34529477 | 3619281.935 | 567964.7463 | T |
| Line | 56166.96762 | 0 | -4.37991016 | 3619705.545 | 567812.9821 | 　 |
| Line | 58034.01482 | 0 | -4.37991016 | 3621470.346 | 567203.602 | 　 |

In IFCAlignment, a plane straight line segment is derived from a 2D curve segment. The attribute definition is shown in the following table:

<p align="center">Table 2 Attribute definition of 2D curve segment</p>

| No. | Attribute | Attribute type | Constraint value | Comment |
| --- | --- | --- | --- | --- |
| 1 | Startpoint | IfcCartesianPoint | [1:1] | Starting point coordinates |
| 2 | StartDirection | IfcPlaneAngleMeasure | [1:1] | The starting point direction is the angle between the X axis and the plane rectangular coordinate system. Clockwise is positive and counterclockwise is negative. The absolute value of the angle value should not be greater than 360 ° or 2 π |
| 3 | SegmentLength | IfcPositiveLengthMeasure | [1:1] | Length of 2D curve |



The attribute definition of plane circular curve is shown in the following table:

<p align="center">Table 3 Attribute definition of 2D arc segment</p>

| No. | Attribute | Attribute type | Constraint value | Comment |
| --- | --- | --- | --- | --- |
| 1 | Radius | IfcPositiveLengthMeasure | [1:1] | Arc radius |
| 2 | StartDirection | IfcBoolean | [1:1] | Is the arc deflected counterclockwise |

The attribute definition of planar transition curve is shown in the following figure：

<p align="center">Table 4 Attribute definition of 2D transition curve</p>

| No. | Attribute | Attribute type | Constraint value | Comment |
| --- | --- | --- | --- | --- |
| 1 | StartRadius | IfcCartesianPoint | [1:1] | Start radius of transition curve |
| 2 | IsCCW | IfcPlaneAngleMeasure | [1:1] | Is the transition curve deflected counterclockwise |
| 3 | EndRadius | IfcPositiveLengthMeasure | [1:1] | End radius of transition curve |
| 4 | TransitionCurveType | IfcTransitionCurveTypeEnum | [1:1] | Type of transition curve |

As for the plane transition curve, the type of spiral or cubic parabola is adopted for all grades of wheel rail railway in China, and the type of one wave sine curve is adopted in the design of high-speed maglev railway (Standard for Technology of Maglev Railway (Trial)).

## 3. **Railway line profile**
### 3.1 Line profile drawing

![alt text](DataSet/Example%20of%20line%20profile%20drawing.png)

<p align="center">Figure 2 Example of line profile drawing</p>

### 3.2 Line profile data description

<p align="center">Table 5 Data description of each unit of line profile</p>

| **Type** | **StartDistAlong** | **HorizontalLength** | **StartHeight** | **StartGradient** | **Radius** | **IsConvex** |
| --- | --- | --- | --- | --- | --- | --- |
| Line | 0 | 930.0131386 | 241.098 | -0.011 | 　 | 　 |
| Arc | 930.0131386 | 239.9804418 | 230.8678555 | -0.011 | 30000 | F |
| Line | 1169.99358 | 2129.641749 | 229.1880193 | -0.003 | 　 | 　 |
| Arc | 3299.63533 | 300.7172637 | 222.799094 | -0.003 | 30000 | T |
| Line | 3600.352594 | 1911.800849 | 220.3896575 | -0.01303 | 　 | 　 |
| Arc | 5512.153442 | 675.7065261 | 195.4884514 | -0.01303 | 30000 | F |
| Line | 6187.859968 | 2138.9269 | 194.2976982 | 0.0095 | 　 | 　 |
| Arc | 8326.786868 | 174.1639924 | 214.6176839 | 0.0095 | 30000 | F |
| Line | 8500.950861 | 1456.862442 | 216.7779087 | 0.01531 | 　 | 　 |
| Arc | 9957.813302 | 672.1482913 | 239.0779781 | 0.01531 | 30000 | T |
| Line | 10629.96159 | 5686.418683 | 241.8357639 | -0.0071 | 　 | 　 |
| Arc | 16316.38028 | 554.9724105 | 201.4621912 | -0.0071 | 30000 | F |
| Line | 16871.35269 | 3558.537309 | 202.6552798 | 0.0114 | 　 | 　 |
| Arc | 20429.89 | 527.9760866 | 243.2226052 | 0.0114 | 30000 | T |
| Line | 20957.86608 | 5991.784802 | 244.5952201 | -0.0062 | 　 | 　 |
| Arc | 26949.65088 | 77.99147093 | 207.4457784 | -0.0062 | 30000 | T |
| Line | 27027.64236 | 1580.529481 | 206.8608409 | -0.0088 | 　 | 　 |
| Arc | 28608.17184 | 460.9542832 | 192.9521814 | -0.0088 | 30000 | F |
| Line | 29069.12612 | 966.0394992 | 192.4372395 | 0.00657 | 　 | 　 |
| Arc | 30035.16562 | 166.9645197 | 198.7798926 | 0.00657 | 30000 | T |
| Line | 30202.13014 | 1601.51904 | 199.4114831 | 0.001 | 　 | 　 |
| Arc | 31803.64918 | 209.9923354 | 201.0130022 | 0.001 | 30000 | F |
| Line | 32013.64151 | 852.9238699 | 201.9579561 | 0.008 | 　 | 　 |
| Arc | 32866.56538 | 84.16212209 | 208.7813471 | 0.008 | 30000 | F |
| Line | 32950.72751 | 3800.046938 | 209.5727126 | 0.01081 | 　 | 　 |
| Arc | 36750.77444 | 275.7255935 | 250.6351796 | 0.01081 | 30000 | F |
| Line | 37026.50004 | 1659.741424 | 254.8820607 | 0.02 | 　 | 　 |
| Arc | 38686.24146 | 704.8793929 | 288.0768892 | 0.02 | 30000 | T |
| Line | 39391.12085 | 1650.031185 | 293.8913415 | -0.0035 | 　 | 　 |
| Arc | 41041.15204 | 194.9856442 | 288.1162324 | -0.0035 | 30000 | T |
| Line | 41236.13768 | 4957.521454 | 286.8000932 | -0.01 | 　 | 　 |
| Arc | 46193.65914 | 389.9845961 | 237.2248786 | -0.01 | 30000 | F |
| Line | 46583.64373 | 5390.851293 | 235.8599902 | 0.003 | 　 | 　 |
| Arc | 51974.49503 | 408.2667179 | 252.0325441 | 0.003 | 25000 | F |
| Line | 52382.76174 | 2726.777687 | 256.5914092 | 0.01933 | 　 | 　 |
| Arc | 55109.53943 | 558.2660429 | 309.3116595 | 0.01933 | 25000 | T |
| Line | 55667.80547 | 1295.837338 | 313.8705246 | -0.003 | 　 | 　 |
| Arc | 56963.64281 | 50.00847572 | 309.9830126 | -0.003 | 25000 | F |
| Line | 57013.65129 | 1020.363712 | 309.8830045 | -0.001 | 　 | 　 |

The attribute definition of profile line segment is shown in the following table：
<p align="center">Table 6 Attribute definition of line segment of profile</p>

| No. | Attribute | Attribute type | Constraint value | Comment |
| --- | --- | --- | --- | --- |
| 1 | StartDistAlong | IfcLengthMeasure | [1:1] | The length along the line plane from the starting point of the line |
| 2 | HorizontalLength | IfcPositiveLengthMeasure | [1:1] | The length of the line plane corresponding to the profile line segment |
| 3 | StartHeight | IfcLengthMeasure | [1:1] | Starting point elevation value |
| 4 | StartGradient | IfcRatioMeasure | [1:1] | The slope value in the tangent direction of the start point. Its value is the tangent value of the angle formed by the tangent of the starting point of the line segment expressed in percentage and the positive direction of the x-axis |
| 5 | ToVertical | [IfcAlignment2DVertical@Segment](mailto:IfcAlignment2DVertical@Segment) | S[1:1] | Reverse property that points to the line profile that contains the line profile segment |

The attribute definition of profile circular curve is shown in the following table：
<p align="center">Table7 Profile vertical curve attribute definition</p>

| No. | Attribute | Attribute type | Constraint value | Comment |
| --- | --- | --- | --- | --- |
| 1 | Radius | IfcPositiveLengthMeasure | [1:1] | Curve radius |
| 2 | IsConvex | IfcBoolean | [1:1] | Is it a convex curve |


## 4. **Line broken chain**

### 4.1 Line broken chain drawing

![alt text](DataSet/Example%20of%20line%20broken%20chain%20drawing.png)
<p align="center">Figure 3 Example of line broken chain drawing</p>

In the broken chain shown in the figure, &quot;dk387 + 949.1&quot; is called the equal sign left lane mileage, &quot;dk387 + 950&quot; is called the equal sign right mileage.

### 4.2 Line broken chain data description

<p align="center">Table 8 Data description of line broken chain</p>


| **StartDistAlong** | **Length** | **StartChainageNominal** | **IsChainageNominalIncrease** | **Prefix** |
| --- | --- | --- | --- | --- |
| 0 | 6843.872 | 388000 | T | DK |
| 6843.872 | 19194.78 | 394900 | T | DK |
| 26038.647 | 31995.37 | 414100 | T | DK |



According to the &quot;Standard for Storage of Railway Engineering Information Model Data (Version 1.0)&quot; issued by China Railway BIM alliance, the definitions of IfcChainageSystem and IfcChainageSystemSegment are defined, and the details are as follows:

The attribute definition of line broken chain is shown in the following figure：

| No. | Attribute | Attribute type | Constraint value | Comment |
| --- | --- | --- | --- | --- |
| 1 | StartDistAlong | IfcLengthMeasure | [1:1] | The length along the line plane from the starting point of the line |
| 2 | Length | IfcPositiveLengthMeasure | [1:1] | The length of the line plane corresponding to the curve |
| 3 | StartChainageNominal | IfcLengthMeasure | [1:1] | Nominal mileage value of starting point of mileage section |
| 4 | IsChainageNominalIncrease | IfcBoolean | [1:1] | Is the mileage increased along the line |
| 5 | Prefix | [IfcText](mailto:IfcAlignment2DVertical@Segment) | [1:1] | Prefix string for mileage |

![alt text](DataSet/Attribute%20definition%20of%20line%20broken%20chain.png)
<p align="center">Figure 4 Attribute definition of line broken chain</p>

## 5. **BTS site placement**

The dataset includes 5 BTS sites that placed according to the alignment curve. The geometry of the BTS site is simplified, which only includes the tower and technical room.

For the placement of a BTS site, there is no parameter that depends on cant.The placement of the BTS site will be determined by the mileage location and left/right side of the BTS site, the lateral and vertical offset.

The lateral offset is the distance between the position of the center point of the BTS site and the horizontal alignment curve at the corresponding mileage. This distance is measured along the axis that is perpendicular to the tangent of the horizontal alignment curve at the corresponding mileage. The offset is always a positive value. The direction of the offset is defined by the &quot;Side&quot; parameter.

The vertical offset is the distance between the position of the center point of the BTS site and the vertical alignment curve at the corresponding mileage. This distance is measured along the vertical axis of the general coordinate system. A positive vertical offset indicates that, in the general coordinate system, the vertical coordinate of the vertical alignment curve at the corresponding mileage is less than the vertical coordinate of the origin of the BTS site.

### 5.1 BTS site placement drawing

![alt text](DataSet/Example%20of%20BTS%20site%20placement%20drawing.png)

<p align="center">Figure 5 Example of BTS site placement drawing</p>

![alt text](DataSet/Example%20of%20BTS%20site%20drawing.JPG)

<p align="center">Figure 6 Example of BTS site drawing</p>

5.2 BTS placement data description

<p align="center">Table 9 Data description of BTS placement</p>

| No | Site Length </br>（ m ）| Site Width</br> （ m ） | Prefix | Mileage | Lateral Offset</br>（ m ） | Vertical Offset</br> （ m ） | Side |
| ---- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| 1 | 37 | 22 | DK | 408+480 | 52 | 13.9 | Right |
| 2 | 37 | 22 | DK | 413+680 | 65 | 4.2 | Right |
| 3 | 37 | 22 | DK | 424+885 | 34 | 7.5 | Left |
| 4 | 37 | 22 | DK | 428+925 | 26 | 8.3 | Left |
| 5 | 37 | 22 | DK | 429+270 | 53 | 2.6 | Right |

The attribute definition of BTS site placement are shown in the following table：

| **No** | **Attribute** | **Attribute Type** | **Constraint Value** | **Comment** |
| --- | --- | --- | --- | --- |
| 1 | Site length | IfcLengthMeasure | [1:1] | The length of BTS site |
| 2 | Site Width | IfcLengthMeasure | [1:1] | The width of BTS site |
| 3 | Prefix | IfcText | [1:1] | Prefix string for mileage |
| 4 | Mileage | IfcLengthMeasure | [1:1] | Mileage value of line plane corresponding to BTS site center |
| 5 | Lateral Offset | IfcLengthMeasure | [1:1] | The distance between the position of the center point of the BTS site and the horizontal alignment curve at the corresponding mileage |
| 6 | Vertical Offset | IfcLengthMeasure | [1:1] | The distance between the position of the center point of the BTS site and the vertical alignment curve at the corresponding mileage |
| 7 | Side | [IfcBoolean](mailto:IfcAlignment2DVertical@Segment) | [1:1] | Left or right side of alignment |

## 6. **Attachment**

1. UT_DEP_4_case 1_A document containing the [linear placement parameters](#Linear placement of Base Transceiver Station(BTS)) [.doc]
2. UT_DEP_4_case 2_The IFC model of the BTS site [.ifc]
3. UT_DEP_4_case 3_Linear placement of the 5 BTS sites [.dwg]
4. UT_DEP_4_case 4_ Linear Placement of Base Transceiver Station(BTS) Data[.xlsx]
