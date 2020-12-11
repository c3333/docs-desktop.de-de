---
title: 'Gewusst wie: Behandeln des MouseDoubleClick-Ereignisses für die einzelnen ListView-Einträge'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView controls [WPF], MouseDoubleClick event
ms.assetid: 81b39369-655a-4585-ac58-4640e5bb8fed
ms.openlocfilehash: 58c17697c5053be267893834e8364c531c1db4de
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977778"
---
# <a name="how-to-handle-the-mousedoubleclick-event-for-each-item-in-a-listview"></a>Gewusst wie: Behandeln des MouseDoubleClick-Ereignisses für die einzelnen ListView-Einträge
Um ein Ereignis für ein Element in einem zu behandeln <xref:System.Windows.Controls.ListView> , müssen Sie jedem einen Ereignishandler hinzufügen <xref:System.Windows.Controls.ListViewItem> . Wenn ein <xref:System.Windows.Controls.ListView> an eine Datenquelle gebunden ist, erstellen Sie nicht explizit eine <xref:System.Windows.Controls.ListViewItem> , aber Sie können das-Ereignis für jedes Element behandeln, indem Sie ein einem <xref:System.Windows.EventSetter> Stil von hinzufügen <xref:System.Windows.Controls.ListViewItem> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Daten gebundenes erstellt <xref:System.Windows.Controls.ListView> und ein erstellt <xref:System.Windows.Style> , um jedem einen Ereignishandler hinzuzufügen <xref:System.Windows.Controls.ListViewItem> .  
  
 [!code-xaml[ListViewHowTos#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#1)]  
[!code-xaml[ListViewHowTos#5](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#5)]  
[!code-xaml[ListViewHowTos#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#2)]  
  
 Im folgenden Beispiel wird das- <xref:System.Windows.Controls.Control.MouseDoubleClick> Ereignis behandelt.  
  
 [!code-csharp[ListViewHowTos#6](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml.cs#6)]
 [!code-vb[ListViewHowTos#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewHowTos/VisualBasic/Window1.xaml.vb#6)]  
  
> [!NOTE]
> Obwohl es am häufigsten ist, ein <xref:System.Windows.Controls.ListView> an eine Datenquelle zu binden, können Sie einen-Stil verwenden, um jedem in einer nicht Daten gebundenen einen Ereignishandler hinzuzufügen, <xref:System.Windows.Controls.ListViewItem> <xref:System.Windows.Controls.ListView> unabhängig davon, ob Sie explizit ein erstellen <xref:System.Windows.Controls.ListViewItem> .  Weitere Informationen zu explizit und implizit erstellten Steuer <xref:System.Windows.Controls.ListViewItem> Elementen finden Sie unter <xref:System.Windows.Controls.ItemsControl> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Xml.XmlElement>
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [Binden an XML-Daten mithilfe von XmlDataProvider-und XPath-Abfragen](../data/how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [Übersicht über ListView](listview-overview.md)
