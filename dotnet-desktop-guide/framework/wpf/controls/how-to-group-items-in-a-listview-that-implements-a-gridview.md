---
title: 'Gewusst wie: Gruppieren von Elementen in einem ListView, in dem ein GridView implementiert ist'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], grouping items with GridViews
- grouping items in ListViews implementing GridViews [WPF]
- GridView controls [WPF], grouping items
ms.assetid: eebef25b-ddc6-424e-a66d-ea228d1bf33d
ms.openlocfilehash: b3dd6891976a942b299c87fca25e430e9ee59a51
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975499"
---
# <a name="how-to-group-items-in-a-listview-that-implements-a-gridview"></a>Gewusst wie: Gruppieren von Elementen in einem ListView, in dem ein GridView implementiert ist
In diesem Beispiel wird gezeigt, wie Gruppen von Elementen im <xref:System.Windows.Controls.GridView> Ansichtsmodus eines-Steuer Elements angezeigt werden <xref:System.Windows.Controls.ListView> .  
  
## <a name="example"></a>Beispiel  
 Um Gruppen von Elementen in einer anzuzeigen <xref:System.Windows.Controls.ListView> , definieren Sie eine <xref:System.Windows.Data.CollectionViewSource> . Das folgende Beispiel zeigt <xref:System.Windows.Data.CollectionViewSource> , wie Datenelemente gemäß dem Wert des `Catalog` Datenfelds gruppiert werden.  
  
 [!code-xaml[GridViewWithGroups#GroupingCollectionViewSource](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#groupingcollectionviewsource)]  
  
 Im folgenden Beispiel wird der <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> für den <xref:System.Windows.Controls.ListView> auf den festgelegt <xref:System.Windows.Data.CollectionViewSource> , der im vorherigen Beispiel definiert wurde. Im Beispiel wird auch ein definiert <xref:System.Windows.Controls.ItemsControl.GroupStyle%2A> , das ein-Steuerelement implementiert <xref:System.Windows.Controls.Expander> .  
  
 [!code-xaml[GridViewWithGroups#ListViewGroups](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewgroups)]  
[!code-xaml[GridViewWithGroups#ListViewEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewend)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
- [Übersicht über ListView](listview-overview.md)
- [Übersicht über GridView](gridview-overview.md)
