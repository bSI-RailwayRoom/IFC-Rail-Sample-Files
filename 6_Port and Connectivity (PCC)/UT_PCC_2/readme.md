# Unit Test: BTS Cluster Wired Network



|       Unit Test title     | ID | Author | Data Owner | Format | Software Vendors |
|:-------------------------:|:--:|:------:| :---------:| :-----:| :---------------:|
| BTS Cluster Wired Network |  UT_PCC_2 | Florian Hulin | SNCF | text, images, |  |


## General
This Unit Test intends to experiment the use of IFC to represent a wired transmission network used in the GSM-R base station subsystem.


For the scope of this UT, illustration of the transmission segment connecting the base transceiver stations installed along the railway line N° 944000,  was taken as an example.

The dataset is provided by SNCF.


## Dataset Description

The datasets aim to provide some technical constraints and requirements that are related to the wired transmission network and which need to be faithfully transcribed in an IFC model. 

The figure below represents the distribution network that connects the 4 BTS installed along the railway line N° 944000, between CANNES-LA-BOCCA and GRASSE railway stations, as well as the SDH transport network connecting the 4 BTS cluster (N° PAK_Marseille_BSC1_44) to the BSC site in Marseille: 
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/UT_PCC_2/6_Port%20and%20Connectivity%20(PCC)/UT_PCC_2/Dataset/BTS%20Cluster%20Cannes-Grasse.png)

As indicated in the figure above, the 4 BTS (FERME DE RANGUIN BTS, MOUGINS BTS, GRASSE ST-MARC BTS and GRASSE MADELAINE BTS) are connected via an optical fiber transmission medium to form the transmission segment of the distribution network (desserte) that starts from the PART of Cannes 1 to the PART of Grasse. This distribution network segments represents the 4 BTS cluster referenced under the code PAK_Marseille_BSC1_44. It is important to mention that a cluster consists of a maximum of 6 BTS. The distribution network segment can either use copper cables as transmission medium.

The transport network starts from the PARTs to the base station controller (BSC) site. The PARTs mark the border between the distribution network (Desserte) and the transport network (Transport).
As represented in the figure 1 above, in the PART of Cannes1, the optical modem from the distribution network is connected to the Add-Drop Multiplexer STM-1 from the SDH transport network. 
The Add-Drop Multiplexer STM-1  (ADM1) is an optical multiplexer that combines, or multiplexes, several lower-bandwidth streams of data into a single beam of light.


The [schematic representation](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/UT_PCC_2/6_Port%20and%20Connectivity%20(PCC)/UT_PCC_2/Dataset/PCC2%20Schema.png)  of the needs : 
![alt text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/UT_PCC_2/6_Port%20and%20Connectivity%20(PCC)/UT_PCC_2/Dataset/PCC2%20Schema.png)




## Expected Results

Considering the aim of this UT, the expected results are:
1. Screenshot of the system geometric representation, as represented in the native application.
2. The resulting IFC file containing the system topology information as requested.

