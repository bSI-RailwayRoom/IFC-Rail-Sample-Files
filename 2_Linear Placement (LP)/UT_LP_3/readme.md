# Unit Test: Linear placement of sleeper

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Linear placement of sleeper and fastener |   UT_LP_3 | Claude Marschal | SBB | xlsx | |

## Prerequisites
This Unit Test intends to experiment the use of IFC for representing the linear placement of sleeper. In the dataset, the placement of the sleeper is lineary referenced to the alignment curve. 

The dataset refers to the alignment curve provided in file UT_LP_3_Alignment.XTR. The dataset includes 182 positions of sleepers that are placed according to the alignment curve. 

The specificities of this unit test are:
- The distance along for the placement of the sleeper is the distance measured according to the projection of the alignment in the horizontal plane i.e., according to the horizontal alignment curve.
- The rotation of the sleeper depends on cant
- The geometry of the sleeper is simplified

The dataset is provided by SBB, see [Dataset Description](#data-description) section for details.


## Prerequisites
None

To know the IFC scope for this test (which entities and concept templates are involved), please check the [LP](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/readme.md) Topic readme

## Data Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/2_Linear%20placement%20(LP)/UT_LP_3/Dataset) is currently made of:
1. A spreadsheet containing the  explanation for context, alignment, linear referencing and sleeper testdata
2. A [data snippet](#data-snippet) for sleeper of the table above [.PNG]
3. The IFC model of the sleeper [UT_LP_3_Sleeper.ifc]
5. A picture explaining the [use of the placement parameters](#use-of-the-placement-parameters) [.PNG]
6. A picture explaining the origin of the sleeper, for rotation purposes [.jpg]

---
### Linear placement parameters

The spreadsheet contains the linear placement parameters. The meaning of the columns in the spreadsheet is explained below (from left to right).

1. **id**: defines the unique identifier of the sleeper
2. **type**: defines the type of sleeper
3. **LP-Curve**; defines the id of the alignment curve on which the sleeper are linear positioned
4. **LP-Dist**: defines the distance along the alignment curve, the distance is measured according to the projection of the alignment in the horizontal plane, i.e., the horizontal alignment curve.
5. **LP-Lateral**: defines the distance between the position of the origin of the sleeper (inserion point) and the horizontal alignment curve at LP-Dist. This distance is measured along the axis that is perpendicular to the tangent of the horizontal alignment curve at LP-Dist. The offset is always 0
6. **LP-Vertical**: defines the distance between the position of the origin of the sleeper and the vertical alignment curve at LP-Dist. This distance is measured along the vertical axis of the general coordinate system. A negative Vertical offset indicates that, in the general coordinate system, the vertical coordinate of the vertical alignment curve at LP-Dist is greater than the vertical coordinate of the origin of the post. 

### Data snippet
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_3/Dataset/UT_LP_3_Sleeper.png)

### Use of the placement parameters
Below is a picture explaining the use of vertical an lateral offset parameters. The point (A) represent the alignment curve.

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_3/Dataset/UT_LP_3_Positioning.png)

**NOTE**:




