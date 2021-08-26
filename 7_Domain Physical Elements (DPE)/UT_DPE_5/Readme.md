# Unit Test: Signalling equipment for a level crossing

|UnitTest title	 |ID |	Author	|Data Owner	|Format	|SWV|
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|Signalling equipment for a level crossing|UT_DPE_5|Lars W|FTIA|DWG, IFC, XML|  |

## 1. **General**

This unit test intends to experiment the use of IFC for the representation of signalling equipment located at a level crossing. The equipment included is:

- A boom barrier
- A guardrail
- A signal assembly
  - audio signal
  - visual signal
  - sign
  - post
  - footing
- Axle counters and junction boxes
- Cabling
- Cabinets
- A technical building

A proposal for a spatial structure for the project is provided as well as track panel and ballast bed for context.

## 2. Spatial structure

The proposed spatial structure is shown here:

![](./DataSet/Toivola_area_borders.JPG)

![](./DataSet/Toivola_area_borders2.JPG)

The spatial structure can be simplified, but is available in the reference file.

## 3. Elements

The different elements have been provided in dwg-files as well as IFC 2x3 files (using IfcBuildingElementProxy elements).

The following mapping to IFC 4.3 is proposed (all these elements are available in the IFC reference file):

| Element                  | IFC representation                                           |
| ------------------------ | ------------------------------------------------------------ |
| Boom barrier             | IfcDoor/BOOM_BARRIER                                         |
| Signal assembly          | IfcElementAssembly/SIGNALASSEMBLY                            |
| Audio signal             | IfcSignal/AUDIO                                              |
| Visual signal            | IfcSignal/VISUAL                                             |
| Sign                     | IfcSign/PICTORAL                                             |
| Signal post              | IfcMember/POST                                               |
| Axle counter             | IfcSensor/WHEELSENSOR                                        |
| Junction box             | IfcJunctionBox/DATA                                          |
| Cables                   | IfcCableSegment                                              |
| Cabinet                  | IfcFurniture/TECHNICALCABINET                                |
| Snow plough protection   | IfcDiscreteAccessory/RAIL_MECHANICAL_EQUIPMENT               |
| Controllers/Computers    | IfcController/PROGRAMMABLE<br />IfcCommunicationsAppliance/COMPUTER<br />IfcSwitchingDevice/TOGGLESWITCH |
| Other optional equipment | IfcRailing/GUARDRAIL<br />IfcFooting/PAD_FOOTING<br />IfcStair/LADDER |

## 4. System structure 

An optional addition is to create a system structure. A proposed structure is available in the IFC reference file:

- IfcDistributionSystem/USERDEFINED/RoadProtection
  - IfcDistributionSystem/CONTROL (Boom barrier)
    - Signal assembly
    - Cables
    - Guardrail, Ladder
  - IfcDistributionSystem/Control ("Central intelligence")
    - Controllers/computers
  - IfcDistributionSystem/SIGNAL (axle counting)
    - Axle counters/junction boxes
    - Cabling connecting the axle counters/junction boxes to "Central intelligence"

## 5. Georeferencing

Refer to the picture below for georeferencing parameters. The coordinate reference system used is EPSG:3878, datum is ETRS89 and vertical datum is N2000.

![](./DataSet/Figure1-Situation.PNG)

## 6. Reference file

As stated above, there are IFC reference files available:

- [Without georeferencing](./IFC reference files/Draft/Signaling_LC_incl_Track_Cables.ifc)
- [With georeferencing](./IFC reference files/Draft/Signaling_LC_incl_Track_Cables_Georef.ifc)

Currently, the reference files use local placement for all elements. Desirable would be to have at least the axle counters/junction boxes and snow plough protection placed linearly along the alignment. The track alignment is not included in the IFC reference files either.

In addition to the elements listed above, the IFC reference files also includes a track panel (rails + sleepers) and ballast bed for context. These elements are classified correctly according to IFC 4.3, but also using local placement.

![](./DataSet/Overview.PNG)

## 7. **Attachment**

1. SIIRTO_ORIVESI-HAAPAMAKI_270-273_GK24_KAANNETTY.XML - Track alignment
2. TOI_Axle_counter_329161 [.dwg/.ifc] - Axle counters
3. TOI_Ballast_24100 [.dwg/.ifc] - Ballast
4. TOI_Boom_barrier_system_329100 [.dwg/.ifc] - Boom barrier 
5. TOI_Cabinet_329131 [.dwg/.ifc] - Cabinets
6. TOI_Cable_junction_box_329161 [.dwg/.ifc] - Junction boxes
7. TOI_Cables_32900 [.dwg/.ifc] - Cables
8. TOI_Rails_242100 [.dwg/.ifc] - Rails
9. TOI_Sleepers_242200 [.dwg/.ifc] - Sleepers
10. TOI_Snow_Plough_protection_329163 [.dwg/.ifc] - Snow plough protection
11. TOI_Technical_building_329132 [.dwg/.ifc] - Technical building
12. Toivola_area_borders.dwg - Project overview including proposed spatial structure breakdown
13. Toivola_area_borders.JPG - Project overview including proposed spatial structure breakdown - part 1 
14. Toivola_area_borders2.JPG Project overview including proposed spatial structure breakdown - part2
