---
title: 'Gewusst wie: Verbessern der Leistung von TreeView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TreeView control [WPF], improving the performance
ms.assetid: b792c740-cf2b-4da8-8ba8-3d2e5a821874
ms.openlocfilehash: de1b46da2a7c6c3db0c0c19cdbb654fcf2fbbd6c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977188"
---
# <a name="how-to-improve-the-performance-of-a-treeview"></a><span data-ttu-id="c5d08-102">Gewusst wie: Verbessern der Leistung von TreeView</span><span class="sxs-lookup"><span data-stu-id="c5d08-102">How to: Improve the Performance of a TreeView</span></span>
<span data-ttu-id="c5d08-103">Wenn eine <xref:System.Windows.Controls.TreeView> zahlreiche Elemente enthält, kann die Zeitspanne, die zum Laden benötigt wird, zu einer erheblichen Verzögerung in der Benutzeroberfläche führen.</span><span class="sxs-lookup"><span data-stu-id="c5d08-103">If a <xref:System.Windows.Controls.TreeView> contains many items, the amount of time it takes to load may cause a significant delay in the user interface.</span></span> <span data-ttu-id="c5d08-104">Sie können die Ladezeit verbessern, indem Sie die `VirtualizingStackPanel.IsVirtualizing` angefügte-Eigenschaft auf festlegen `true` .</span><span class="sxs-lookup"><span data-stu-id="c5d08-104">You can improve the load time by setting the `VirtualizingStackPanel.IsVirtualizing` attached property to `true`.</span></span>  <span data-ttu-id="c5d08-105">Die Benutzeroberfläche kann auch langsam reagieren, wenn ein Benutzer mit <xref:System.Windows.Controls.TreeView> dem Mausrad oder dem Ziehpunkt einer Scrollleiste einen Bildlauf durchführt.</span><span class="sxs-lookup"><span data-stu-id="c5d08-105">The UI might also be slow to react when a user scrolls the <xref:System.Windows.Controls.TreeView> by using the mouse wheel or dragging the thumb of a scrollbar.</span></span> <span data-ttu-id="c5d08-106"><xref:System.Windows.Controls.TreeView>Durch Festlegen der `VirtualizingStackPanel.VirtualizationMode` angefügten-Eigenschaft auf können Sie die Leistung des verbessern, wenn der Benutzer einen Bildlauf durchführt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="c5d08-106">You can improve the performance of the <xref:System.Windows.Controls.TreeView> when the user scrolls by setting the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c5d08-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c5d08-107">Example</span></span>  
  
## <a name="description"></a><span data-ttu-id="c5d08-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5d08-108">Description</span></span>  
<span data-ttu-id="c5d08-109">Im folgenden Beispiel wird ein erstellt <xref:System.Windows.Controls.TreeView> , der die `VirtualizingStackPanel.IsVirtualizing` angefügte-Eigenschaft auf true und die `VirtualizingStackPanel.VirtualizationMode` angefügte-Eigenschaft auf festlegt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> , um die Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="c5d08-109">The following example creates a <xref:System.Windows.Controls.TreeView> that sets the `VirtualizingStackPanel.IsVirtualizing` attached property to true and the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> to optimize its performance.</span></span>  
  
## <a name="code"></a><span data-ttu-id="c5d08-110">Code</span><span class="sxs-lookup"><span data-stu-id="c5d08-110">Code</span></span>  
 [!code-xaml[RecycleItemContainerShippets#VirtualizingTreeView](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizingtreeview)]  
  
 <span data-ttu-id="c5d08-111">Das folgende Beispiel zeigt die Daten, die im vorherigen Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5d08-111">The following example shows the data that the previous example uses.</span></span>  
  
 [!code-csharp[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#treeviewdata)]
 [!code-vb[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#treeviewdata)]  
  
## <a name="see-also"></a><span data-ttu-id="c5d08-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5d08-112">See also</span></span>

- [<span data-ttu-id="c5d08-113">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c5d08-113">Controls</span></span>](../advanced/optimizing-performance-controls.md)
