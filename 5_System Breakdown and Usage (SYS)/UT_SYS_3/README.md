# Unit Test: Group Assignment

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Pset association to groups |   UT_SYS_3 | Evandro Alfieri, Giulia Minnucci| RFI | text, images, excel|  |


## General
This Unit Test is the third of a series of tests, each one building on the previous step. The final goal is to provide the user with a functional view of the content of the model which is detached and decoupled from the spatial structure tree. This functional perspective (grouping) shall be defined by the user, using different criteria, and may change across the life-cycle of a model.

As for the other UTs in this topic, the focus of this test is: first on the definition of the semantics of the relationship between groups and spatial structure elements; then on the test of a panel/window in the UI of a tool, for the purpose of visualisation and navigation of the functional network.

Part of the dataset is the same as the one for UT_SYS_1 and UT_SYS_2,  a simple railway Node, (further explained in the [Dataset Description](#data-description) section), which contains a list of elements grouped according to functional aspects.

The dataset is provided by RFI, see [Dataset Description](#data-description) section for details.


## Prerequisites
This UT is built upon  [UT_SYS_2](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_2).

To know the IFC scope for this test (which entities and concept templates are involved), please check the [SYS](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)) Topic readme.

## Data Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_3/Dataset) is currently made of:
1. The dataset of [UT_SYS_2](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_2) or the resulting IFC file from it;
2. A picture showing the [Property Sets associated to gorups](#Property-Sets-associated-to-gorups);
3. A [Table of Pset reference](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/SYS_topic/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_3/Dataset/Table%20of%20Pset%20reference.csv), describing the Property Sets to be associated to each group;
4. A [Table of properties](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/SYS_topic/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_3/Dataset/Table%20of%20properties.csv), listing the properties contained in each Property Set and their values.

---
### Project Breakdown:

In this Unit Test the example project is the one for UT_SYS_1 and UT_SYS_2 (for clarification, please check the [Prerequisites](#prerequisites)). In particular, a TLC Node was selected, together with some elements contained within.

As stated in UT-SYS-1 and UT_SYS_2, the TLC Node shall be defined as an **IFcRailway** (subtype of IfcFacility), with "Name: TLC Node".

 The elements selected in UT_SYS_1 shall de defined as **IfcBuiltElement**.

**IfcRelContainedInSpatialStructure** shall be the relationship used for spatial containment.

According to UT_SYS_1, each element shall be collected in a functional group and there shall be 6 groups in total.

According to UT_SYS_2, the group "Sistemi Radio Frequenza"  shall be referenced to the TLC Node through the **IfcRelReferencedInspatialStructure** relationship.

For the sake of this UT, there are 3 relevant Property Sets to be considered and named as follows:
1. PSET_Asset_Impianto radiomobile
2. PSET_System_BSC
3. PSET_System_BTS

As the name of the Pset says, the first one applies to all Assets of the type "Impianto radiomobile", while the second applies to all Systems of type "BSC" and the third to all Systems of type "BTS".
Thus, according to this, these Psets shall be associated to the correct assets/systems through the **IfcRelDefinesByProperties** relationship.

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_3/Dataset/Property%20Sets%20associated%20to%20groups.png)

#### Table of Pset reference

The [table](#data-description) has 2 columns:
- "RelatedObjects", in which all groups that have a Property Set are listed.
- "RelatingPropertyDefinition", where the Property Set  associated to each group is listed.

### Table of properties
The [table](#data-description) has 4 columns:
- IfcPreopertySet
- IfcPreoperty
- Value
- Type
- Shared

 It describes which properties each Property Set has, which values are requested for each property, and the required type for each property. The last column specifies if the property is shared with other PSets.

---
### Expected Results

Considering the aim of this UT, the expected results are:
1. Screen-shot of the project breakdown as represented in the native application, according to the Node TLC spatial structure breakdown.
2. Screenshot of the functional (groups) breakdown, as represented in the native application. For the moment, it is recommended for it to be a separate  visualization than the one requested in point 1.
3. Screenshot that shows the relationships used as requested.
4. The resulting IFC file containing the information as requested.



