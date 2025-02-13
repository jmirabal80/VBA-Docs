---
title: Shape.Line property (Publisher)
keywords: vbapb10.chm2228290
f1_keywords:
- vbapb10.chm2228290
ms.prod: publisher
api_name:
- Publisher.Shape.Line
ms.assetid: 3d53f917-87ad-159d-65c3-e6fdfa72b15e
ms.date: 06/13/2019
ms.localizationpriority: medium
---


# Shape.Line property (Publisher)

Returns a **[LineFormat](Publisher.LineFormat.md)** object that contains line formatting properties for the specified shape. For a line, the **LineFormat** object represents the line itself; for a shape with a border, the **LineFormat** object represents the border.


## Syntax

_expression_.**Line**

_expression_ A variable that represents a **[Shape](Publisher.Shape.md)** object.


## Example

This example adds a blue dashed line to the active publication.

```vb
With ActiveDocument.Pages(1).Shapes _ 
 .AddLine(BeginX:=10, BeginY:=10, _ 
 EndX:=250, EndY:=250).Line 
 .DashStyle = msoLineDashDotDot 
 .ForeColor.RGB = RGB(50, 0, 128) 
End With
```

<br/>

This example adds a cross to the first page and then sets its border to be 8 points thick and red.

```vb
With ActiveDocument.Pages(1).Shapes _ 
 .AddShape(Type:=msoShapeCross, _ 
 Left:=10, Top:=10, Width:=50, Height:=70).Line 
 .Weight = 8 
 .ForeColor.RGB = RGB(255, 0, 0) 
End With
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]