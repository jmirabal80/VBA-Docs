---
title: Master.SelectionDeleteCanceled event (Visio)
keywords: vis_sdr.chm10719365
f1_keywords:
- vis_sdr.chm10719365
ms.prod: visio
api_name:
- Visio.Master.SelectionDeleteCanceled
ms.assetid: 87ecdfcb-616f-0b47-bfa4-216ef456deaa
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Master.SelectionDeleteCanceled event (Visio)

Occurs after an event handler has returned **True** (cancel) to a **QueryCancelSelectionDelete** event.


## Syntax

_expression_.**SelectionDeleteCanceled** (_Selection_)

_expression_ A variable that represents a **[Master](Visio.Master.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Selection_|Required| **[IVSELECTION]**|The selection of shapes that was going to be deleted.|

## Remarks

If you are using Microsoft Visual Basic or Visual Basic for Applications (VBA), the syntax in this topic describes a common, efficient way to handle events.

If you want to create your own **Event** objects, use the **[Add](visio.eventlist.add.md)** or **[AddAdvise](visio.eventlist.addadvise.md)** method. 

To create an **Event** object that runs an add-on, use the **Add** method as it applies to the **EventList** collection. 

To create an **Event** object that receives notification, use the **AddAdvise** method. 

To find an event code for the event that you want to create, see [Event codes](../visio/Concepts/event-codesvisio.md).

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]