# Railway Spatial Structures & zones

|              Topic title                  |Topic ID|
|:-----------------------------------------:|:------:|
|  Railway Spatial Structure                |   RSS  |


## Associated Unit Tests

Please contact @MatthieuPERIN to reserve UT in RSS topic, "WIP/" prefixed UT are Work In Progress

| N |   Unit Test title                                                   |Unit Test ID                      |    Full Unit Test name   |
|:-:|:--------------------------------------------------------------------|:--------------------------------:| :-----------------------:|
| 1 | Single Domain Spatial Structure  	                                  |  [UT_RSS_1](UT_RSS_1/README.md)  | RSS_UT1_RFI              |
| 2 | Early design Railway spatial structure                              |  [UT_RSS_2](UT_RSS_2/README.md)  | RSS_UT2_M4R              |
| 3 | Spatial structure with geometry for duct clearance check            |  [UT_RSS_3](UT_RSS_3/README.md)  | RSS_UT3_M4R              |
| 4 | Multiple Domain Spatial Structure (railway, road, level crossing)   |  [UT_RSS_4](UT_RSS_4/README.md)  | RSS_UT4_NOR              |
| 5 | Road & Railway urban crossing detailed spatial structure            |  [UT_RSS_5](UT_RSS_5/README.md)  | RSS_UT5_M4R              |
| 6 | WIP / Railway spatial structure with alignment-based geometry       |   UT_RSS_6                       | RSS_UT6_M4R              |



## Intent
The Unit Tests associated to this Topic are meant to prove the possibility to allocate space and volume inside a railway project. The unit test shall cover the following usages:

- Spatial structure of Railway projects
  - Use high level spatial decomposition for Railway projects
  - Allocate spacial structure for each Domain (Track, Signalling, Telecom & Energy) within a railway project
  - Based on usage of IfcRelAggregates and IfcRelContainedInSpatialStructure 
- Spatial Zone usage
  - Use of Railway-specific Spatial Zone when domain need to share space
  - Use of several Spatial Zone to sort usage of highly shared spaces
  - Based on usage of IfcRelReferencedInSpatialStructure 
- Spatial structure of mixed project
  - Use of Railway Spatial structure in conjunction with Infrastructure or Building Spatial structure for mixed project.
  - Use of Railway Spatial Zone with non Railway spatial structure for foreign space usage on neighbouring infrastructure/buildings.
  - Based on teh usage of IfcRelInterferesElements

## IFC scope
- Dependant on topics
  - Infrastructure Spatila Structures (Bridge, Marine, Road) for mixed projects
- Required IFC concept templates
  - **Existing**:
    - [Spatial Composition](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/spatial-composition.htm)
    - [Spatial Decomposition](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/spatial-decomposition.htm)    

- Focused IFC entities
  - **Existing**:
    - [IfcSite](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcsite.htm)
    - [IfcSpatialZone](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcspatialzone.htm)
    - [IfcFacility](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcfacility.htm)
    - [IfcFacilityPart](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcfacility.htm)
    - [IfcBuilding](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcbuilding.htm)
    - [IfcRelAggregates](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcrelaggregates.htm)
    - [IfcRelContainedInSpatialStructure](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcrelcontainedinspatialstructure.htm)
    - [IfcRelReferencedInSpatialStructure](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcrelreferencedinspatialstructure.htm)
    - [IfcRelInterferesElements](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcrelinterfereselements.htm)
    
  - **New**:
    - [IfcBridge](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcbridge.htm)
    - [IfcRailway](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcrailway.htm)
    - [IfcRoad](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcroad.htm)
    - [Pset_RailwayFacility](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/pset_railwayfacility.htm)
    - [Pset_RailwayPart](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/pset_railwaypart.htm)


## REF. to Conceptual Model Report
- Common : 6.4
- Track : 2.2
- Signalling : 3.2
- Telecom : 4.2
- Energy : 5.2 

## REF. to Mapping Diagram Report
Section 6.2 in completly about RSS

## Concept templates
- TBD
