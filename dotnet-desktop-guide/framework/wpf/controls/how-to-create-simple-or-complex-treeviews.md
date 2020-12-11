---
title: 'Gewusst wie: Erstellen einfacher und komplexer TreeViews'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], creating
- Control class [WPF], TreeView [WPF], creating
ms.assetid: 1defbb78-b8e7-4c0e-b650-576453ac828d
ms.openlocfilehash: 7edb4933ebcc0f0d2cb02754238c2342ee9dd4a2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977816"
---
# <a name="how-to-create-simple-or-complex-treeviews"></a>Gewusst wie: Erstellen einfacher und komplexer TreeViews
Dieses Beispiel zeigt, wie einfache oder komplexe Steuer <xref:System.Windows.Controls.TreeView> Elemente erstellt werden.  
  
 Ein <xref:System.Windows.Controls.TreeView> besteht aus einer Hierarchie von Steuer <xref:System.Windows.Controls.TreeViewItem> Elementen, die einfache Text Zeichenfolgen und außerdem komplexere Inhalte enthalten können, z. b. Steuer <xref:System.Windows.Controls.Button> Elemente oder ein <xref:System.Windows.Controls.StackPanel> mit eingebettetem Inhalt. Sie können den Inhalt explizit definieren, <xref:System.Windows.Controls.TreeView> oder eine Datenquelle kann den Inhalt bereitstellen. Dieses Thema enthält Beispiele für diese Konzepte.  
  
## <a name="example"></a>Beispiel  
 Die- <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> Eigenschaft des <xref:System.Windows.Controls.TreeViewItem> enthält den Inhalt, der von <xref:System.Windows.Controls.TreeView> für dieses Element angezeigt wird. Ein <xref:System.Windows.Controls.TreeViewItem> kann auch über Steuerelemente als untergeordnete Elemente verfügen, <xref:System.Windows.Controls.TreeViewItem> und Sie können diese untergeordneten Elemente mithilfe der- <xref:System.Windows.Controls.ItemsControl.Items%2A> Eigenschaft definieren.  
  
 Im folgenden Beispiel wird gezeigt, wie Sie Inhalte explizit definieren, <xref:System.Windows.Controls.TreeViewItem> indem Sie die- <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> Eigenschaft auf eine Text Zeichenfolge festlegen.  
  
 [!code-xaml[TreeViewSimple#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#1)]  
  
 Im folgenden Beispiel wird gezeigt, wie untergeordnete Elemente einer definiert <xref:System.Windows.Controls.TreeViewItem> werden, indem definiert <xref:System.Windows.Controls.ItemsControl.Items%2A> wird <xref:System.Windows.Controls.Button>  
  
 [!code-xaml[TreeViewSimple#3](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#3)]  
  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt wird, <xref:System.Windows.Controls.TreeView> in dem ein <xref:System.Windows.Data.XmlDataProvider> <xref:System.Windows.Controls.TreeViewItem> -Inhalt bereitstellt und eine <xref:System.Windows.HierarchicalDataTemplate> die Darstellung des Inhalts definiert.  
  
 [!code-xaml[TreeViewSimple#6](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#6)]  
  
 [!code-xaml[TreeViewSimple#7](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#7)]  
  
 [!code-xaml[TreeViewSimple#5](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#5)]  
  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt wird, <xref:System.Windows.Controls.TreeView> in dem der <xref:System.Windows.Controls.TreeViewItem> Inhalt Steuer <xref:System.Windows.Controls.DockPanel> Elemente enthält, die über eingebetteten Inhalt verfügen.  
  
 [!code-xaml[TreeViewSimple#9](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#9)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.TreeView>
- <xref:System.Windows.Controls.TreeViewItem>
- [Übersicht über TreeView](treeview-overview.md)
- [Artikel zu Vorgehensweisen](treeview-how-to-topics.md)
