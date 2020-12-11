---
title: 'Gewusst wie: Sortieren von Daten in einer Ansicht'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], sorting data in views
- data binding [WPF], grouping data in views
- grouping data in views [WPF]
- views [WPF], sorting data
- views [WPF], grouping data
- sorting data in views [WPF]
ms.assetid: f4c43578-01b7-4774-a953-acb95a13b94a
ms.openlocfilehash: 4ff90cc58cb3d7ceee0be2fd7f6ddaaa27df4cef
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977332"
---
# <a name="how-to-sort-data-in-a-view"></a>Gewusst wie: Sortieren von Daten in einer Ansicht
In diesem Beispiel wird beschrieben, wie Daten in einer Ansicht sortiert werden.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein einfaches <xref:System.Windows.Controls.ListBox> und ein erstellt <xref:System.Windows.Controls.Button> :  
  
 [!code-xaml[ListBoxSort_snip#HowTo](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxSort_snip/CSharp/Window1.xaml#howto)]  
  
 Der- <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignishandler der Schaltfläche enthält Logik zum Sortieren der Elemente in der <xref:System.Windows.Controls.ListBox> absteigenden Reihenfolge. Dies ist möglich, da durch das Hinzufügen von Elementen zu einer auf <xref:System.Windows.Controls.ListBox> diese Weise die <xref:System.Windows.Controls.ItemCollection> der <xref:System.Windows.Controls.ListBox> -Klasse hinzugefügt und <xref:System.Windows.Controls.ItemCollection> von der-Klasse abgeleitet wird <xref:System.Windows.Data.CollectionView> . Wenn Sie <xref:System.Windows.Controls.ListBox> das mithilfe der-Eigenschaft an eine Sammlung binden <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> , können Sie das gleiche Verfahren für die Sortierung verwenden.  
  
 [!code-csharp[ListBoxSort_snip#HowToCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxSort_snip/CSharp/Window1.xaml.cs#howtocode)]
 [!code-vb[ListBoxSort_snip#HowToCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListBoxSort_snip/visualbasic/window1.xaml.vb#howtocode)]  
  
 Solange Sie über einen Verweis auf das Ansichts Objekt verfügen, können Sie das gleiche Verfahren verwenden, um den Inhalt anderer Auflistungs Ansichten zu sortieren. Ein Beispiel zum Abrufen einer Ansicht finden Sie unter Abrufen [der Standardansicht einer Datensammlung](how-to-get-the-default-view-of-a-data-collection.md). Ein weiteres Beispiel finden Sie unter [Sortieren einer GridView-Spalte beim Klicken auf einen Header](../controls/how-to-sort-a-gridview-column-when-a-header-is-clicked.md). Weitere Informationen zu Ansichten finden Sie unterbinden an Auflistungen in der Übersicht über die [Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).  
  
 Ein Beispiel für das Anwenden von Sortier Logik in [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] finden Sie unter [Sortieren und Gruppieren von Daten mit einer Ansicht in XAML](how-to-sort-and-group-data-using-a-view-in-xaml.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Data.ListCollectionView.CustomSort%2A>
- [Sortieren einer GridView-Spalte beim Klicken auf einen Header](../controls/how-to-sort-a-gridview-column-when-a-header-is-clicked.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Filtern von Daten in einer Ansicht](how-to-filter-data-in-a-view.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
