# Unit Test: Alignment with Plane Sine Transition Curve Vertical Transition Curve and Cant

| Unit Test title        | ID       | Author        | Data Owner      | Format                              | Software Vendors | 
|:----------------------:|:--------:|:-------------:|:---------------:|:-----------------------------------:|:----------------:|
|  Alignment with Plane Sine Transition Curve Vertical Transition Curve and Cant | UT_AWC_6 | Guoliang Kong | CRBIM CRDC | DWG, Excel, Ifc, pf | RDS, Catia   |

 

## 1.General
This document describes in detail the data organization of the plane, profile and cant of a double line railway line through a railway line example, in particular provides some special elements such as sine plane transition curve and clothid vertical transition curve,so as to facilitate the software service manufacturer to test and verify.

## 2.Railway line plane(with sine transition curve)
**(1)Line plane drawing**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/1_Example_of_double_line_railway_plan_drawing.jpg)

**(2)Line plane original data description**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/2_Description_of_line_plane_original_data.jpg)

In RDS software, the type 7 represents  sine type transition curve. 
The original data is shown in the attachment "pf" file.

**(3)Description of line plane each element data**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/3_Description_of_line_plane_each_element_data.jpg)

The data is shown in the attached excel table.

## 3.Railway line profile(with clothoid profile transition curve)
**(1)Line profile drawing**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/4_Example_of_line_profile_drawing.jpg)

Vertical transition curve of profile: In the design of wheel rail railway of all grades in China, vertical transition curve is not set in profile; in the design of high-speed maglev, due to the high running speed of high-speed maglev train, the line type has a great impact on the train dynamic target. In order to ensure the stationarity and comfort of the train at the change-grade point, a vertical transition curve should be set between the straight slope section and the vertical circular curve, so as to achieve the continuity of curve curvature and reduce the impact caused by sudden acceleration change. The clothoid transition curve is adopted as the vertical transition curve type.

Compared with that without vertical transition curve, the changes are as follows:

**1) Change of slope line**

The drawing of setting vertical transition curve slope:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/5_Slopegrade_vertical_transition_curve.jpg)

The drawing of not setting vertical transition curve slope:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/6_drawing_of_not_setting_vertical_transition_curve_slope.jpg)

**2) Vertical curve bar drawing changes**

The drawing of setting vertical transition curve bar:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/7_drawing_of_setting_vertical_transition_curve_bar.jpg)

The drawing of not setting vertical transition curve bar:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/8_drawing_of_not_setting_vertical_transition_curve_bar.jpg)

**(2)Description of original data of line profile**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/9_Description_of_original_data_of_line_profile.jpg)

In RDS software, type 2 represents cycloid transition curve. The specific data are shown in the attachment "pf" file.

**(3)Description of line profile each element data**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/10_Description_of_line_profile_each_element_data.jpg)

The data is shown in the attached excel table.

## 4.Line cant
**(1)Line cant drawing**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/11_Line_cant_drawing.jpg)

**(2)Description of the initial data of line cant**

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/2_Description_of_line_plane_original_data.jpg)

In RDS software, cant data is set on each curve, as shown in the figure above. The original data is shown in the attachment "pf" file.

**(3)Description of line cant each element data**

In RDS, according to the definition of straight line cant segment and cant transition section by IFCAlignment, the data of each element is output respectively, as shown in the table below.

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/12_Description_of_line_cant_each_element_data.jpg)

Description of cant data: according to the IFCAlignment definition, the cant value is the elevation of the left rail surface minus the elevation of the right rail surface. In the design of China's wheel rail railway, the cant on the curve is generally set as the elevation of the inner shoulder remains unchanged and the outer side is raised. Therefore, there is a positive and negative cant difference on the curve, and the absolute cant value is not reduced by half (different from the example provided by "IFC rail alignment test data"). In this example, the unit of measurement for cant is millimeter.

There is a question here:

Is TransitionCurveType the transition curve type? Or the transition type of cant?

In my opinion,it refers to the transition type of cant. In wheel rail or maglev railway, cant transition is allways straight line. If the type of straight line is filled in here, IfcTransitionCurvetype does not contain straight line. Does it need to be modified?

**(4)Line cant applications**

When BIM software has not yet provided the function of cant design, the method of setting out section with cant and sweeping the front and rear sections along the guide line to form a body is used to realize the road base modeling involving cant.

Single line rail skeleton:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/13_Single_line_rail_skeleton.jpg)

Double line subgrade with cant ballasted track:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/14_Double_line_subgrade_with_cant_ballasted_track.jpg)

Double-line bridge with cant ballasted track:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/15_Double-line_bridge_with_cant_ballasted_track.jpg)

Double-line tunnel with cant ballastless track:

![image text](https://github.com/IFCRail/IFC-Rail-Unit-Test/blob/master/1_Alignment%20with%20Cant%20(AWC)/UT_AWC_6/Dataset/Images/16_Double-line_tunnel_with_cant_ballastless_track.jpg)


## 4.Generate IFC File
The version of IFC schema adopted is "IFC4x3_RC1".

**(1)The entities used in the plane**

Include:IfcAlignment; IfcAlignmentCurve; IfcAlignment2DHorizontal; IfcAlignment2DHorizontalSegment; IfcLineSegment2D; IfcCircularArcSegment2D; IfcTransitionCurveSegment2D.

**(2)The entities used in the profile**

Include:IfcAlignment2DVertical; IfcAlignment2DVerSegLine; IfcAlignment2DVerSegCircularArc.

**(3)The entities used in the cant**

Include:IfcLinearAxisWithInclination; IfcAlignment2Dcant; IfcAlignment2DcantSegment; IfcAlignment2DcantSegLine; IfcAlignment2DCantSegTransition.


## 5.Attachment
1.Double Line Railway Raw Data_(Sine Transition Curve+Vertical Transition Curve+Cant).pf

2.Line Plane Vertical and Cant Drawing.dwg

3.Each Unit Data of Plane Vertical and Cant.xls

4.Double Line Railway Alignment(Sine Transition Curve+Vertical Transition Curve+Cant).ifc

5.IFC4x3_RC1.exp