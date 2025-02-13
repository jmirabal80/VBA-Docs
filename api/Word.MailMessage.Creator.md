---
title: MailMessage.Creator property (Word)
keywords: vbawd10.chm163185641
f1_keywords:
- vbawd10.chm163185641
ms.prod: word
api_name:
- Word.MailMessage.Creator
ms.assetid: 6e5fbcf4-965d-c932-fc6c-0f6d61cb53c0
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# MailMessage.Creator property (Word)

Returns a 32-bit integer that indicates the application in which the specified object was created. Read-only **Long**.


## Syntax

_expression_.**Creator**

_expression_ Required. A variable that represents a '[MailMessage](Word.MailMessage.md)' object.


## Remarks

If the object was created in Microsoft Word, the **Creator** property returns the hexadecimal number 4D535744, which represents the string "MSWD." This property was primarily designed to be used on the Macintosh, where each application has a four-character creator code. For example, Microsoft Word has the creator code MSWD. For additional information about this property, consult the language reference Help included with Microsoft Office Macintosh Edition.


## See also


[MailMessage Object](Word.MailMessage.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]