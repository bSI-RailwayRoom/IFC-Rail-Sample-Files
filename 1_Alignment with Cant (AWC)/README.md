# Railway parametric alignment with cant

|              Topic title                  |Topic ID |
|:-----------------------------------------:|:-------:|
|  Railway parametric alignment with cant   |   AWC   |


## Associated Unit Tests


| N |   Unit Test title   |Unit Test ID|  Description                 |
|:-:|:-------------------:|:----------:|:----------------------------:|
| 1 | Cant Alignment 1    |  UT_AWC_1  |  AWC_UT1_SBB_scenario        |
| 2 | Cant Alignment 2    |  UT_AWC_2  |  AWC_UT2_SNCF_scenario       |
| 3 | Cant Alignment 3    |  UT_AWC_3  |  AWC_UT3_NORDICS_scenario    |
| 4 | Cant Alignment 4    |  UT_AWC_4  |  AWC_UT4_RFI_scenario        |
| 5 | Cant Alignment 5    |  UT_AWC_5  |  AWC_UT4_RailComplete_scenario        |
| 6 | Cant Alignment 6    |  UT_AWC_6  |  AWC_UT4_CRBIM_scenario        |
| 7 | Cant Alignment 7    |  UT_AWC_7  |  AWC_UT7_RFI_scenario with cubic parabola   

## Intent
The Unit Tests associated to this Topic are meant to prove the possibility to parametrically represent and exchange the information of railway alignment using IFC. Such alignmenet includes the cant parameters.

## IFC scope
- Required IFC Concept Templates
  - **Existing**:
    - [Spatial Containment](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/spatial-containment.htm) (IfcAlignment is contained in IfcSite)
    - [Spatial Composition](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/spatial-composition.htm)`(IfcProject is decomposed by IfcSite)
    - [Project Representation Context](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/schema/templates/project-representation-context.htm)
    - [Project Units](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/project-units.htm)
  - **New**:
    - [Alignment with Cant](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/AWC_ConceptTemplate.png)
- Focused IFC Entities
  - **Existing**:
    - [IfcAlignment](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment.htm)
    - [IfcAlignmentCurve](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignmentcurve.htm)
    - [IfcAlignment2DHorizontal](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dhorizontal.htm)
	- [IfcAlignment2DVertical](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dvertical.htm)
	- [IfcAlignment2DVertical](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dvertical.htm)
	- [IfcAlignment2DHorizontal](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dhorizontalsegment.htm)
	- [IfcLineSegment2D](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifclinesegment2d.htm)
	- [IfcCircularArcSegment2D](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifccirculararcsegment2d.htm)
	- [IfcTransitionCurveSegment2D](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifctransitioncurvesegment2d.htm)
	- [IfcAlignment2DVerSegLine](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dversegline.htm)
	- [IfcAlignment2DVerSegCircularArc](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dversegcirculararc.htm)
	
  - **New**:
    - [IfcLinearAxisWithInclination](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifclinearaxiswithinclination.htm)
    - [IfcAlignment2DCant](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dcant.htm)
	- [IfcAlignment2DCantSegLine](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dcantsegline.htm)
	- [IfcAlignment2DCantSegTransition](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dcantsegtransition.htm)
	- [IfcAlignment2DVerSegTransition](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcalignment2dversegtransition.htm)

## REF. to [Conceptual Model Report](https://app.box.com/s/m0kl6qnsl269kgz2sa8ciu5mio96m04a)
Section 6.1

## REF. to [Mapping Diagram Report](https://app.box.com/s/m0kl6qnsl269kgz2sa8ciu5mio96m04a)
Section XXX, Paragraph YYY
