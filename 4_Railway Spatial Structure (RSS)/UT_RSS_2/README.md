# Unit Test: Early design Railway spatial structure

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  Railway & infra spatial structure project |   UT_RSS_2 | Vincent Keller| MINnD4Rail | PPT + DataSet | TBD |


## General
This Unit Test intends to test the capablity to have a project based on a existing ifcSite that contains an IfcRailway spatial structure. These Railway structures is then veiw with another ifc file that is containing surrounding Roads & Tunnels.

---
## Prerequisites

### IFC projects
* IfcTunnel spatial structure (or IfcFacilityPart for remplacement)
* IfcRoad spatial structure

### Software vendor
* IfcSite import/use capability
* Suppprt for IfcTunnel and/or IfcRoad
* Support for Spatial structure links (IfcRelAggregates)

---
## Data Description

* Use case: urban railway:  
![urban railway](Dataset/UT_RSS_2_SAN01_SAN02.png)

* Railway topology:  
![topology](Dataset/UT_RSS_2_topo.png)

* Spatial structure description:  
![spatial structure description](Dataset/UT_RSS_2_DataSet.png)

### Project Breakdown: 

The Railway construction site is separated into 4 Sites:
* SAN01: Part of the road & urban railway with a Tunnel and some platforms. **Main DataSet of the UT**
* SAN02: Part of the road & urban railway. **Not used in the UT**
* SAN03: Part of the road & urban railway. **Not used in the UT**
* Depot: Part of the road & urban railway. **Not used in the UT**


#### SAN01 (IfcSite)

**This is the core of the UT to test spatial structure organization.**

This Site hold a complete spatial structure of an urban railway with:
* IfcRailway for the railway infrastructure, composed of:
  * Two double Lines (Railway 1 & 3)
  * two single Lines (Railway 2a & 2b)
* IFcRoad x 8
* Tunnel (IfcFacility for test purpose)

### Detail of the Objects

#### Rail Project

* IfcProject: Rail
  * HasName: Urban Railway
* IfcSite: SAN01 
  * GlobalId: 2GeNRqWib7AxRAMTf8zRbG (shared by both SAN01 Object)
  * CompositionType: COMPLEX
* IfcRailway: Railway0
  * CompositionType: COMPLEX
* IfcRailway: Railway1
  * CompositionType: ELEMENT
* IfcRailway: Railway2a
  * CompositionType: ELEMENT
* IfcRailway: Railway2b
  * CompositionType: ELEMENT
* IfcRailway: Railway3
  * CompositionType: ELEMENT

#### Road Project

* IfcProject: Road
  * HasName: Urban Railway
* IfcSite: SAN01 
  * GlobalId: 2GeNRqWib7AxRAMTf8zRbG (shared by both SAN01 Object)
  * CompositionType: COMPLEX
* IfcRoad: Road1
  * CompositionType: ELEMENT
* IfcRoad: Road2
  * CompositionType: ELEMENT
* IfcRoad: Road3
  * CompositionType: ELEMENT
* IfcRoad: Road4
  * CompositionType: ELEMENT
* IfcRoad: Road5
  * CompositionType: ELEMENT
* IfcRoad: Road6
  * CompositionType: ELEMENT
* IfcRoad: Road7
  * CompositionType: ELEMENT
* IfcRoad: Road8
  * CompositionType: ELEMENT
* IfcFacilityPart: Tunnel
  * CompositionType: ELEMENT

[Road Project - IFC file](Dataset/UT_RSS2_Road.ifc)


---
### Expected Results

The projet containing Rail spatial structure can be created using a given IfcSite object from exstig project to ensure future gloabl placement. The created infrastructure is then exported and reviewd to ensure similar IfcSite configuration.

**Reference File can be found** [HERE](./IFC%20reference%20files/UT_RSS_2_Reference_File.ifc)
