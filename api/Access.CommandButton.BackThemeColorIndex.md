---
title: CommandButton.BackThemeColorIndex property (Access)
keywords: vbaac10.chm14631
f1_keywords:
- vbaac10.chm14631
ms.prod: access
api_name:
- Access.CommandButton.BackThemeColorIndex
ms.assetid: 891e6d86-5935-1d75-1cda-ea5bcb422583
ms.date: 02/28/2019
ms.localizationpriority: medium
---


# CommandButton.BackThemeColorIndex property (Access)

Gets or sets a value that represents a color in the applied color theme associated with the **BackColor** property of the specified object. Read/write **Long**.


## Syntax

_expression_.**BackThemeColorIndex**

_expression_ A variable that represents a **[CommandButton](Access.CommandButton.md)** object.


## Remarks

The **BackThemeColorIndex** property contains one of the index values listed in the following table.

|Index value|Description|
|:-----|:-----|
|0|Text 1|
|1|Background 1|
|2|Text 2|
|3|Background 2|
|4|Accent 1|
|5|Accent 2|
|6|Accent 3|
|7|Accent 4|
|8|Accent 5|
|9|Accent 6|
|10|Hyperlink|
|11|Followed Hyperlink|

If no theme is applied, the **BackThemeColorIndex** property contains -1.

This property is not surfaced in the property sheet.


## Example

The following code example sets the background color to the Text 2 color by setting the **BackThemeColorIndex** property.

```vb
Me.FormHeader.BackThemeColorIndex=2
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]