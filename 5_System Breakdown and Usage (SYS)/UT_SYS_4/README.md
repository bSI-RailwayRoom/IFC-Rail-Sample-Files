# Unit Test: BTS functionnal breakdown

|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
|  BTS functionnal breakdown |   UT_SYS_4 | Florian HULIN| SNCF | text, images, excel |  |

## General
This Unit Test intends to experiment the use of IFC to represent the functionnal breakdown of the GSM-R access network.

This mobile communication system is named GSM-R (Global System for Mobile communications - Railways) and together with the ETCS (European Train Control System), they constitute the 2 main technologies on which the ERTMS relies.  

The functional breakdown that will be described in this documentation only corresponds to the GSM-R system. The functional model of the whole GSM-R system will indeed be presented, but since only the Base Station Subsystem of GSM-R (also known as the access network) is involved in the storyline, it will therefore be the only subsystem to detail in this document. 

The functional model presented in this document allows understanding the functional hierarchies of the GSM-R system and especially its Base Station Subsystem (BSS). These functional hierarchies describe the decomposition of the required functional goal into sub-functions that can be achieved by agents, which are viewed as the main actor to achieve the function and do not necessarily correspond to the physical components. 

The dataset is provided by SNCF.


## Dataset Description

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/UT_SYS_4/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_4/Dataset/FunctionnalBreakDownSNCF.png)

The goal of this functional modelling is to verify if we can generate an IFC file that could include all the information provided by the current functional model of GSM-R system

The main function of a GSM-R Access Network (Base Station Subsystem) is to aggregates the global functions of wireless signal receiving/transmitting and radio resource management, which are respectively realized by the Base Transceiver Station (BTS) and the Base Station Controller (BSC);  

### Functional grouping within the BTS
As mentioned before, the ERTMS storyline scope is limited to the base station subsystem of GSM-R. The GSMR subsystem can be considered as an aggregation of other functional groups, which are: the base transceiver station functional group and the weak-field coverage functional group.

#### 1 - Base transceiver station functional group 

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/UT_SYS_4/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_4/Dataset/BTS%20System.png)

This group includes the telecom objects that transmit and receive information on the radio channel by providing a physical interface between the train and the Base Station Controller. 

*IFC Mapping :  IfcDistributionSystem*

The grouping of objects within the Base transceiver station functional group is presented in the list below:

**Remote Radio Unit** (also called a remote radio head RRH), is usually sitting on top of cell tower. It mainly performs the following functions:
•	Convert optical signal to electrical signal and vice versa;
•	In transmitter section of RRU, it converts digital signal to radio frequency (RF) signal and amplifies that signal to the desire power level and antenna connected to it, radiates the RF signal in air;
•	In receiver section of RRU, it receives the desired band of signal from antenna and amplify it;
•	And convert RF signal back to digital signal in the receiver chain;
*IFC Mapping : IfcMobileTelecommunicationsAppliancePredefinedTypeREMOTERADIOUNIT*

**Base Band Unit (BBU)**, is usually placed inside a cabinet next to the cell tower. It performs frequency hopping and the digital signal processing. One BBU is connected to multiple RRUs depending upon the capability of base-band unit

*IFC Mapping : IfcMobileTelecommunicationsAppliancePredefinedTypeBASEBANDEUNIT*

**Antennas**, may also be considered as components of BTS. An antenna is a device that effectively radiates or receives electromagnetic waves. In open sites, it is placed on a radio mast, tower, or other raised structure. 

*IFC Mapping : IfcCommunicationsAppliancePredefinedTypeANTENNA*

**Supporting System**, represent the raised structure that support antennas and one or more RRU in open sites. 

*IFC Mapping :  IfcElementAssemblyPredefinedTypeMAST*

**Cabinet**

*IFC Mapping :  IfcElementAssemblyPredefinedTypeSHELTER*

#### 2 - Weak-coverage functional group 

![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/UT_SYS_4/5_System%20Breakdown%20and%20Usage%20(SYS)/UT_SYS_4/Dataset/weakcoveragesystem.png)

This group includes the telecom objects that expand the radio coverage of the BTS in areas where it is difficult to install one such as inside tunnels.  

The grouping of objects within the weak-coverage functional group is presented in the list below:

**Master Unit**, is a component of a repeater for coupling base station signals. It is used to expand the radio coverage, with the assistance of remote units, in the areas where we cannot put a BTS like in tunnels for example.

*IFC Mapping : IfcMobileTelecommunicationsAppliancePredefinedTypeMASTERUNIT*

**Remote Unit**, is used to amplify a base station signal and insure its wireless transmission in the areas where it is difficult to put a BTS. It receives a coded signal from the master unit via a wired transport link (usually optical fiber cables) and transmits it to the antennas for being wirelessly transmitted

*IFC Mapping :  IfcMobileTelecommunicationsAppliancePredefinedTypeREMOTEUNIT*

**Antennas**, may also be considered as components of BTS. An antenna is a device that effectively radiates or receives electromagnetic waves. In open sites, it is placed on a radio mast, tower, or other raised structure. 

*IFC Mapping : IfcCommunicationsAppliancePredefinedTypeANTENNA*

**Supporting System**, represent the raised structure that support antennas and one or more RRU in open sites.

*IFC Mapping :  IfcElementAssemblyPredefinedTypeMAST*

## Expected Results

Considering the aim of this UT, the expected results are:
1. The resulting IFC file containing the system breakdown information as requested.

