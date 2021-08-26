# Unit Test: Group Assignment

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Group Assignment |   UT_SYS_1 | Evandro Alfieri, Giulia Minnucci| RFI | text, images, excel |  |


## General
This Unit Test is the first of a series of tests, each one building on the previous step. The final goal is to provide the user with a functional view of the content of the model which is detached and decoupled from the spatial structure tree. This functional perspective (grouping) shall be defined by the user, using different criteria, and may change across the life-cycle of a model. The focus of this test is: first on the definition of the semantics of the relationships between the objects; then on the test of a panel/window in the UI of a tool, for the purpose of visualisation and navigation of the functional network.

For the scope of this UT, the TLC domain was taken as an example.

The dataset refers to a simple railway Node, (further explained in the [Dataset Description](#data-description) section), which contains a list of elements grouped according to functional aspects.

As the aim of the Unit Test is to implement group assignment, there is no need for the moment to go further into the relationship between the Node and the functional groups.

The dataset is provided by RFI, see [Dataset Description](#data-description) section for details.


## Prerequisites
Understanding the single domain spatial structure used in [UT_RSS_1](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1).

To know the IFC scope for this test (which entities and concept templates are involved), please check the [SYS](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)) Topic readme.

## Data Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1/Dataset) is currently made of:
1. A picture representing the Railway Node breakdown: [TLC Node and spatial containment](#TLC-node-and-spatial-containment)[.PNG];
2. A [Table_IFC Entities](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1/Dataset/Table_IFC%20Entities.csv)[.csv] that defines the IFC Entities for the Node Breakdown;
3. A [Table_TLC Node breakdown](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1/Dataset/Table_Node%20TLC%20Breakdown.csv)(.csv) containing the elements contained in TLC Node to be used for this UT;
4. A [Table_ Grouping of Elements](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1/Dataset/Table_Grouping%20of%20elements.csv)(.csv) defining the required collection in functional groups;
5. A picture that shows the overview of the [System breakdown](#system-breakdown-overview)[.PNG] requested.

---
### Project Breakdown:

In this Unit Test the example project is represented by a single railway Node (for clarification, please check the [Prerequisites](#prerequisites)). In particular, a TLC Node was selected, together with some elements contained within.

The following picture shows the TLC Node and all the elements contained within. However, for the scope of this UT, we will consider just some of these elements, as stated in the [Table_TLC Node breakdown](#Data-description).

#### TLC Node and spatial containment
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1/Dataset/SpatialContainment.png)

The TLC Node shall be defined as an *IfcSpatialStructureElement*, and in particular as an:
-  *IFcRailway* (subtype of IfcFacility)
    - Name: TLC Node

 The elements taken into consideration shall de defined as:
 -  *IfcBuiltElement*

*IfcRelContainedInSpatialStructure* shall be the relationship used for spatial containment.

*NOTES*:
- *For the scope of this test, only some elements from those shown in the picture have been taken into consideration, as shown in the dataset table.*
- *The shape of the IfcBuiltElement is not relevant. If provided, it can be a simple geometrical shape like a bounding box.*


### System Breakdown and group assignment

Each element shall be collected in a functional group, as shown in the [Table_ Grouping of Elements](#data-description).
The table has 2 columns:
- "RelatedObjects", in which all objects to be grouped are listed by name.
- "RelatingGroup", where the groups to which the objects are assigned are listed by name.

Each object listed in the "RelatedObjects" column shall be assigned to the corresponding group in the "RelatingGroup" column.
The groups shall be 6 in total (as shown also in the table):
- 1 IfcGroup
   - Name: Sistemi Radio Frequenza
- 1 IfcGroup
   - Name: Aggregatore Stazioni Radio Base
- 1 IfcAsset
   - Name: Impianto radiomobile 01
- 1 IfcAsset
   - Name: Impianto radiomobile 02
- 1 IfcSystem
   - Name: Base Station controller (BSC)
- 1 IfcSystem
   - Name: Stazione Radio Base (BTS)

*IfcRelAssignsToGroup* shall be the relationship linking the objects in the "RelatedObjects" column to the respective group in the "RelatingGroup" column.


*Note: for the scope of this test, only the objects assigned to one IfcAsset have been taken into consideration. However, the IfcGroup (Name: Sistemi Radiofrequenza) is to be considered as a non hierarchical collection of multiple IfcAsset (Impianto radiomobile 01..02). Please note that the IfcSystem is assigned both to an IfcAsset and to an IfcGroup. That is beacause the relationship is non hierarchical, but functional.*

As an example, there is the [Table_IFC Entities](#data-description) and an overview of the system breakdown in the picture below.

#### System Breakdown Overview
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_1/Dataset/System%20breakdown%20overview.png)

*IfcRelDeclares* shall be the relationship linking all groups to the project (See IFC4.3RC2 documentation for IfcProject, section 5.2.3.11.3).

---
### Expected Results

Considering the aim of this UT, the expected results are:
1. Screen-shot of the project breakdown as represented in the native application, according to the Node TLC breakdown.
2. Screenshot of the functional (groups) breakdown, as represented in the native application. For the moment, it is recommended for it to be a separate  visualization than the one requested in point 1.
2. The resulting IFC file containing the information as requested.



