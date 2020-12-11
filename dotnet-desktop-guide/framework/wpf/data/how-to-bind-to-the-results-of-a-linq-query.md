---
title: 'Gewusst wie: Binden an die Ergebnisse einer LINQ-Abfrage'
ms.date: 03/30/2017
helpviewer_keywords:
- running a LINQ query [WPF], bind to results
- binding to LINQ query results [WPF]
ms.assetid: ff2844d9-17ed-4ea6-aab1-5111af0bc684
ms.openlocfilehash: 47f39319f2d6a6c67361157afaceb6d605ce01d1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974655"
---
# <a name="how-to-bind-to-the-results-of-a-linq-query"></a>Gewusst wie: Binden an die Ergebnisse einer LINQ-Abfrage

In diesem Beispiel wird veranschaulicht, wie eine LINQ-Abfrage ausgeführt und anschließend an die Ergebnisse gebunden wird.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden zwei Listenfelder erstellt. Das erste Listenfeld enthält drei Listenelemente.

[!code-xaml[LinqExample#UI](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml#ui)]

Wenn Sie ein Element aus dem ersten Listenfeld auswählen, wird der folgende Ereignishandler aufgerufen. In diesem Beispiel `Tasks` ist eine Auflistung von- `Task` Objekten. Die- `Task` Klasse verfügt über eine-Eigenschaft mit dem Namen `Priority` . Dieser Ereignishandler führt eine LINQ-Abfrage aus, die die Auflistung von `Task` -Objekten mit dem ausgewählten Prioritätswert zurückgibt, und legt diese dann als fest <xref:System.Windows.FrameworkElement.DataContext%2A> :

[!code-csharp[LinqExample#Using](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#using)]
[!code-csharp[LinqExample#Tasks](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#tasks)]
[!code-csharp[LinqExample#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#handler)]

Das zweite Listenfeld wird an diese Auflistung gebunden, da der <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> Wert auf festgelegt ist `{Binding}` . Daraufhin wird die zurückgegebene Auflistung (basierend auf dem `myTaskTemplate` <xref:System.Windows.DataTemplate> ) angezeigt.

## <a name="see-also"></a>Siehe auch

- [Verfügbar machen von Daten für die Bindung in XAML](how-to-make-data-available-for-binding-in-xaml.md)
- [Binden an eine Sammlung und Anzeigen von Informationen auf Grundlage der Auswahl](how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [Neues in WPF Version 4.5](../getting-started/whats-new.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
