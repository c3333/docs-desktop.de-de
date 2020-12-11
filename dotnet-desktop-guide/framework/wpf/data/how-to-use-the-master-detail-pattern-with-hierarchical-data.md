---
title: 'Gewusst wie: Verwenden des Master/Detail-Musters mit hierarchischen Daten'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], Master-Detail data paradigm
- Master-Detail data paradigm
ms.assetid: 11429b9e-058d-4084-bfb6-2cf209c8ddf7
ms.openlocfilehash: dd3ecff2593c88505a1d301f14fe3456e8e4dc85
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976548"
---
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-data"></a>Gewusst wie: Verwenden des Master/Detail-Musters mit hierarchischen Daten
Dieses Beispiel zeigt, wie das Master/Detail-Szenario implementiert wird.  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel `LeagueList` ist eine Auflistung von `Leagues` . Jede `League` verfügt über eine `Name` -und eine-Auflistung von `Divisions` , und jede `Division` verfügt über einen Namen und eine Auflistung von `Teams` . Jede `Team` verfügt über einen Teamnamen.  
  
 [!code-xaml[MasterDetail#HowTo1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto1)]  
[!code-xaml[MasterDetail#HowTo2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto2)]  
  
 Im Folgenden finden Sie ein Bildschirmfoto des Beispiels. Die `Divisions` <xref:System.Windows.Controls.ListBox> Auswahl in wird von automatisch nachverfolgt, `Leagues` <xref:System.Windows.Controls.ListBox> und die entsprechenden Daten werden angezeigt. Der `Teams` <xref:System.Windows.Controls.ListBox> verfolgt die Auswahl in den anderen zwei-Steuer <xref:System.Windows.Controls.ListBox> Elementen.  
  
 ![Screenshot, der ein Beispiel für ein Master&#45;Detail Szenario zeigt.](./media/how-to-use-the-master-detail-pattern-with-hierarchical-data/databinding-master-detail-scenario.png)  
  
 In diesem Beispiel sind die folgenden zwei Punkte zu beachten:  
  
1. Die drei Steuer <xref:System.Windows.Controls.ListBox> Elemente werden an dieselbe Quelle gebunden. Legen Sie die- <xref:System.Windows.Data.Binding.Path%2A> Eigenschaft der Bindung auf fest, um anzugeben, welche Datenebene <xref:System.Windows.Controls.ListBox> angezeigt werden soll.  
  
2. Sie müssen die- <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> Eigenschaft für die Steuerelemente, deren Auswahl Sie nachverfolgen, auf festlegen `true` <xref:System.Windows.Controls.ListBox> . Durch Festlegen dieser Eigenschaft wird sichergestellt, dass das ausgewählte Element immer als festgelegt ist <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A> . Wenn die <xref:System.Windows.Controls.ListBox> Daten aus einem abruft, werden die <xref:System.Windows.Data.CollectionViewSource> Auswahl und die Währung Alternativ automatisch synchronisiert.  
  
 Das Verfahren unterscheidet sich geringfügig bei der Verwendung von XML-Daten. Ein Beispiel finden Sie unter [Verwenden des Master-Detail Musters mit hierarchischen XML-Daten](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.HierarchicalDataTemplate>
- [Binden an eine Sammlung und Anzeigen von Informationen auf Grundlage der Auswahl](how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Übersicht über Datenvorlagen](data-templating-overview.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
