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
# <a name="how-to-improve-the-performance-of-a-treeview"></a>Gewusst wie: Verbessern der Leistung von TreeView
Wenn eine <xref:System.Windows.Controls.TreeView> zahlreiche Elemente enthält, kann die Zeitspanne, die zum Laden benötigt wird, zu einer erheblichen Verzögerung in der Benutzeroberfläche führen. Sie können die Ladezeit verbessern, indem Sie die `VirtualizingStackPanel.IsVirtualizing` angefügte-Eigenschaft auf festlegen `true` .  Die Benutzeroberfläche kann auch langsam reagieren, wenn ein Benutzer mit <xref:System.Windows.Controls.TreeView> dem Mausrad oder dem Ziehpunkt einer Scrollleiste einen Bildlauf durchführt. <xref:System.Windows.Controls.TreeView>Durch Festlegen der `VirtualizingStackPanel.VirtualizationMode` angefügten-Eigenschaft auf können Sie die Leistung des verbessern, wenn der Benutzer einen Bildlauf durchführt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> .  
  
## <a name="example"></a>Beispiel  
  
## <a name="description"></a>BESCHREIBUNG  
Im folgenden Beispiel wird ein erstellt <xref:System.Windows.Controls.TreeView> , der die `VirtualizingStackPanel.IsVirtualizing` angefügte-Eigenschaft auf true und die `VirtualizingStackPanel.VirtualizationMode` angefügte-Eigenschaft auf festlegt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> , um die Leistung zu optimieren.  
  
## <a name="code"></a>Code  
 [!code-xaml[RecycleItemContainerShippets#VirtualizingTreeView](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizingtreeview)]  
  
 Das folgende Beispiel zeigt die Daten, die im vorherigen Beispiel verwendet werden.  
  
 [!code-csharp[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#treeviewdata)]
 [!code-vb[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#treeviewdata)]  
  
## <a name="see-also"></a>Siehe auch

- [Steuerelemente](../advanced/optimizing-performance-controls.md)
