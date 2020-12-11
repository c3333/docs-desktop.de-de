---
title: 'Gewusst wie: Ändern der horizontalen Ausrichtung einer Spalte in einem ListView-Element'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], horizontal alignment [WPF]
ms.assetid: b9573e44-9dad-4d14-939c-7859ca372758
ms.openlocfilehash: cdf479fc9f84f88fccc877e9fdf8ca56d53c1c4b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977468"
---
# <a name="how-to-change-the-horizontal-alignment-of-a-column-in-a-listview"></a>Gewusst wie: Ändern der horizontalen Ausrichtung einer Spalte in einem ListView-Element
Standardmäßig ist der Inhalt jeder Spalte in einem <xref:System.Windows.Controls.ListViewItem> linksbündig ausgerichtet. Sie können die Ausrichtung der einzelnen Spalten ändern, indem Sie eine bereitstellen <xref:System.Windows.DataTemplate> und die- <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschaft für das-Element in der festlegen <xref:System.Windows.DataTemplate> . In diesem Thema wird gezeigt <xref:System.Windows.Controls.ListView> , wie der Inhalt von a standardmäßig ausgerichtet wird und wie die Ausrichtung einer Spalte in einer geändert wird <xref:System.Windows.Controls.ListView> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden die Daten in der `Title` `ISBN` -Spalte und der-Spalte linksbündig ausgerichtet.  
  
 [!code-xaml[ListViewHowTos#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#1)]  
[!code-xaml[ListViewHowTos#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#2)]  
  
 Um die Ausrichtung der Spalte zu ändern `ISBN` , müssen Sie angeben, dass die- <xref:System.Windows.Controls.Control.HorizontalContentAlignment%2A> Eigenschaft jedes-Objekts <xref:System.Windows.Controls.ListViewItem> ist <xref:System.Windows.HorizontalAlignment.Stretch> , damit die Elemente in <xref:System.Windows.Controls.ListViewItem> den einzelnen Spalten die gesamte Breite der einzelnen Spalten überspannen oder positionieren können. Da <xref:System.Windows.Controls.ListView> an eine Datenquelle gebunden ist, müssen Sie einen Stil erstellen, der den festlegt <xref:System.Windows.Controls.Control.HorizontalContentAlignment%2A> . Als nächstes müssen Sie einen verwenden, <xref:System.Windows.DataTemplate> um den Inhalt anzuzeigen, anstatt die- <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> Eigenschaft zu verwenden. Um die `ISBN` jeder Vorlage anzuzeigen, kann die <xref:System.Windows.DataTemplate> nur einen enthalten, <xref:System.Windows.Controls.TextBlock> dessen- <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.HorizontalAlignment.Right> .  
  
 Im folgenden Beispiel werden der Stil und der erforderliche Stil definiert <xref:System.Windows.DataTemplate> , um die `ISBN` Spalte rechtsbündig zu machen, und die so ändern, dass <xref:System.Windows.Controls.GridViewColumn> auf das verwiesen wird <xref:System.Windows.DataTemplate> .  
  
 [!code-xaml[ListViewHowTos#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#3)]  
[!code-xaml[ListViewHowTos#4](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#4)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Übersicht über Datenvorlagen](../data/data-templating-overview.md)
- [Binden an XML-Daten mithilfe von XmlDataProvider-und XPath-Abfragen](../data/how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [Übersicht über ListView](listview-overview.md)
