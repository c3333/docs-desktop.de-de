---
title: 'Gewusst wie: Filtern von Daten in einer Ansicht'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [WPF], filtering data
- filtering data in views [WPF]
- data binding [WPF], filtering data in views
ms.assetid: c76e8606-4cc4-45a8-9110-e2ec66dc6afd
ms.openlocfilehash: c015194609de507725a17fbe5d72e41d7027c68f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978146"
---
# <a name="how-to-filter-data-in-a-view"></a>Gewusst wie: Filtern von Daten in einer Ansicht
In diesem Beispiel wird gezeigt, wie Daten in einer Ansicht gefiltert werden.  
  
## <a name="example"></a>Beispiel  
 Zum Erstellen eines Filters definieren Sie eine Methode, die die Filter Logik bereitstellt. Die-Methode wird als Rückruf verwendet und akzeptiert einen Parameter vom Typ `object` . Die folgende Methode gibt alle- `Order` Objekte zurück, deren- `filled` Eigenschaft auf "No" festgelegt ist, und filtert die restlichen Objekte heraus.  
  
 [!code-csharp[SortFilter#2](~/samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#2)]
 [!code-vb[SortFilter#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#2)]  
  
 Sie können dann den Filter anwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel `myCollectionView` ist ein- <xref:System.Windows.Data.ListCollectionView> Objekt.  
  
 [!code-csharp[SortFilter#Filter](~/samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#filter)]
 [!code-vb[SortFilter#Filter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#filter)]  
  
 Um das Filtern rückgängig zu machen, können Sie die- <xref:System.Windows.Data.CollectionView.Filter%2A> Eigenschaft auf festlegen `null` :  
  
 [!code-csharp[SortFilter#Unfilter](~/samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#unfilter)]
 [!code-vb[SortFilter#Unfilter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#unfilter)]  
  
 Weitere Informationen zum Erstellen oder Abrufen einer Ansicht finden Sie unter Abrufen [der Standardansicht einer Datensammlung](how-to-get-the-default-view-of-a-data-collection.md). Das komplette Beispiel finden Sie unter [Sortieren und Filtern von Elementen in einem Ansichts](https://github.com/Microsoft/WPF-Samples/tree/master/Data%20Binding/SortFilter)Beispiel.  
  
 Wenn das View-Objekt von einem- <xref:System.Windows.Data.CollectionViewSource> Objekt stammt, wenden Sie Filter Logik an, indem Sie einen Ereignishandler für das- <xref:System.Windows.Data.CollectionViewSource.Filter> Ereignis festlegen. Im folgenden Beispiel `listingDataView` ist eine Instanz von <xref:System.Windows.Data.CollectionViewSource> .  
  
 [!code-csharp[DataBindingLab#10](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#10)]
 [!code-vb[DataBindingLab#10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#10)]  
  
 Im folgenden Beispiel wird die Implementierung des Beispiel `ShowOnlyBargainsFilter` Filter Ereignis Handlers veranschaulicht. Dieser Ereignishandler verwendet die- <xref:System.Windows.Data.FilterEventArgs.Accepted%2A> Eigenschaft, um `AuctionItem` Objekte auszufiltern, die über eine `CurrentPrice` von $25 oder höher verfügen.  
  
 [!code-csharp[DataBindingLab#5](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#5)]
 [!code-vb[DataBindingLab#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#5)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Data.CollectionView.CanFilter%2A>
- <xref:System.Windows.Data.BindingListCollectionView.CustomFilter%2A>
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Sortieren von Daten in einer Ansicht](how-to-sort-data-in-a-view.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
