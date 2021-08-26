# Unit Test: Group Assignment

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Group reference to spatial structure |   UT_SYS_2 | Evandro Alfieri, Giulia Minnucci| RFI | text, images, excel|  |


## General
This Unit Test is the second of a series of tests, each one building on the previous step. The final goal is to provide the user with a functional view of the content of the model which is detached and decoupled from the spatial structure tree. This functional perspective (grouping) shall be defined by the user, using different criteria, and may change across the life-cycle of a model. 

The focus of this test is: first on the definition of the semantics of the relationship between groups and spatial structure elements; then on the test of a panel/window in the UI of a tool, for the purpose of visualisation and navigation of the functional network.

The dataset is the same as the one for UT_SYS_1,  a simple railway Node, (further explained in the [Dataset Description](#data-description) section), which contains a list of elements grouped according to functional aspects.  

The dataset is provided by RFI, see [Dataset Description](#data-description) section for details.


## Prerequisites
This UT is built upon  [UT_SYS_1](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1). 

To know the IFC scope for this test (which entities and concept templates are involved), please check the [SYS](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)) Topic readme.

## Data Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_2/Dataset) is currently made of:
1. The dataset of [UT_SYS_1](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1) or the resulting IFC file from it;
2. A picture showing the [Reference to the spatial structure element](#reference-to-spatial-structure);
3. A [Table of reference](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/SYS_topic/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_2/Dataset/Table%20of%20reference.csv), describing the required relationship to be used to reference the group to the spatial structure.

---
### Project Breakdown: 

In this Unit Test the example project is the one for UT_SYS_1 (for clarification, please check the [Prerequisites](#prerequisites)). In particular, a TLC Node was selected, together with some elements contained within.

As stated in UT-SYS-1, the TLC Node shall be defined as an **IFcRailway** (subtype of IfcFacility), with "Name: TLC Node".
 
 The elements selected in UT_SYS_1 shall de defined as **IfcBuiltElement**. 
     
**IfcRelContainedInSpatialStructure** shall be the relationship used for spatial containment. 

According to UT_SYS_1, each element shall be collected in a functional group and there shall be 6 groups in total. 

For the business need of RFI, in this UT it is required that one specific group shall be referenced to the TLC Node through the **IfcRelReferencedInspatialStructure** relationship.

The group to be referenced shall be: 
- IfcGroup
  - Name: Sistemi Radio Frequenza

#### Table of reference

The [table](#data-description) has 2 columns:
- "RelatedElements", in which all groups to be referenced are listed by name.  
- "RelatingStructure", where the spatial elements to which the groups are referenced are listed by name.

Each group listed in the "RelatedElements" column shall be referenced to the corresponding spatial element in the "RelatingStructure" column, through **IfcRelReferencedInspatialStructure**. 

#### Reference to spatial structure
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_2/Dataset/reference_spatial_structure.png)
---
### Expected Results

Considering the aim of this UT, the expected results are:
1. Screen-shot of the project breakdown as represented in the native application, according to the Node TLC spatial structure breakdown. 
2. Screenshot of the functional (groups) breakdown, as represented in the native application. For the moment, it is recommended for it to be a separate  visualization than the one requested in point 1. 
3. Screenshot that shows the relationships used as requested.
4. The resulting IFC file containing the information as requested.



