---
title: 'Gewusst wie: Binden der Eigenschaften von zwei Steuerelementen'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], binding properties of two controls
- binding properties of two controls [WPF]
- controls [WPF], binding properties of
ms.assetid: 06318fac-6afd-4c7d-a277-6d7ef50f47bc
ms.openlocfilehash: 28b5f65a57fc210f3d405020daa0d75c28b934c8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972448"
---
# <a name="how-to-bind-the-properties-of-two-controls"></a><span data-ttu-id="adf30-102">Gewusst wie: Binden der Eigenschaften von zwei Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="adf30-102">How to: Bind the Properties of Two Controls</span></span>

<span data-ttu-id="adf30-103">In diesem Beispiel wird gezeigt, wie die-Eigenschaft eines instanziierten Steuer Elements mithilfe der-Eigenschaft an die eines anderen gebunden wird <xref:System.Windows.Data.Binding.ElementName%2A> .</span><span class="sxs-lookup"><span data-stu-id="adf30-103">This example shows how to bind the property of one instantiated control to that of another using the <xref:System.Windows.Data.Binding.ElementName%2A> property.</span></span>

## <a name="example"></a><span data-ttu-id="adf30-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="adf30-104">Example</span></span>

<span data-ttu-id="adf30-105">Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.Controls.Panel.Background%2A> Eigenschaft eines <xref:System.Windows.Controls.Canvas> an die [SelectedItem. Content](xref:System.Windows.Controls.ContentControl.Content%2A) -Eigenschaft einer gebunden wird <xref:System.Windows.Controls.ComboBox> :</span><span class="sxs-lookup"><span data-stu-id="adf30-105">The following example shows how to bind the <xref:System.Windows.Controls.Panel.Background%2A> property of a <xref:System.Windows.Controls.Canvas> to the [SelectedItem.Content](xref:System.Windows.Controls.ContentControl.Content%2A) property of a <xref:System.Windows.Controls.ComboBox>:</span></span>

[!code-xaml[BindDptoDp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/BindDPtoDP/CS/Window1.xaml#1)]

<span data-ttu-id="adf30-106">Bei Rendern dieses Beispiels sieht es folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="adf30-106">When this example is rendered it looks like the following:</span></span>

![Screenshot, der ein Kombinations Feld mit ausgewähltem grünen Wert und einem grünen Quadrat anzeigt](./media/how-to-bind-the-properties-of-two-controls/data-binding-bind-background-canvas.png)

> [!NOTE]
> <span data-ttu-id="adf30-108">Die Bindungs Ziel Eigenschaft (in diesem Beispiel die- <xref:System.Windows.Controls.Panel.Background%2A> Eigenschaft) muss eine Abhängigkeits Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="adf30-108">The binding target property (in this example, the <xref:System.Windows.Controls.Panel.Background%2A> property) must be a dependency property.</span></span> <span data-ttu-id="adf30-109">Weitere Informationen finden Sie unter [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).</span><span class="sxs-lookup"><span data-stu-id="adf30-109">For more information, see [Data Binding Overview](/dotnet/desktop-wpf/data/data-binding-overview).</span></span>

## <a name="see-also"></a><span data-ttu-id="adf30-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adf30-110">See also</span></span>

- [<span data-ttu-id="adf30-111">Angeben der Bindungs Quelle</span><span class="sxs-lookup"><span data-stu-id="adf30-111">Specify the Binding Source</span></span>](how-to-specify-the-binding-source.md)
- [<span data-ttu-id="adf30-112">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="adf30-112">How-to Topics</span></span>](data-binding-how-to-topics.md)
