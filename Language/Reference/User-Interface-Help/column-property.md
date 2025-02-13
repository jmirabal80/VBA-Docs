---
title: Column property (Microsoft Forms)
keywords: fm20.chm2000930
f1_keywords:
- fm20.chm2000930
ms.prod: office
api_name:
- Office.Column
ms.assetid: 989f9e98-8764-ca23-c90d-a64966568f86
ms.date: 09/15/2021
ms.localizationpriority: medium
---


# Column property (Microsoft Forms)

Specifies one or more items in a **[ListBox](listbox-control.md)** or **[ComboBox](combobox-control.md)**.

## Syntax

_object_.**Column(**_column, row_**)** [= _Variant_ ]

The **Column** property syntax has these parts:

|Part|Description|
|:-----|:-----|
| _object_|Required. A valid object.|
| _column_|Optional. An integer with a range from 0 to one less than the total number of columns.|
| _row_|Optional. An integer with a range from 0 to one less than the total number of rows.|
| _Variant_|Optional. Specifies a single value, a column of values, or a two-dimensional array to load into a **ListBox** or **ComboBox**.|

## Settings

If you specify both the column and row values, **Column** reads or writes a specific item.

If you specify only the column value, the **Column** property reads or writes the specified column in the current row of the object. For example, MyListBox.Column (3) reads or writes the third column in MyListBox.

**Column** returns a _Variant_ from the cursor. When a built-in [cursor](../../Glossary/glossary-vba.md#cursor) provides the value for _Variant_ (such as when using the **AddItem** method), the value is a string. When an external cursor provides the value for _Variant_, formatting associated with the data is not included in the _Variant_.

## Remarks

Use **Column** to assign the contents of a combo box or list box to another control, such as a text box. For example, you can set the **ControlSource** property of a text box to the value in the second column of a list box.
If the user makes no selection when you refer to a column in a combo box or list box, the **Column** setting is **Null**. You can check for this condition by using the IsNull function.

You can also use **Column** to copy an entire two-dimensional [array](../../Glossary/vbe-glossary.md#array) of values to a control. This syntax lets you quickly load a list of choices rather than individually loading each element of the list using **AddItem**.

> [!NOTE] 
> When copying data from a two-dimensional array, **Column** transposes the contents of the array in the control so that the contents of ListBox1.Column( _X_, _Y_ ) is the same as MyArray( _Y_, _X_ ). You can also use **List** to copy an array without transposing it.

## See also

- [Microsoft Forms examples](examples-microsoft-forms.md)
- [Microsoft Forms reference](reference-microsoft-forms.md)
- [Microsoft Forms concepts](concepts-microsoft-forms.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
