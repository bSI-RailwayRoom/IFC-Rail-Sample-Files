# Unit Test: Multiple Domain Spatial Structure (railway, road, level crossing)
|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
| Level crossing Spatial Structure |   UT_RSS_4 | Lars Wikström, Marion Schenkwein | FTIA | text, images |  |


## General
This Unit Test intends to experiment the use of IFC to represent the project breakdown for a road/railway level crossing spatial structure with an explicitly modelled relationship between the railway facility part and the corresponding road facility part representing the overlapping of the two facilities.   

As the aim of the Unit Test is to implement the spatial structure, there is no need for the moment to introduce elements contained within.  

The dataset is provided by FTIA, see [Dataset Description](#data-description) section for details.


## Prerequisites
This Unit Test does not have any pre-requisites. 

To know the IFC scope for this test (which entities and concept templates are involved), please check the [RSS](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/4_Railway%20Spatial%20Structure%20(RSS)) Topic readme.

## Data Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset) is currently made of:

1. A project + site
2. A road facility with three facility parts where the level crossing overlaps the corresponding railway facility part 
3. A railway facility with three facility parts where the level crossing overlaps the corresponding road facility part
4. The explicit interference relationship between the overlapping facility parts

---
### Situation:

![](./Dataset/Figure%201%20-%20situation.png)

### Project Breakdown: 

To represent the project breakdown for this unit test, we envision the following project structure:

- A. IfcProject
  - A.a IfcSite
    - IfcGeoModel (or similar representing terrain - optional for this unit test)
    - A.a.1 IfcRoad
      - IfcAlignment (optional for this unit test)
      - A.a.1.1 IfcFacilityPart
        - PredefinedType*=IfcRoadPartTypeEnum.ROADSEGMENT
        - UsageType=LONGITUDINAL
      - A.a.1.2 IfcFacilityPart
        - PredefinedType*=IfcFacilityPartCommonTypeEnum.LEVELCROSSING
        - UsageType=LONGITUDINAL
      - A.a.1.3 IfcFacilityPart
        - PredefinedType*=IfcRoadPartTypeEnum.ROADSEGMENT
        - UsageType=LONGITUDINAL
    - A.a.2 IfcRailway
      - IfcAlignment (optional for this unit test)
      - A.a.2.1 IfcFacilityPart
        - PredefinedType*=IfcRailwayPartTypeEnum.TRACKSTUCTUREPART
        - UsageType=LONGITUDINAL
      - A.a.2.2 IfcFacilityPart
        - PredefinedType*=IfcFacilityPartCommonTypeEnum.LEVELCROSSING
        - UsageType=LONGITUDINAL
      - A.a.2.3 IfcFacilityPart
        - PredefinedType*=IfcRailwayPartTypeEnum.TRACKSTRUCTUREPART
        - UsageType=LONGITUDINAL
- IfcRelInterferesElements 
  - InterferenceType="Crosses"
  - RelatingElement=#A.a.1.2
  - RelatedElement=#A.a.2.2
  - InterferenceGeometry=optional for this unit test

_* the PredefinedType enumeration is selected through "IfcFacilityPartTypeSelect"_.


---
### Expected Results

The aim of this Unit Test, as explained above, is to test the implementation of the project breakdown through the spatial structure concepts of IFC 4.3.

As such, the expected results are:

1. Screen-shot of the spatial structure breakdown as represented in the native application,
2. The resulting IFC file containing the spatial structure requested.

For example, the application should be able to display something like what is shown in the picture below: 

#### Project Breakdown Browser

![](./Dataset/Figure%202%20-%20result.png)