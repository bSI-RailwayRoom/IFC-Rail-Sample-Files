# Unit Test: Multiduct System topology



|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
| Multiduct System topology |  UT_PCC_1 | Sylvain Marie | M4R | text, images, powerpoint |  |


## General
This Unit Test intends to experiment the use of IFC to represent the topology of the multiduct system in order to complete the piping system description.

For the scope of this UT, part of an underground electrical system for an urban railway was taken as an example.

The dataset is provided by MINnD4Rail, see [Dataset Description](#dataset-description) section for details.


## Dataset Description

The [dataset](./Dataset) is currently made of:
1. A picture representing the multiduct topology: [Multiduct system](./Dataset/UT_PCC_1_multiduct%20system.png);
3. A picture show the IFC entities involved in the system topology: [Entities](./Dataset/UT_PCC_1_entities.png).
3. An IFC4 file storing the piping system with no connectivity involved.

## IFC Reference file

One [IFC reference file](./IFC%20reference%20files/UT_PCC_1.ifc) is provided including connected duct ports between duct segments.


## Expected Results

Considering the aim of this UT, the expected results are:
1. Screen-shot of the project breakdown as represented in the native application, showing the System topology.
2. Screenshot of the system geometric representation, as represented in the native application.
2. The resulting IFC file containing the system topology information as requested.
