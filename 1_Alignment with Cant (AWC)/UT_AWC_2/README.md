# Unit Test: Alignment with Cant 2

|              Unit Test title                  | ID| Author | Data Owner | Input Format | Software Vendors | 
|:-----------------------------------------:|:------:|:------:| :------:| :------:| :------:|
|  Alignment with Cant 2 |   UT_AWC_2 | Florian Hulin | SNCF | LandXML |  |

 

## General
This Unit Test Scenario contains two alignments that are defined by three layouts : Horizontal, Vertical and Cant.

The horizontal alignment consists of straight line segments, circular segments and transition curve (Clothoid), vertical alignment consists of straight line and circular segments, and cant alignment consists of straight line segments. These 3 layouts are condensed in one LandXML file.

This dataset contains 2 curved tracks alignement linked by a switch. 
The particularity of this dataset is that the deviated track will have an off-Camber (it keeps the same cant as the first track even if the direction is opposite).

The input dataset is provided by SNCF Réseau in LandXML format. The software vendors joining the project will be expected to produce an IFC file.


## Prerequisites
This scenario builds upon following scenarios:
- None

## Data Description
This Dataset is in LandXML 2.0 format, produced by OpenRail Designer, which is a softaware developed by Bentley Systems, Inc.

To get more information about alignment in LandXML data Schema, you can visit the website : 
http://www.landxml.org/schema/LandXML-1.2/documentation/LandXML-1.2Doc_Alignment.html

The file describes 2 alignements : 
- V1 which is the main track alignment
- V2 which is the derivated track alignment

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_2/Dataset/Alignment%20picture.PNG)

### Horizontal Alignment
Inside the LandXML file, horizontal alignment part is located between the tags  <'CoordGeom'>.

Geometry type : 
| Alignment Geometry | XML Tag |
|--|--|
|straight line|Line |
|Arc|Curve crvType="arc"|
|transition curve (in this case : clothoid) |Spiral spiType="clothoid"|



#### Data snippet
```
<Spiral spiType="clothoid" length="79.999999999999986" rot="cw" radiusStart="INF" radiusEnd="600">
	<Start>422.74416446215679 541.9315958704226 0</Start>
	<PI>422.82998225016405 595.27728168659087 0</PI>
	<End>421.09559279948905 621.8988031773016 0</End>
	<Feature>
		<Property label="style" value="Alignment\0_SNCF\Voie_AXE_Coloré" />
	</Feature>
</Spiral>
```



### Vertical Alignment
Inside the LandXML file, vertical alignment part is located between the tags  <'Profile'>.

The vertical alignments of this data set only consists of straight line which are defined by their intersections. 
Theses intersections points are called 'Points  of vertical intersection' (PVI). Theses PVI points are  characterized by a kilometer Point, and an Altitude.

#### Data snippet
```
<Profile>
	<ProfAlign name="V1_PL">
		<PVI>2700 19.44708598060754</PVI>
	</ProfAlign>
</Profile>
```


### Cant Alignment

Cant Alignment view for track 1 :
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_2/Dataset/View%20Cant%20V1.PNG)

Cant Alignment view for track 2 :
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_2/Dataset/View%20Cant%20V2.PNG)

Inside the LandXML file, Cant alignment part is located between the tags  <'Cant'>.

The cant alignment is defined by multiple Cant stations. 

Below are some importants variables for cant definition : 

| XML Tag |Cant Alignment definition |
|--|--|
|CantStation station|Starting Kilometer Point (Km value) |
|AppliedCant|Cant applied to the section (in mm)|
|Speed|Speed applied to the section (in Km per hour)|
|Curvature|Curvature of the section (Clockwise or CounterClockwise)|
|Transition curve (in this case : clothoid) |Spiral spiType="clothoid"|

#### Data snippet
```
<Cant name="Cant_V1" equilibriumConstant="11.810279667422526" gauge="1.5" rotationPoint="insideRail">
	<CantStation station="0" equilibriumCant="0" appliedCant="0" cantDeficiency="0" rateOfChangeOfAppliedCantOverTime="0" rateOfChangeOfAppliedCantOverLength="0" rateOfChangeOfCantDeficiencyOverTime="0" cantGradient="0" speed="90" curvature="ccw" adverse="false" />
	<CantStation station="83.076281198" equilibriumCant="18.860" appliedCant="70.000" cantDeficiency="-51.140" rateOfChangeOfAppliedCantOverTime="0.000" rateOfChangeOfAppliedCantOverLength="0.000" rateOfChangeOfCantDeficiencyOverTime="0.011" cantGradient="0.000" speed="100.0" curvature="ccw" adverse="false"/>
</Cant>			
```

## Execution Log

