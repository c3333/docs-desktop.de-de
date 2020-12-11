---
title: 'Gewusst wie: Verwenden von Triggern zum Formatieren ausgewählter Elemente in einem ListView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 1e2bdce0-afe8-4507-9b18-f33de43de25a
ms.openlocfilehash: ad64382b871bae9114a1e63257de3f8595376923
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977084"
---
# <a name="how-to-use-triggers-to-style-selected-items-in-a-listview"></a>Gewusst wie: Verwenden von Triggern zum Formatieren ausgewählter Elemente in einem ListView
In diesem Beispiel wird gezeigt, wie <xref:System.Windows.Style.Triggers%2A> für ein Steuerelement definiert <xref:System.Windows.Controls.ListViewItem> wird, sodass bei einer Änderung des Eigenschafts Werts eine der <xref:System.Windows.Controls.ListViewItem> <xref:System.Windows.Style> <xref:System.Windows.Controls.ListViewItem> Änderungen in der Antwort.  
  
## <a name="example"></a>Beispiel  
 Wenn Sie möchten <xref:System.Windows.Style> , dass sich die eines <xref:System.Windows.Controls.ListViewItem> in Reaktion auf Eigenschafts Änderungen ändert, definieren Sie <xref:System.Windows.Style.Triggers%2A> für die <xref:System.Windows.Style> Änderung.  
  
 Im folgenden Beispiel wird ein definiert <xref:System.Windows.Trigger> , mit dem die <xref:System.Windows.Controls.Control.Foreground%2A> -Eigenschaft auf festgelegt wird <xref:System.Windows.Media.Brushes.Blue%2A> und der geändert wird <xref:System.Windows.FrameworkElement.Cursor%2A> , <xref:System.Windows.Input.CursorType.Hand> Wenn die- <xref:System.Windows.UIElement.IsMouseOver%2A> Eigenschaft in geändert wird `true` .  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#Trigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#trigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
 Im folgenden Beispiel wird ein definiert <xref:System.Windows.MultiTrigger> , mit dem die <xref:System.Windows.Controls.Control.Foreground%2A> -Eigenschaft eines auf festgelegt <xref:System.Windows.Controls.ListViewItem> wird, <xref:System.Windows.Media.Brushes.Yellow%2A> Wenn das <xref:System.Windows.Controls.ListViewItem> das ausgewählte Element ist und über den Tastaturfokus verfügt.  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#MultiTrigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#multitrigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
- [Übersicht über ListView](listview-overview.md)
- [Übersicht über GridView](gridview-overview.md)
