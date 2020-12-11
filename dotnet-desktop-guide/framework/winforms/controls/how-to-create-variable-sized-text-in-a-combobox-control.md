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
# <a name="how-to-create-variable-sized-text-in-a-combobox-control"></a><span data-ttu-id="ff02a-102">Vorgehensweise: Erstellen von Text mit variabler Größe in einem ComboBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ff02a-102">How to: Create Variable Sized Text in a ComboBox Control</span></span>
<span data-ttu-id="ff02a-103">Dieses Beispiel zeigt die benutzerdefinierte Zeichnung von Text in einem- <xref:System.Windows.Forms.ComboBox> Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ff02a-103">This example demonstrates custom drawing of text in a <xref:System.Windows.Forms.ComboBox> control.</span></span> <span data-ttu-id="ff02a-104">Wenn ein Element bestimmte Kriterien erfüllt, wird es in einer größeren Schriftart gezeichnet und rot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff02a-104">When an item meets a certain criteria, it is drawn in a larger font and turned red.</span></span>

## <a name="example"></a><span data-ttu-id="ff02a-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff02a-105">Example</span></span>

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

## <a name="compiling-the-code"></a><span data-ttu-id="ff02a-106">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="ff02a-106">Compiling the Code</span></span>
 <span data-ttu-id="ff02a-107">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ff02a-107">This example requires:</span></span>

- <span data-ttu-id="ff02a-108">Ein Windows Form.</span><span class="sxs-lookup"><span data-stu-id="ff02a-108">A Windows form.</span></span>

- <span data-ttu-id="ff02a-109">Ein- <xref:System.Windows.Forms.ComboBox> Steuerelement `ListBox1` mit dem Namen mit drei Elementen in der- <xref:System.Windows.Forms.ComboBox.Items%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ff02a-109">A <xref:System.Windows.Forms.ComboBox> control named `ListBox1` with three items in the <xref:System.Windows.Forms.ComboBox.Items%2A> property.</span></span> <span data-ttu-id="ff02a-110">In diesem Beispiel werden die drei Elemente benannt `"One", Two", and Three"` .</span><span class="sxs-lookup"><span data-stu-id="ff02a-110">In this example, the three items are named `"One", Two", and Three"`.</span></span> <span data-ttu-id="ff02a-111">Die- <xref:System.Windows.Forms.ComboBox.DrawMode%2A> Eigenschaft von `ComboBox1` muss auf festgelegt werden <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable> .</span><span class="sxs-lookup"><span data-stu-id="ff02a-111">The <xref:System.Windows.Forms.ComboBox.DrawMode%2A> property of `ComboBox1` must be set to <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable>.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff02a-112">Dieses Verfahren gilt auch für das- <xref:System.Windows.Forms.ListBox> Steuerelement – Sie können einen <xref:System.Windows.Forms.ListBox> für die ersetzen <xref:System.Windows.Forms.ComboBox> .</span><span class="sxs-lookup"><span data-stu-id="ff02a-112">This technique is also applicable to the <xref:System.Windows.Forms.ListBox> control — you can substitute a <xref:System.Windows.Forms.ListBox> for the <xref:System.Windows.Forms.ComboBox>.</span></span>

- <span data-ttu-id="ff02a-113">Verweise auf die Namespaces <xref:System.Windows.Forms?displayProperty=nameWithType> und <xref:System.Drawing?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ff02a-113">References to the <xref:System.Windows.Forms?displayProperty=nameWithType> and <xref:System.Drawing?displayProperty=nameWithType> namespaces.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff02a-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff02a-114">See also</span></span>

- <xref:System.Windows.Forms.ComboBox.DrawItem>
- <xref:System.Windows.Forms.DrawItemEventArgs>
- <xref:System.Windows.Forms.ComboBox.MeasureItem>
- [<span data-ttu-id="ff02a-115">Steuerelemente mit integrierter Ownerdrawing-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ff02a-115">Controls with Built-In Owner-Drawing Support</span></span>](controls-with-built-in-owner-drawing-support.md)
- [<span data-ttu-id="ff02a-116">ListBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ff02a-116">ListBox Control</span></span>](listbox-control-windows-forms.md)
- [<span data-ttu-id="ff02a-117">ComboBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ff02a-117">ComboBox Control</span></span>](combobox-control-windows-forms.md)
