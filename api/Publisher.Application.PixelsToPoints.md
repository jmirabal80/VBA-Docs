---
title: Application.PixelsToPoints method (Publisher)
keywords: vbapb10.chm131153
f1_keywords:
- vbapb10.chm131153
ms.prod: publisher
api_name:
- Publisher.Application.PixelsToPoints
ms.assetid: 5d7e453f-e962-e557-48e4-44766d0c64d9
ms.date: 06/05/2019
ms.localizationpriority: medium
---


# Application.PixelsToPoints method (Publisher)

Converts a measurement from pixels to [points](../language/glossary/vbe-glossary.md#point) (1 pixel = 0.75 points). Returns the converted measurement as a **Single**.


## Syntax

_expression_.**PixelsToPoints** (_Value_)

_expression_ A variable that represents an **[Application](Publisher.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
|_Value_|Required| **Single**|The pixel value to be converted to points.|

## Return value

Single


## Remarks

Use the **[PointsToPixels](Publisher.Application.PointsToPixels.md)** method to convert measurements in points to pixels.


## Example

This example converts measurements in pixels entered by the user to measurements in points.

```vb
Dim strInput As String 
Dim strOutput As String 
 
Do While True 
 ' Get input from user. 
 strInput = InputBox( _ 
 Prompt:="Enter measurement in pixels (0 to cancel): ", _ 
 Default:="0") 
 
 ' Exit the loop if user enters zero. 
 If Val(strInput) = 0 Then Exit Do 
 
 ' Evaluate and display result. 
 strOutput = Trim(strInput) & " pixels = " _ 
 & Format(Application _ 
 .PixelsToPoints(Value:=Val(strInput)), _ 
 "0.00") & " points" 
 
 MsgBox strOutput 
Loop 

```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]