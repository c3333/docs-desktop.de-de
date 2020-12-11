---
title: 'Gewusst wie: Suchen eines TreeViewItem-Elements in TreeView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TreeView control [WPF], finding a TreeViewItem
- TreeViewItem [WPF], finding
ms.assetid: 72ecd40c-3939-4e01-b617-5e9daa6074d9
ms.openlocfilehash: ad72c7a7fb11dfe605db4119dde831b47dd7c5a4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975509"
---
# <a name="how-to-find-a-treeviewitem-in-a-treeview"></a>Gewusst wie: Suchen eines TreeViewItem-Elements in TreeView
Das- <xref:System.Windows.Controls.TreeView> Steuerelement stellt eine bequeme Möglichkeit zum Anzeigen hierarchischer Daten dar. Wenn Ihr <xref:System.Windows.Controls.TreeView> an eine Datenquelle gebunden ist, stellt die- <xref:System.Windows.Controls.TreeView.SelectedItem%2A> Eigenschaft eine bequeme Methode zum schnellen Abrufen des ausgewählten Datenobjekts bereit. Es ist in der Regel am besten, mit dem zugrunde liegenden Datenobjekt zu arbeiten. manchmal müssen Sie jedoch möglicherweise die enthaltenden Daten Programm gesteuert bearbeiten <xref:System.Windows.Controls.TreeViewItem> . Beispielsweise müssen Sie möglicherweise Programm gesteuert erweitern <xref:System.Windows.Controls.TreeViewItem> oder ein anderes Element in der auswählen <xref:System.Windows.Controls.TreeView> .  
  
 Um einen zu suchen, der <xref:System.Windows.Controls.TreeViewItem> ein bestimmtes Datenobjekt enthält, müssen Sie jede Ebene von durchlaufen <xref:System.Windows.Controls.TreeView> . Die Elemente in einer <xref:System.Windows.Controls.TreeView> können auch virtualisiert werden, um die Leistung zu verbessern. Wenn Elemente virtualisiert werden können, müssen Sie auch einen erkennen, <xref:System.Windows.Controls.TreeViewItem> um zu überprüfen, ob das Datenobjekt enthalten ist.  
  
## <a name="example"></a>Beispiel  
  
## <a name="description"></a>BESCHREIBUNG  
 Im folgenden Beispiel wird ein <xref:System.Windows.Controls.TreeView> -Objekt für ein bestimmtes-Objekt durchsucht und die enthaltende des Objekts zurückgegeben <xref:System.Windows.Controls.TreeViewItem> . Im Beispiel wird sichergestellt, dass jede <xref:System.Windows.Controls.TreeViewItem> instanziiert wird, sodass die untergeordneten Elemente durchsucht werden können. Dieses Beispiel kann auch verwendet werden, wenn <xref:System.Windows.Controls.TreeView> keine virtualisierten Elemente verwendet.  
  
> [!NOTE]
> Das folgende Beispiel funktioniert <xref:System.Windows.Controls.TreeView> unabhängig vom zugrunde liegenden Datenmodell, und sucht alle, <xref:System.Windows.Controls.TreeViewItem> bis das-Objekt gefunden wird. Ein weiteres Verfahren, das eine bessere Leistung bietet, ist das Durchsuchen des Datenmodells nach dem angegebenen Objekt, das Nachverfolgen seines Speicher Orts in der Daten Hierarchie und das anschließende suchen der entsprechenden <xref:System.Windows.Controls.TreeViewItem> in der <xref:System.Windows.Controls.TreeView> . Das Verfahren, das eine bessere Leistung bietet, erfordert jedoch Kenntnisse des Datenmodells und kann nicht für eine bestimmte verallgemeinert werden <xref:System.Windows.Controls.TreeView> .  
  
## <a name="code"></a>Code  
 [!code-csharp[TreeViewFindTVI#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewFindTVI/CSharp/MainWindow.xaml.cs#1)]
 [!code-vb[TreeViewFindTVI#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TreeViewFindTVI/VisualBasic/MainWindow.xaml.vb#1)]  
  
 Der vorherige Code basiert auf einem benutzerdefinierten <xref:System.Windows.Controls.VirtualizingStackPanel> , das eine Methode mit dem Namen verfügbar macht `BringIntoView` . Im folgenden Code wird der benutzerdefinierte definiert <xref:System.Windows.Controls.VirtualizingStackPanel> .  
  
 [!code-csharp[TreeViewFindTVI#2](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewFindTVI/CSharp/MainWindow.xaml.cs#2)]
 [!code-vb[TreeViewFindTVI#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TreeViewFindTVI/VisualBasic/MainWindow.xaml.vb#2)]  
  
 Der folgende XAML-Code zeigt, wie Sie einen erstellen <xref:System.Windows.Controls.TreeView> , der den benutzerdefinierten verwendet <xref:System.Windows.Controls.VirtualizingStackPanel> .  
  
 [!code-xaml[TreeViewFindTVI#3](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewFindTVI/CSharp/MainWindow.xaml#3)]  
  
## <a name="see-also"></a>Siehe auch

- [Verbessern der Leistung eines TreeView-Objekts](how-to-improve-the-performance-of-a-treeview.md)
