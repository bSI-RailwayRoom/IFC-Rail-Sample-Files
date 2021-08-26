# Port Connectivity

|              Topic title                  |Topic ID|
|:-----------------------------------------:|:------:|
|  Port and Connectivity              |   PCC  |


## Associated Unit Tests
| N |   Unit Test title   |Unit Test ID|        Full Unit Test name     |
|:-:|:-------------------:|:----------:| :-----------------------------:|
| 1 |    [Port and Connectivity 1](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/UT_PCC_1/6_Port%20and%20Connectivity%20(PCC)/UT_PCC_1)    |  UT_PCC_1  |  PCC_UT1_M4R  |
| 2 | Port Connectivity 2 |   UT_PCC_2    | PCC_UT2_SNCF |
| 3 |  |   UT_PCC_3    |          |


## Intent
The Unit Tests associated to this Topic are meant to prove the possibility to use IfcPort and relevant IfcRelationship subtypes to realize connections among elements as networks.

- Connections between two Distribution Element nesting Distribution Port for power supply, communication or any other flows.
- Systeme breakdown of elements linked by ports
- Communication between two functional groups (Relation between two systems)



## IFC scope

- Required IFC concept templates
  - **Existing**:
  - [Port Connectivity](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/templates/port-connectivity.htm)
  - [Port Nesting](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/templates/port-nesting.htm)
  - [Control Flow](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/templates/control-flow.htm)

- Focused IFC entities
  - **Existing**:
  - [IfcRelConnectsPorts](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcproductextension/lexical/ifcrelconnectsports.htm)
  - [IfcRelNests](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifckernel/lexical/ifcrelnests.htm)
  - [IfcDistributionPort](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcsharedbldgserviceelements/lexical/ifcdistributionport.htm)
  - [IfcElement](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcproductextension/lexical/ifcelement.htm)
  - [IfcDistributionElement and its subtypes](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcproductextension/lexical/ifcdistributionelement.htm)
  - [IfcDistributionSystem](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcsharedbldgserviceelements/lexical/ifcdistributionsystem.htm)
  - [IfcDistributionCircuit](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcsharedbldgserviceelements/lexical/ifcdistributioncircuit.htm)

  - [IfcRelFlowControlElements](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcsharedbldgserviceelements/lexical/ifcrelflowcontrolelements.htm)
  - [IfcFlowSegment and its subtypes](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcsharedbldgserviceelements/lexical/ifcflowsegment.htm)
  - [IfcGroup and its subtypes](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifckernel/lexical/ifcgroup.htm)
  - [IfcRelAssignToGroup](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifckernel/lexical/ifcrelassignstogroup.htm)


  - **New**:
  - [IfcBuiltElement](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC2/HTML/schema/ifcproductextension/lexical/ifcbuiltelement.htm)

