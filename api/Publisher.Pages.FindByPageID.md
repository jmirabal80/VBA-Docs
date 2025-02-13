---
title: Pages.FindByPageID method (Publisher)
keywords: vbapb10.chm458759
f1_keywords:
- vbapb10.chm458759
ms.prod: publisher
api_name:
- Publisher.Pages.FindByPageID
ms.assetid: 23ff5e69-33b1-e394-9d09-7199eae19fe9
ms.date: 06/12/2019
ms.localizationpriority: medium
---


# Pages.FindByPageID method (Publisher)

Returns a **[Page](Publisher.Page.md)** object that represents the page with the specified page ID number. Each page is automatically assigned a unique ID number when it is created. Use the **[PageID](Publisher.Page.PageID.md)** property to return a page's ID number.


## Syntax

_expression_.**FindByPageID** (_PageID_)

_expression_ A variable that represents a **[Pages](Publisher.Pages.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
|_PageID_|Required| **Long**|Specifies the ID number of the page that you want to return. Publisher assigns this number when the page is created.|

## Return value

Page


## Remarks

Unlike the **[PageIndex](Publisher.Page.PageIndex.md)** property, the **PageID** property of a **Page** object won't change when you add pages to or rearrange pages in the publication. Therefore, using the **FindByPageID** method with the page ID number can be a more reliable way to return a specific **Page** object from a **Pages** collection than using the **Item** method with the page's index number.


## Example

This example demonstrates how to retrieve the unique ID number for a **Page** object, and then use this number to return that **Page** object from the **Pages** collection and add a new shape to the page.

```vb
Sub FindPage() 
 Dim lngPageID As Long 
 
 'Get page ID 
 lngPageID = ActiveDocument.Pages.Add(Count:=1, After:=1).PageID 
 
 'Use page ID to add a new shape to the page 
 ActiveDocument.Pages.FindByPageID(PageID:=lngPageID) _ 
 .Shapes.AddShape Type:=msoShape5pointStar, _ 
 Left:=200, Top:=72, Width:=50, Height:=50 
 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]