# Unit Test: Alignment with Cant 4

|              Unit Test title                  | ID| Author | Data Owner | Format | Software Vendors | 
|:-----------------------------------------:|:------:|:------:| :------:| :------:| :------:|
|  Alignment with Cant 4 |   UT_AWC_4 | Evandro Alfieri | RFI | xlsx / LandXML |  |

## Table of content
- [General](#general)
- [Prerequisites](#prerequisites)
- [Dataset description](#dataset-description)

## General
This Unit Test intends to experiment the use of IFC for representing a railway alignment curve, starting from its parameters.

The porovided parameters describe the alignment of a railway track of about 3,7 km between two nodal points. Visual representations of the track are provided below.

The peculiarities of this alignment curve are:
- cant presence
- a point of inflection
- an articulated vertical alignment

The dataset is provided by RFI/Itaferr, see [Dataset Description](#dataset-description) section for details.

EPSG code: 32632 (WGS 84 / UTM zone 32N)

IMPORTANT:
- In Italy, the vertical alignment is measured from the lower rail, as showed in the picture below.
- The `RailHeadDistance` is a normalized value used to compute the angle of cant. RFI uses 1500mm for a track gauge of 1435mm.

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_CantFromLowerRail.PNG)


## Prerequisites
This Unit Test builds upon following Unit Test:
- None

To know the IFC scope for this test (which entities and concept templates are involved), please check the [AWC Topic readme](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/README.md)

## Dataset Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset) is currently made of:
1. A spreadsheet containing the alignment parameters [**.xlsx**]
2. Table screenshoot + picture for the Horizontal alignment [**.PNG**]
3. Table screenshoot + picture for the Vertical alignment [**.PNG**]
4. Table screenshoot + picture for the Cant alignment [**.PNG**]
5. Alignment parameters **without cant** in LandXML [**.xml**]
6. Two pictures explainig cant [**.PNG**]

Inside the spreadsheet, the alignment parameters are provided in three separate sheets:
1. [Horizontal alignment segment](#horizontal-alignment)
2. [Vertical alignment segment](#vertical-alignment)
3. [Cant alignment segment](#cant-alignment)

---

### Horizontal Alignment
The meaning of the columns in the spreadsheet for the Horizontal Alignment is explained below (from left to right). **Please note** that *Spiral* is equal to *Clothoid* in the Point Type:

1. **Element type**:
    - Linear = straight line
    - Clothoid = transition curve used in Italy
    - Circular = arc curve
2. **Point Type** (start)
    - TS tangent to spiral 
    - SC spiral to curve 
    - CS curve to spiral 
    - ST spiral to tangent
    - SS spiral spiral
    - START starting point 
    - END ending point
3. **Station**: defines the point distance from the origin on the horizontal projection
4. **Start northing**: defines the start coordinate North
5. **Start easting**: defines the start coordinate East
6. **Start direction**: defines the Azimuth of the start point
7. **Point Type** (end): same as Point Type (start)
8. **End northing**: defines the end coordinate North
9. **End easting**: defines the end coordinate East
10. **End direction**: defines the Azimuth of the end point
11. **Length**: defines the length of the element (segment) on the horizontal projection
12. **Radius**: defines the Radius of the segment, only for “circular arc curve”

**NOTE**:
- All distances are in meters
- All angles are in gradian
- All the coordinates are defined using the UTM Coordinate System
- This case contains a reversing spiral [**TO BE CONFIRMED**]
- The radius is considered positive when the curve is to the right, and negative when it is to the left

#### Data snippet

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_Horizontal%20alignment%20image.png)

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_Horizontal%20alignment%20table.png)

---

### Vertical Alignment
The meaning of the columns in the spreadsheet for the Vertical Alignment is explained below (from left to right):

1. **Element type**:
    - Linear = straight line
    - Circular = arc curve
2. **Point Type** (start):
    - VPC Vertical point of curvature 
    - VPT Vertical point of tangency 
    - START point of beginning 
    - END point of ending
3. **Start Station**: defines the point distance from the origin, on the horizontal projection
4. **Start Elevation**: defines the start elevation:
5. **Start Gradient**: defines the Zenith angle of the start point
6. **Point Type** (end): same as Pont Type (start)
7. **End Station**: defines the point distance from the origin, on the horizontal projection
8. **End Elevation**: defines the end elevation:
9. **End Gradient**: defines the Zenith angle of the end point
10. **R**: defines the vertical circular radius of the segment.

**NOTE**:
- All distances are in meters
- All angles are in gradian
- The radius (**R**) is considered positive when the curve is convex, and negative when it is concave

#### Data snippet

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_Vertical%20alignment%20image.png)

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_Vertical%20alignment%20table.png)

___

### Cant Alignment
The meaning of the columns in the spreadsheet for the Cant Alignment is explained below (from left to right). **Please note** that *Spiral* is equal to *Clothoid* in the Point Type:

1. **Type**: is the type of point
    - TS tangent to spiral 
    - SC spiral to curve 
    - CS curve to spiral 
    - ST spiral to tangent
    - SS spiral spiral
    - START starting point 
    - END ending point
2. **Station**: defines the point distance from the origin, on the horizontal projection
3. **Speed**: parameter used to calculate cant (may be used used for validation)
4. **Radius**: the radius of the curve that, in the horizontal alignment, starts/ends in that station point
5. **Transition**: the type of transition curve that, in the horizontal alignment, stays between that station point and the next one
6. **Applied cant**: in a cross-section plane, orthogonal to the track axis, it is the difference in height (h<sub>t</sub> in the picture below) between two points, of the track plane, that have a conventional distance between them of 1500 mm. The cant is always applied to the external rail (the furthest rail from the center or the curve). Cant measure is positive because the external rail of a track is always higher than the internal rail.

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_Cant-CantAngle.png)

**NOTE**:
- In Italy, only straight line is used for cant segment
- All distances are in meters, except the Cant that is in millimiters
- All angles are in gradian
- Speed is in kilometers per hour (km/h)
- The radius (**R**) is considered positive when the curve is to the right, and negative when it is to the left


#### Data snippet

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_Cant%20alignment%20image.jpg)

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_4/Dataset/UT_AWC_4_Cant%20alignment%20table.PNG)



