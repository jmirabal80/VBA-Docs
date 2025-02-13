---
title: Application.Build property (Access)
keywords: vbaac10.chm12600
f1_keywords:
- vbaac10.chm12600
ms.prod: access
api_name:
- Access.Application.Build
ms.assetid: d96de996-33f5-a4a1-66d9-c18b3cdbac43
ms.date: 02/05/2019
ms.localizationpriority: medium
---


# Application.Build property (Access)

Returns as a **Long** representing the build number of the currently installed copy of Microsoft Access. Read-only.


## Syntax

_expression_.**Build**

_expression_ A variable that represents an **[Application](Access.Application.md)** object.


## Example

The following example displays the version and build number of the currently-installed copy of Microsoft Access.


```vb
MsgBox "You are currently running Microsoft Access, " _ 
 & " version " & Application.Version & ", build " _ 
 & Application.Build & "."
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]