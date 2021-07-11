# Unit Test: Broken chainage

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
| Broken chainage | UT_LP_4 | Lars Wikström | Trafikverket | LandXML |  |


## General
This Unit Test intends to experiment the use of IFC for representing broken chainage. 

The dataset is provided by Trafikverket, see [Dataset Description](https://github.com/IFCRail/IFC-Rail-Unit-Test/tree/master/2_Linear placement (LP)/UT_LP_1#data-description) section for details.

The specification for how to use LandXML is described in Requirements of Track alignments - English draft.pdf  


## Prerequisites
The dataset itself contains the alignment necessary to perform this unit test.

## Data Description

The dataset is currently made up of two alignments (each defined by a horizontal and vertical component. The figure below illustrates these alignments as shown in the TUM Open Infra Platform.

![](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_4/Figure%201.png)

Figure 1 - Alignment oID=2 (green)

 ![](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_4/Figure%202.png)

Figure 2 - Alignment oID=1 (green)

 

The alignments are composed of:

- Horizontal alignment
  - Straight line (Line-element)
  - Circular arc (Curve-element)
  - Clothoid (Spiral-element)
- Vertical alignment
  - Using PVI- and CircCurve-elements

To each alignment there is also a description of chainage using StaEquation-elements.

Chainage for Alignment (oID=1):

```
<StaEquation staAhead="205.4145419" staBack="27205.4145419" staInternal="27205.4145419">
	<Feature code="StaEquation">
		<Property label="bckEqn" value="" />
		<Property label="ahdEqn" value="KM27+" />
    </Feature>
</StaEquation>
<StaEquation staAhead="0.0000000" staBack="1000.6596581" staInternal="28000.6596581">
	<Feature code="StaEquation">
		<Property label="bckEqn" value="KM27+" />
		<Property label="ahdEqn" value="KM28+" />
	</Feature>
</StaEquation>
```

 

Chainage for Alignment (oID=2):

   

```
<StaEquation staAhead="980.7997460" staBack="25980.7997460" staInternal="25980.7997460">
	<Feature code="StaEquation">
		<Property label="bckEqn" value="" />
		<Property label="ahdEqn" value="KM25+" />
    </Feature>
</StaEquation>
<StaEquation staAhead="0.0000000" staBack="1001.8000030" staInternal="26001.8000030">
	<Feature code="StaEquation">
		<Property label="bckEqn" value="KM25+" />
		<Property label="ahdEqn" value="KM26+" />
	</Feature>
</StaEquation>
<StaEquation staAhead="0.0000000" staBack="993.1271925" staInternal="26994.9271955">
	<Feature code="StaEquation">
		<Property label="bckEqn" value="KM26+" />
		<Property label="ahdEqn" value="KM27+" />
	</Feature>
</StaEquation>
<StaEquation staAhead="0.0000000" staBack="1000.8974299" staInternal="27995.8246254">
	<Feature code="StaEquation">
		<Property label="bckEqn" value="KM27+" />
		<Property label="ahdEqn" value="KM28+" />
	</Feature>
</StaEquation>
<StaEquation staAhead="0.0000000" staBack="1001.1529426" staInternal="28996.9775680">
	<Feature code="StaEquation">
		<Property label="bckEqn" value="KM28+" />
		<Property label="ahdEqn" value="KM29+" />
	</Feature>
</StaEquation>
```

 

The figure below shows the situation at and around KM28.

 ![](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_4/Figure%203.png)

Figure 3 - Map view at and around KM28

The figure below provides a schematic illustration of the chainage:

 ![](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/2_Linear%20placement%20(LP)/UT_LP_4/Figure%204.png)

Figure 4 - Chainage (schematic)

Besides what was described above, the LandXML file also contains:

- Cant (<Cant> - out of scope for this unit test)
- Switches (using <CgPoints> - also out of scope for this unit test)



