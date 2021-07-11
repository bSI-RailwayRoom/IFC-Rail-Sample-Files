# Unit Test: Single Domain Spatial Structure

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Single Domain Spatial Structure |   UT_RSS_1 | Evandro Alfieri, Giulia Minnucci| RFI | text, images |  |


## General
This Unit Test intends to experiment the use of IFC to represent the project breakdown for a single domain spatial structure. 
The single domain taken as an example for this test is "Track". 

The dataset refers to a simple railway network, represented by using the paradigma "Node-Edge-Node" (further explained in the [Dataset Description](#data-description) section), and broken down using  asset management criteria.  

As the aim of the Unit Test is to implement the spatial structure, there is no need for the moment to introduce elements contained within.  

The dataset is provided by RFI, see [Dataset Description](#data-description) section for details.


## Prerequisites
This Unit Test does not have any pre-requisites. 

To know the IFC scope for this test (which entities and concept templates are involved), please check the [RSS](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/4_Railway%20Spatial%20Structure%20(RSS)) Topic readme.

## Data Description

The [dataset](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset) is currently made of:
1. A picture representing the simple Railway Network through the "Node-Edge-Node" paradigma: [Rome-Naplels Network](#rome-naples-network) [.PNG]
2. A picture explaining the [Network decomposition](#network-decomposition) [.PNG] 
3. A picture explaining the [higher level spatial structure](#higher-level-spatial-structure) [.PNG]
6. A picture explaining the [Network spatial structure](#network-spatial-structure) to be represented in the model [.PNG]

---
### Project Breakdown: 

In this Unit Test the example project is a simple railway Network connecting two stations, Rome and Naples. 
Using the "Node-Edge-Node" criteria, the Rome-Naples Netwok is composed by two "Nodes" and one "Edge", as shown in the following picture:

#### Rome-Naples Network
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset/Rome-Naples_Network.png)

Each "Node" represents the area of the station as it is considered by the Track domain.

For the scope of this specific example, only one Node (i.e.Rome) and the Edge are further decomposed as follows:

The chosen Node, Rome, is decomposed in the following parts:
- Two tracks, named **T1** and **T2**,
- One siding track, named **T3**,
- Two sidewalks, one for Track T1 named **Sidewalk1** and one for Track T2 named **Sidewalk2**

The Railway Line, is decomposed in the following parts: 
- Two tracks, named **T1** and **T2**.
 
Additionally, in this Network there is an area crossing (overlapping) the Railway Line, in which there could be elements that constitute an **interference**, which are not part of the Railway Line decomposition itself. It is necessary to represent this area in the model, to make sure that any such interefence is taken into consideration when managing the Network.  

The following picture shows the Network decomposition as explained above. 

#### Network Decomposition  
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset/Network%20Decomposition.png)

To represent the project breakdown in the model, the spatial structure as defined in IFC 4.3 shall be used. 

Therefore, the higher level structure shall be:
- The **Network** shall be represented as an IfcSpatialstructureElement, specifically  **IfcRailway** (sub-entity of IfcFacility). It shall have the following attributes:
  - **Name**: Rome-Naples Network


- The **Edge**  shall be represented as an IfcSpatialstructureElement, specifically **IfcRailway** (sub-entity of IfcFacility). It shall have the following attributes:
  - **Name**: Railway Line
  

- The **Node** shall be  represented as an IfcSpatialstructureElement, specifically **IfcRailway** (sub-entity of IfcFacility). It shall have the following attributes:
  - **Name**: Rome



The picture below shows the spatial structure as described above: 
#### Higher level spatial structure
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset/High%20level%20SSR.png)


 
 The Network decompoisition shall be further represented using the spatial structure concepts of IfcFacilityPart.

 In particular:

The chosen Node, Rome, is decomposed in the following parts:
- Two tracks:
  - **T1** shall be represented as **IfcFacilityPart**, with the following attributes:
    - Name: T1
    - PredefinedType*: IfcRailwayPartTypeEnum.TRACKSTRUCTUREPART
    - UsageType: LONGITUDINAL
  
  - **T2** shall be represented as **IfcFacilityPart**, with the following attributes:
    - Name: T2
    - PredefinedType*: IfcRailwayPartTypeEnum.TRACKSTRUCTUREPART
    - UsageType: LONGITUDINAL
   
- One siding track, represented as  as **IfcFacilityPart**, with the following attributes:
    - Name: T3
    - PredefinedType*: IfcRailwayPartTypeEnum.TRACKSTRUCTUREPART
    - UsageType: LONGITUDINAL 
         
- Two sidewalks, also represented as **IfcFacilityPart**
  - one for Track T1, with the following attributes:
    - Name: **Sidewalk1** 
    - PredefinedType*: IfcRailwayPartTypeEnum.LINESIDESTRUCTUREPART
    - UsageType: LATERAL

  - one for Track T2, with the following attributres: 
    - Name: **Sidewalk2** 
    - PredefinedType*: IfcRailwayPartTypeEnum.LINESIDESTRUCTUREPART
    - UsageType: LATERAL

The Railway Line, is decomposed in the following parts: 
- Two tracks, represented as the ones in the Node, but as a part of the Railway Line: 
  - **T1** shall be represented as **IfcFacilityPart** of IfcRailway(Partial): Railway Line, with the following attributes:
    - Name: T1
    - PredefinedType*: IfcRailwayPartTypeEnum.TRACKSTRUCTUREPART
    - UsageType: LONGITUDINAL

  - **T2** shall be represented as **IfcFacilityPart** of IfcRailway(Partial): Railway Line, with the following attributes:
    - Name: T2
    - PredefinedType*: IfcRailwayPartTypeEnum.TRACKSTRUCTUREPART
    - UsageType: LONGITUDINAL
 
 _* the PredefinedType enumeration is selected through "IfcFacilityPartTypeSelect"_.

 Additionally, the **interference** area shall be represented as an **IfcSpatialZone** with the following attributes:
  - Name: Interference Area
  - InterferenceType: PASSESUNDER
  
This IfcSpatialZone is referenced by the Railway Line using **IfcRelReferencedInSpatialStructure**.

To better represent the interference with T1 and T2 of the Railway Line, the following relationship shall be used: 
**IfcRelInterferesElement**.

The following picture summarizes the Network representation using the spatial structure concepts of IfcFacility, IfcFacilityPart and IfcSpatialzone. 

#### Network Spatial Structure
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset/Network%20Spatial%20Structure.png)

#### Spatial Structure Overview
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset/SpatialStructureOverview.png)


---
### Expected Results

The aim of this Unit Test, as explained above, is to test the implementation of the project breakdown through the spatial structure concepts of IFC 4.3.

As such, the expected results are:

1. Screen-shot of the spatial structure breakdown as represented in the native application,
2. The resulting IFC file containing the spatial structure requested.

For example, the application should be able to display something like what is shown in the picture below: 

#### Project Breakdown Browser
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/4_Railway%20Spatial%20Structure%20(RSS)/UT_RSS_1/Dataset/Project_breakdown_browser.png)
