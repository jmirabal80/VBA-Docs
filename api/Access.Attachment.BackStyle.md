---
title: Attachment.BackStyle property (Access)
keywords: vbaac10.chm13924
f1_keywords:
- vbaac10.chm13924
ms.prod: access
api_name:
- Access.Attachment.BackStyle
ms.assetid: 7e86f99d-a74a-8153-64ef-fe7cea81d218
ms.date: 02/07/2019
ms.localizationpriority: medium
---


# Attachment.BackStyle property (Access)

Use the **BackStyle** property to specify whether a control will be transparent. Read/write **Byte**.


## Syntax

_expression_.**BackStyle**

_expression_ A variable that represents an **[Attachment](Access.Attachment.md)** object.


## Remarks

The **BackStyle** property uses the following settings.

|Setting|Visual Basic|Description|
|:-----|:-----|:-----|
|Normal|1|(Default) The control has its interior color set by the **[BackColor](access.attachment.backcolor.md)** property.|
|Transparent|0|The control is transparent. The color of the form or report behind the control is visible.|

You can set the default for this property by using a control's default control style or the **[DefaultControl](access.form.defaultcontrol.md)** property in Visual Basic.

If the **Transparent** button on the **Back Color** button palette is selected, the **BackStyle** property is set to Transparent; otherwise, the **BackStyle** property is set to Normal.

To make a command button invisible, set its **Transparent** property to Yes.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]