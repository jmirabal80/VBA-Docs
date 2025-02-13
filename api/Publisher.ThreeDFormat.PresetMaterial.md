---
title: ThreeDFormat.PresetMaterial property (Publisher)
keywords: vbapb10.chm3801351
f1_keywords:
- vbapb10.chm3801351
ms.prod: publisher
api_name:
- Publisher.ThreeDFormat.PresetMaterial
ms.assetid: 5f12fb22-f596-0d59-1f02-63ce8d4bd927
ms.date: 06/15/2019
ms.localizationpriority: medium
---


# ThreeDFormat.PresetMaterial property (Publisher)

Returns or sets an **[MsoPresetMaterial](Office.MsoPresetMaterial.md)** constant that represents the extrusion surface material. Read/write.


## Syntax

_expression_.**PresetMaterial**

_expression_ A variable that represents a **[ThreeDFormat](Publisher.ThreeDFormat.md)** object.


## Return value

MsoPresetMaterial


## Remarks

The **PresetMaterial** property value can be one of the **MsoPresetMaterial** constants declared in the Microsoft Office type library.


## Example

This example specifies that the extrusion surface for shape one in the active publication be a wireframe. For this example to work, the specified shape must be a 3D shape.

```vb
Sub SetExtrusionMaterial() 
 With ActiveDocument.Pages(1).Shapes(1).ThreeD 
 .Visible = True 
 .PresetMaterial = msoMaterialWireFrame 
 End With 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]