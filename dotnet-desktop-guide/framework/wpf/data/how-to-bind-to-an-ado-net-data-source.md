---
title: 'Gewusst wie: Binden an eine ADO.NET-Datenquelle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], binding to ADO.NET data sources
- ADO.NET data sources [WPF], binding to
- binding [WPF], to ADO.NET data sources
ms.assetid: a70c6d7b-7b38-4fdf-b655-4804db7c8315
ms.openlocfilehash: d7ffaae472d89ebc23804c4032a75253756dc871
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972439"
---
# <a name="how-to-bind-to-an-adonet-data-source"></a>Gewusst wie: Binden an eine ADO.NET-Datenquelle

Dieses Beispiel zeigt, wie ein- [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] <xref:System.Windows.Controls.ListBox> Steuerelement an ein ADO.net-Element gebunden wird `DataSet` .

## <a name="example"></a>Beispiel

In diesem Beispiel wird ein `OleDbConnection`-Objekt zum Herstellen der Verbindung mit der Datenquelle verwendet, die als `Access MDB`-Datei in der Verbindungszeichenfolge angegeben ist. Nach dem Herstellen der Verbindung wird ein `OleDbDataAdapter`-Objekt erstellt. Das- `OleDbDataAdapter` Objekt führt eine SELECT strukturierte Abfragesprache (SQL)-Anweisung aus, um das Recordset aus der Datenbank abzurufen. Die Ergebnisse des SQL-Befehls werden in einer `DataTable` von gespeichert, `DataSet` indem die- `Fill` Methode von aufgerufen wird `OleDbDataAdapter` . Die `DataTable` in diesem Beispiel heißt `BookTable`. Im Beispiel wird dann die- <xref:System.Windows.FrameworkElement.DataContext%2A> Eigenschaft von <xref:System.Windows.Controls.ListBox> auf das-Objekt festgelegt `DataSet` .

[!code-csharp[ADODataSet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml.cs#1)]
[!code-vb[ADODataSet#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ADODataSet/VisualBasic/Window1.xaml.vb#1)]

Anschließend können Sie die- <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> Eigenschaft des an den binden <xref:System.Windows.Controls.ListBox> `BookTable` `DataSet` :

[!code-xaml[ADODataSet#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml#2)]

`BookItemTemplate` ist der <xref:System.Windows.DataTemplate> , der definiert, wie die Daten angezeigt werden:

[!code-xaml[ADODataSet#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml#3)]

`IntColorConverter` konvertiert `int` in eine Farbe. Bei Verwendung dieses Konverters <xref:System.Windows.Controls.TextBlock.Background%2A> wird die Farbe des dritten <xref:System.Windows.Controls.TextBlock> grün angezeigt, wenn der Wert von `NumPages` kleiner als 350 und andernfalls rot ist. Die Implementierung des Konverters wird hier nicht gezeigt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Data.BindingListCollectionView>
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
