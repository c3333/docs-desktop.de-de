---
title: 'Gewusst wie: Navigieren durch die Objekte in einer Datenauflistungsansicht'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CollectionView [WPF], navigating through objects
- data binding [WPF], navigating through objects in data CollectionView
- navigating through objects in data CollectionView [WPF]
ms.assetid: fcd37590-bce1-4ac9-8b74-3b96c7458b8a
ms.openlocfilehash: dc8b1e0dec0f99c3537587fe60cbecf165047f44
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975959"
---
# <a name="how-to-navigate-through-the-objects-in-a-data-collectionview"></a>Gewusst wie: Navigieren durch die Objekte in einer Datenauflistungsansicht
Sichten ermöglichen, dass dieselbe Datensammlung in Abhängigkeit von Sortierung, Filterung oder Gruppierung auf verschiedene Weise angezeigt wird. Sichten stellen auch ein Aktuelles Datensatz-Zeiger Konzept bereit und ermöglichen das Verschieben des Zeigers. In diesem Beispiel wird gezeigt, wie das aktuelle-Objekt und die in der-Klasse bereitgestellten Funktionen durch die Objekte in einer Daten Auflistung navigiert werden <xref:System.Windows.Data.CollectionView> .  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel `myCollectionView` ist ein- <xref:System.Windows.Data.CollectionView> Objekt, das eine Ansicht über eine gebundene Auflistung ist.  
  
 Im folgenden Beispiel `OnButton` ist ein Ereignishandler für die Schaltflächen `Previous` und `Next` in einer Anwendung, bei denen es sich um Schaltflächen handelt, die es dem Benutzer ermöglichen, in der Datensammlung zu navigieren. Beachten Sie, dass die <xref:System.Windows.Data.CollectionView.IsCurrentBeforeFirst%2A> -Eigenschaft und die-Eigenschaft melden, <xref:System.Windows.Data.CollectionView.IsCurrentAfterLast%2A> ob der aktuelle Daten Satz Zeiger am Anfang und am Ende der Liste steht, sodass <xref:System.Windows.Data.CollectionView.MoveCurrentToFirst%2A> und <xref:System.Windows.Data.CollectionView.MoveCurrentToLast%2A> entsprechend aufgerufen werden können.  
  
 Die- <xref:System.Windows.Data.CollectionView.CurrentItem%2A> Eigenschaft der Sicht wird `Order` in umgewandelt, um das aktuelle Bestell Element in der Auflistung zurückzugeben.  
  
 [!code-csharp[CollectionView#OnButton](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#onbutton)]
 [!code-vb[CollectionView#OnButton](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#onbutton)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Sortieren von Daten in einer Ansicht](how-to-sort-data-in-a-view.md)
- [Filtern von Daten in einer Ansicht](how-to-filter-data-in-a-view.md)
- [Sortieren und Gruppieren von Daten mit einer Ansicht in XAML](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
