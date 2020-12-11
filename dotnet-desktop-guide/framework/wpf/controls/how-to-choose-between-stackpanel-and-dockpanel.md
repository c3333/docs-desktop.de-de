---
title: 'Gewusst wie: Auswählen von StackPanel oder DockPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], StackPanel control compared to
- StackPanel control [WPF], DockPanel control compared to
- controls [WPF], StackPanel
ms.assetid: f9239086-451f-42e6-81f7-ef89ef349742
ms.openlocfilehash: bdf4b38e67a7856136224368e86609c135e5ad6f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978086"
---
# <a name="how-to-choose-between-stackpanel-and-dockpanel"></a><span data-ttu-id="981fa-102">Gewusst wie: Auswählen von StackPanel oder DockPanel</span><span class="sxs-lookup"><span data-stu-id="981fa-102">How to: Choose Between StackPanel and DockPanel</span></span>
<span data-ttu-id="981fa-103">In diesem Beispiel wird gezeigt, wie Sie zwischen <xref:System.Windows.Controls.StackPanel> der Verwendung eines oder eines auswählen, <xref:System.Windows.Controls.DockPanel> Wenn Sie Inhalt in einem Stapeln <xref:System.Windows.Controls.Panel> .</span><span class="sxs-lookup"><span data-stu-id="981fa-103">This example shows how to choose between using a <xref:System.Windows.Controls.StackPanel> or a <xref:System.Windows.Controls.DockPanel> when you stack content in a <xref:System.Windows.Controls.Panel>.</span></span>

## <a name="example"></a><span data-ttu-id="981fa-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="981fa-104">Example</span></span>
 <span data-ttu-id="981fa-105">Obwohl Sie entweder <xref:System.Windows.Controls.DockPanel> oder <xref:System.Windows.Controls.StackPanel> zum Stapeln untergeordneter Elemente verwenden können, werden die beiden-Steuerelemente nicht immer die gleichen Ergebnisse liefern.</span><span class="sxs-lookup"><span data-stu-id="981fa-105">Although you can use either <xref:System.Windows.Controls.DockPanel> or <xref:System.Windows.Controls.StackPanel> to stack child elements, the two controls do not always produce the same results.</span></span> <span data-ttu-id="981fa-106">Beispielsweise kann sich die Reihenfolge, in der Sie untergeordnete Elemente platzieren, auf die Größe der untergeordneten Elemente in einer, <xref:System.Windows.Controls.DockPanel> aber nicht in einer auswirken <xref:System.Windows.Controls.StackPanel> .</span><span class="sxs-lookup"><span data-stu-id="981fa-106">For example, the order that you place child elements can affect the size of child elements in a <xref:System.Windows.Controls.DockPanel> but not in a <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="981fa-107">Dieses unterschiedliche Verhalten tritt <xref:System.Windows.Controls.StackPanel> auf, weil Measures in der Stapel Richtung bei [Double. PositiveInfinity](xref:System.Double.PositiveInfinity), jedoch <xref:System.Windows.Controls.DockPanel> nur die verfügbare Größe messen.</span><span class="sxs-lookup"><span data-stu-id="981fa-107">This different behavior occurs because <xref:System.Windows.Controls.StackPanel> measures in the direction of stacking at [Double.PositiveInfinity](xref:System.Double.PositiveInfinity); however, <xref:System.Windows.Controls.DockPanel> measures only the available size.</span></span>

 <span data-ttu-id="981fa-108">Im folgenden Beispiel wird dieser Hauptunterschied zwischen <xref:System.Windows.Controls.DockPanel> und veranschaulicht <xref:System.Windows.Controls.StackPanel> .</span><span class="sxs-lookup"><span data-stu-id="981fa-108">The following example demonstrates this key difference between <xref:System.Windows.Controls.DockPanel> and <xref:System.Windows.Controls.StackPanel>.</span></span>

 [!code-cpp[StackPanelOvw4#1](~/samples/snippets/cpp/VS_Snippets_Wpf/StackPanelOvw4/CPP/StackPanel_Ovw_Sample4.cpp#1)]
 [!code-csharp[StackPanelOvw4#1](~/samples/snippets/csharp/VS_Snippets_Wpf/StackPanelOvw4/CSharp/StackPanel_Ovw_Sample4.cs#1)]
 [!code-vb[StackPanelOvw4#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StackPanelOvw4/VisualBasic/StackPanelSamp.vb#1)]
 [!code-xaml[StackPanelOvw4#1](~/samples/snippets/xaml/VS_Snippets_Wpf/StackPanelOvw4/XAML/default.xaml#1)]

## <a name="see-also"></a><span data-ttu-id="981fa-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="981fa-109">See also</span></span>

- <xref:System.Windows.Controls.StackPanel>
- <xref:System.Windows.Controls.DockPanel>
- [<span data-ttu-id="981fa-110">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="981fa-110">Panels Overview</span></span>](panels-overview.md)
