# Unit Test: Linear placement of catenary posts

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Linear placement of catenary posts |   UT_LP_1 | Evandro Alfieri | RFI | xlsx |  |


## General
This Unit Test intends to experiment the use of IFC for representing the linear placement of the catenary posts. In the dataset, the placement is described as a set of parameters related to the alignment curve. 

The dataset refers to the alignment curve provided in UT_AWC_4, without the cant layout. The dataset includes 84 posts that are placed according to the alignment curve. One type of post is used: LSU14a. 

The peculiarities of this unit test are:
- There is no parameter that depends on cant
- The distance between the posts along the curve is measured according to the projection of the alignment curve onto the horizontal plane, i.e., according to the horizontal alignment curve.
- The only rotation of the posts is around its vertical axis. 
- The geometry of the posts type is simplified
    - The cantilever part of the pole is out of scope for this test, so its height is considered fixed for the specific type of post.

The dataset is provided by RFI/Itaferr, see [Dataset Description](#data-description) section for details.


## Prerequisites
This Unit Test builds upon following Unit Test:
- UT_AWC_4, stripped of its cant part. Please consider only Horizontal and Vertical alignments

To know the IFC scope for this test (which entities and concept templates are involved), please check the [LP](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/readme.md) Topic readme

## Data Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/2_Linear%20placement%20(LP)/UT_LP_1/Dataset) is currently made of:
1. A spreadsheet containing the [linear placement parameters](#Linear-placement-parameters) [.xlsx]
2. A [data snippet](#data-snippet) of the table above [.PNG]
3. The IFC model of the post type with the cantilever [.ifc]
4. A picture of the post type with the cantilever [.PNG]
5. A picture explaining the [use of the placement parameters](#use-of-the-placement-parameters) [.PNG]
6. A picture explaining the origin of the post, for rotation purposes [.jpg]
7. *(to be provided)* a picture of the linear placement of the 84 posts

---
### Linear placement parameters

The spreadsheet contains the linear placement parameters. The meaning of the columns in the spreadsheet is explained below (from left to right).

1. **Post occurrence**: defines the id of the post
2. **Point type**: defines the type of post, in this dataset only one type is used (LSU14a)
3. **(pk)**: defines the distance along the alignment curve, the distance is measured according to the projection of the alignment in the horizontal plane, i.e., the horizontal alignment curve.
4. **Lateral offset**: defines the distance between the position of the origin of the post and the horizontal alignment curve at (pk). This distance is measured along the axis that is perpendicular to the tangent of the horizontal alignment curve at (pk). The offset is always a positive value. The direction of the offset is defined by the “Side” parameter. The direction of the offset is defined by the “Side” parameter.
5. **Vertical offset**: defines the distance between the position of the origin of the post and the vertical alignment curve at (pk). This distance is measured along the vertical axis of the general coordinate system. A negative Vertical offset indicates that, in the general coordinate system, the vertical coordinate of the vertical alignment curve at (pk) is greater than the vertical coordinate of the origin of the post. 
6. **Side**: defines on which direction the “offset” parameter applies. 
    - **Left**: “offset” applies to the left of the alignment curve, as facing in the direction of the basis curve
    - **Right**: “offset” applies to the right of the alignment curve, as facing in the direction of the basis curve

### Data snippet
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_1/Dataset/UT_LP_1_DataSnippet.PNG)

### Use of the placement parameters
Below is a picture explaining the use of verticl an lateral offset parameters. The point (A) represent the alignment curve.

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_1/Dataset/UT_LP_1_LateralAndVerticalOffset.png)

**NOTE**:
- All measures are expressed in meters. 
- Post occurrence #1 is placed at (pk) = 0, and it represents the post placed at the START point of the alignment curve of the UT_AWC_4. 
- The vertical axis of the posts is always parallel to the vertical axis of the general coordinate system. The direction of the two axes is always the same. 
- The y axis of the posts is always parallel to the tangent of the horizontal alignment curve at (pk). Analogously, the x axis of the posts is always perpendicular to the tangent of the horizontal alignment curve at (pk).
- The direction of the y axis of the post depends on the placement side of the post itself. When facing in the direction of the alignment curve, the post that is placed on the left side of the curve has its y axis concordant with the direction of the curve, as shown by the figure below (LEFT). Alternatively, the post that is placed on the right side of the curve has its y axis discordant with the direction of the curve, as shown by the figure below (RIGHT).

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_1/Dataset/UT_LP_1_PostOriginForRotation.jpg)


