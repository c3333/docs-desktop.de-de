---
title: 'Gewusst wie: Abrufen der Standardansicht einer Datenauflistung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data collections [WPF], creating views of
- data binding [WPF], creating views of data collections
ms.assetid: b641e96c-c2f6-42ea-9c5d-bac81176ad65
ms.openlocfilehash: 17ec2a40bf2c274f50b39875a23541932438a317
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978142"
---
# <a name="how-to-get-the-default-view-of-a-data-collection"></a>Gewusst wie: Abrufen der Standardansicht einer Datenauflistung
In Sichten kann die gleiche Datensammlung je nach Sortier-, Filter-oder Gruppierungs Kriterien auf unterschiedliche Weise angezeigt werden. Jede Sammlung verfügt über eine freigegebene Standardansicht, die als tatsächliche Bindungs Quelle verwendet wird, wenn eine Bindung eine Auflistung als Quelle angibt. Dieses Beispiel zeigt, wie Sie die Standardansicht einer Auflistung erhalten.  
  
## <a name="example"></a>Beispiel  
 Um die Ansicht zu erstellen, benötigen Sie einen Objekt Verweis auf die Auflistung. Dieses Datenobjekt kann abgerufen werden, indem Sie auf Ihr eigenes Code-Behind-Objekt verweisen, indem Sie den Datenkontext erhalten, indem Sie eine Eigenschaft der Datenquelle erhalten oder eine Eigenschaft der Bindung erhalten. Dieses Beispiel zeigt, wie Sie den <xref:System.Windows.FrameworkElement.DataContext%2A> eines Datenobjekts abrufen und verwenden können, um die Standard Auflistungs Ansicht für diese Auflistung direkt abzurufen.  
  
 [!code-csharp[CollectionView#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#2)]
 [!code-vb[CollectionView#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#2)]  
  
 In diesem Beispiel ist das Stamm Element ein <xref:System.Windows.Controls.StackPanel> . Der <xref:System.Windows.FrameworkElement.DataContext%2A> wird auf *MyDatasource* festgelegt, was auf einen Datenanbieter verweist, <xref:System.Collections.ObjectModel.ObservableCollection%601> der ein von *Order* -Objekten ist.  
  
 [!code-xaml[CollectionView#CollectionViewDataContext](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml#collectionviewdatacontext)]  
  
 Alternativ können Sie mithilfe der-Klasse instanziieren und an Ihre eigene Auflistungs Ansicht binden <xref:System.Windows.Data.CollectionViewSource> . Diese Auflistungs Ansicht wird nur von Steuerelementen gemeinsam genutzt, die direkt an Sie gebunden werden. Ein Beispiel finden Sie im Abschnitt How to Create a View in der [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).  
  
 Beispiele für die von einer Auflistungs Ansicht bereitgestellte Funktionalität finden Sie unter [Sortieren von Daten in einer Ansicht](how-to-sort-data-in-a-view.md), [Filtern von Daten in einer Ansicht](how-to-filter-data-in-a-view.md)und [Navigieren durch die Objekte in einer Daten CollectionView](how-to-navigate-through-the-objects-in-a-data-collectionview.md).  
  
## <a name="see-also"></a>Siehe auch

- [Sortieren und Gruppieren von Daten mit einer Ansicht in XAML](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
