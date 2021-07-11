# Linear placement

|              Topic title                  |Topic ID|
|:-----------------------------------------:|:------:|
|  Linear placement                     |   LP   |


## Associated Unit Tests


| N |   Unit Test title   |Unit Test ID|        Full Unit Test name     |
|:-:|:-------------------:|:----------:| :-----------------------------:|
| 1 |    Linear placement 1    |  UT_LP_1  |  LP_UT1_RFI_scenario  |
|  2   | Linear placement 1 |   UT_LP_2    | LP_UT2_RailComplete_scenario |
|  3   | Linear placement 3 |   UT_LP_3    |     LP_UT3_SBB_scenario      |
|  4   | Linear placement 4 |   UT_LP_4    |   LP_UT4_Nordics_scenario    |
| 5 | Linear placement 5 | UT_LP_5 | LP_UT5_SNCF_scenario |
| 6 | LInear placement 6 | UT_LP_6 | LP_UT6_SNCF_scenario |
| 7 | Linear placement 7 | UT_LP_7 | LP_UT7_???_scenario |
| 8 | Linear placement 8 | UT_LP_8 | LP_UT8_CRBIM_scenario |
| 9 | Linear placement 9 | UT_LP_9 | LP_UT8_Nordics_scenario |




## Intent
The Unit Tests associated to this Topic are meant to prove the possibility to represent and exchange information about linear placement of products. The unit tests shall cover the following alternative representations:

- Placement at point locations
  - Linear placement without considering cant parameters
  - Linear placement that considers cant parameters
  - Both cases above shall be tested with and without lateral and vertical offsets
  - Both cases above shall be tested with and without orientation specification
- Placement at span locations (from/to)
  - With and without lateral and vertical offsets and offsets?
  - *This case would need some more discussion and clarification since it may not always be clear what it means for objects with explicit geometry*
    - *I think that the main intention was to place things like:*
      - *Longitudinal facility parts without explicit geometry*
      - *Annotations capturing non geometric data such as design speed that occurs along subsections of an alignment*
- Broken chainage
  - Testing should include the definition of broken chainage as a layer of information, using IfcReferent, for alignments and verification that this information can be used to:
    - Transform external chainage values to the internal linear placement representation in IFC (IfcDistanceExpression.DistanceAlong) arriving at the desired location
    - Transform internal IFC representation back to external chainage values, e.g. for presentation for users
  - [Broken chainage in InfraModel 4 (LandXML 1.2) is described in chapter 5.4](https://buildingsmart.fi/infra/inframodel/index.html)
  - [Swedish use of LandXML Station equations](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/SWE%20StaEquation-IFC.docx)

## IFC scope
- Dependant on topics
  - [Alignment with cant](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/1_Alignment%20with%20Cant%20(AWC))
- Required IFC concept templates
  - **Existing**:
    - [Product Linear Placement](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/product-linear-placement.htm)
  - **New**:
    - [Product Linear Placement with Inclination](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/Concept%20template%20-%20Product%20linear%20placement%20with%20inclination.png)
    - [Product Linear Span Placement](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/Concept%20template%20-%20Product%20linear%20span%20placement.png)
    - [*"Alignment with Broken chainage"*](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/Concept%20template%20-%20Broken%20chainage.png)
- Focused IFC entities
  - **Existing**:
    - [IfcProduct](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcproduct.htm) (any convenient instantiable subtype that shall be placed along an alignment)
    - [IfcLinearPlacement](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifclinearplacement.htm)
    - [IfcObjectPlacement](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcobjectplacement.htm)
    - [IfcDistanceExpression](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcdistanceexpression.htm)
    - [IfcOrientationExpression](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcorientationexpression.htm)
    - [IfcDirection](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcdirection.htm)
    - [IfcReferent](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcreferent.htm)
  - **New**:
    - [IfcLinearPlacementWithInclination](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifclinearplacementwithinclination.htm)
    - [IfcLinearSpanPlacement](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifclinearspanplacement.htm)
    - [IfcAxisLateralInclination](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcaxislateralinclination.htm)

## REF. to Conceptual Model Report
Section 6.2-6.3

## REF. to Mapping Diagram Report
Section XXX, Paragraph YYY

## Concept templates
- TBD
