---
title: 'Vorgehensweise: Erstellen von Text mit variabler Größe in einem ComboBox-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- vb
helpviewer_keywords:
- text [Windows Forms], drawing in combo boxes
- examples [Windows Forms], ComboBox control
- combo boxes [Windows Forms], drawing text
- ComboBox control [Windows Forms], examples [C#]
- ComboBox control [Windows Forms], drawing custom text
ms.assetid: ce39b9ea-e626-49fe-bd5a-f567f6d157df
ms.openlocfilehash: acc5ee47536772d98fcfe98849335933c24a41d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975682"
---
# <a name="how-to-create-variable-sized-text-in-a-combobox-control"></a>Vorgehensweise: Erstellen von Text mit variabler Größe in einem ComboBox-Steuerelement
Dieses Beispiel zeigt die benutzerdefinierte Zeichnung von Text in einem- <xref:System.Windows.Forms.ComboBox> Steuerelement. Wenn ein Element bestimmte Kriterien erfüllt, wird es in einer größeren Schriftart gezeichnet und rot angezeigt.

## <a name="example"></a>Beispiel

```vb
Private Sub ComboBox1_MeasureItem(ByVal sender As Object, ByVal e As _
System.Windows.Forms.MeasureItemEventArgs) Handles ComboBox1.MeasureItem
    Dim bFont As New Font("Arial", 8, FontStyle.Bold)
    Dim lFont As New Font("Arial", 12, FontStyle.Bold)
    Dim siText As SizeF

    If ComboBox1.Items().Item(e.Index) = "Two" Then
        siText = e.Graphics.MeasureString(ComboBox1.Items().Item(e.Index), _
lFont)
    Else
        siText = e.Graphics.MeasureString(ComboBox1.Items().Item(e.Index), bFont)
    End If

    e.ItemHeight = siText.Height
    e.ItemWidth = siText.Width
End Sub

Private Sub ComboBox1_DrawItem(ByVal sender As Object, ByVal e As _
System.Windows.Forms.DrawItemEventArgs) Handles ComboBox1.DrawItem
    Dim g As Graphics = e.Graphics
    Dim bFont As New Font("Arial", 8, FontStyle.Bold)
    Dim lFont As New Font("Arial", 12, FontStyle.Bold)

    If ComboBox1.Items().Item(e.Index) = "Two" Then
        g.DrawString(ComboBox1.Items.Item(e.Index), lfont, Brushes.Red, _
e.Bounds.X, e.Bounds.Y)
    Else
        g.DrawString(ComboBox1.Items.Item(e.Index), bFont, Brushes.Black, e.Bounds.X, e.Bounds.Y)
    End If
End Sub
```

## <a name="compiling-the-code"></a>Kompilieren des Codes
 Für dieses Beispiel benötigen Sie Folgendes:

- Ein Windows Form.

- Ein- <xref:System.Windows.Forms.ComboBox> Steuerelement `ListBox1` mit dem Namen mit drei Elementen in der- <xref:System.Windows.Forms.ComboBox.Items%2A> Eigenschaft. In diesem Beispiel werden die drei Elemente benannt `"One", Two", and Three"` . Die- <xref:System.Windows.Forms.ComboBox.DrawMode%2A> Eigenschaft von `ComboBox1` muss auf festgelegt werden <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable> .

    > [!NOTE]
    > Dieses Verfahren gilt auch für das- <xref:System.Windows.Forms.ListBox> Steuerelement – Sie können einen <xref:System.Windows.Forms.ListBox> für die ersetzen <xref:System.Windows.Forms.ComboBox> .

- Verweise auf die Namespaces <xref:System.Windows.Forms?displayProperty=nameWithType> und <xref:System.Drawing?displayProperty=nameWithType>.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ComboBox.DrawItem>
- <xref:System.Windows.Forms.DrawItemEventArgs>
- <xref:System.Windows.Forms.ComboBox.MeasureItem>
- [Steuerelemente mit integrierter Ownerdrawing-Unterstützung](controls-with-built-in-owner-drawing-support.md)
- [ListBox-Steuerelement](listbox-control-windows-forms.md)
- [ComboBox-Steuerelement](combobox-control-windows-forms.md)
