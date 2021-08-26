# System: Breakdown and Usage

|              Topic title                  |Topic ID|
|:-----------------------------------------:|:------:|
|  System: breakdown and usage                  |   SYS  |


## Associated Unit Tests

| N |   Unit Test title   |Unit Test ID|        Full Unit Test name     |
|:-:|:-------------------:|:----------:| :-----------------------------:|
| 1 |   System breakdown and Group Assignment 	|  UT_SYS_1    | SYS_UT1_RFI|
|  2   | Group reference to spatial structure |  UT_SYS_2    |SYS_UT2_RFI |
|  3   | Property Sets for Groups (and Group types)|  UT_SYS_3    |SYS_UT3_RFI |


## Intent
The Unit Tests associated to this Topic are meant to prove the possibility to aggregate objects under non geometrical, functional grouping aspects. In particular,as opposed to Spatial Structure, which is typically a hierarchy of elements, System tructure tends to be non-hierarchical. The unit tests shall cover the following usages:

- Aggregate and collect elements in a Group
  - Use of IfcGroup, and its subtypes (IfcSystem, IfcAsset) to group elements
  - Based on usage of IfcRelAssignsToGroup

- Collect a Group of elements in another Group
	- Use IfcGroup, and its subtypes (IfcSystem, IfcAsset) to create groups of groups
	- Based on usage of IfcRelAssignsToGroup

- Reference of a Group to the Spatial structure, e.g., to connect a system to the relevant spatial element that it serves
	- Use of IfcRelReferencedInSpatialStructure to refer a Group (and subtypes) to a Spatial Structure Element

- Define types of Groups
	- create a type of group or system
	- based on usage of IfcRelDefinesByType

-  Associate Psets to groups (and group types)
	- based on usage of IfcRelDefinesByProperty to associate IfcPropertySet to IfcGroup

## Requirements collected
1.	An element (subtype of IfcElement) can be part of multiple groups
    -  The relationship to be used is IfcRelAssignsToGroup
2.	A group (IfcGroup or subtypes) can be part of multiple groups (see restrictions, point 7)
    - The relationship to be used is IfcRelAssignsToGroup
3.	It is possible to have a group that does not belong to another group
4.	It is possible to have a group that does not belong to a spatial structure element
    - link (logical, functional, topological, etc.) between a group and an element of the spatial structure is possible, but NOT mandatory
    - If this link is required, the relationship to be used is IfcRelReferencedInSpatialStructure
    - The visual rendering of this relationship in a tool's UI is out of scope
5.	It is required to have a group that belongs to the IfcProject
    - 	The relationship to be used is IfcRelDeclares
6.	The user should be able to specify the functional breakdown
7.	The placement for spatial structure element is not required
8.	Restrictions regrading relationships among groups:
    - Circular reference (e.g., cyclic relationships) is not allowed
      -	neither direct (if A groups B, B cannot group A)
      - nor indirect (if A groups B and B groups C, C cannot group A)
    - Level jump is not needed (if A groups B and B groups C, A cannot group C)
    - Same-level grouping is not needed (if A groups B and C, B cannot group C and vice versa)



## IFC scope

- Required IFC concept templates
  - **Existing**:
    - [Group Assignment](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/group-assignment.htm)
    - [PropertySets for Objects](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/property-sets-for-objects.htm)
    - [Object Typing](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/object-typing.htm)

- Focused IFC entities
  - **Existing**:
    - [IfcGroup](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcgroup.htm) and its subtypes
    - [IfcTypeObject](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifctypeobject.htm)
    - [IfcPropertySet](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcpropertyset.htm)
    - [IfcRelAssignToGroup](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcrelassignstogroup.htm)
    - [IfcRelReferencedInSpatialStructure](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcrelreferencedinspatialstructure.htm)
    - [IfcRelDefinesByType](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcreldefinesbytype.htm)
    - [IfcRelDefinesByProperty](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/link/ifcreldefinesbyproperties.htm)

  - **New**:
    - [IfcBuiltSystem](https://standards.buildingsmart.org/IFC/DEV/IFC4_3/RC1/HTML/schema/ifcsharedinfrastructureelements/lexical/ifcbuiltsystem.htm)


