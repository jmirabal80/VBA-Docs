---
title: InvisibleApp.Stat property (Visio)
keywords: vis_sdr.chm17514420
f1_keywords:
- vis_sdr.chm17514420
ms.prod: visio
api_name:
- Visio.InvisibleApp.Stat
ms.assetid: 6f6897e5-b7c9-8fe3-499b-3fc6252a6f58
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# InvisibleApp.Stat property (Visio)

Returns status information for an object. Read-only.


## Syntax

_expression_.**Stat**

_expression_ A variable that represents an **[InvisibleApp](Visio.InvisibleApp.md)** object.


## Return value

Integer


## Remarks

If an object is a reference to an entity in a document, and if that document closes, the **Stat** property returns a value in which the **visStatClosed** bit is set.

If an object is a reference to an entity that has been deleted, the **Stat** property returns a value in which the **visStatDeleted** bit is set.

A Component Object Model (COM) object, such as a Microsoft Visio **Document** object, lives as long as it is held (pointed to) by a client, even if the object is logically in a deleted or closed state.


## Example

This Microsoft Visual Basic for Applications (VBA) macro shows how to use the **Stat** property to check the status of a **Document** object. Executing the macro prints 0 (**visStatNormal**) and then 8 (**visStatClosed**) in the Immediate window.


```vb
 
Public Sub Stat_Example() 
 
 Dim vsoDocument As Visio.Document 
 Set vsoDocument = Documents.Add("") 
 Debug.Print vsoDocument.Stat 
 vsoDocument.Close 
 Debug.Print vsoDocument.Stat 
 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]