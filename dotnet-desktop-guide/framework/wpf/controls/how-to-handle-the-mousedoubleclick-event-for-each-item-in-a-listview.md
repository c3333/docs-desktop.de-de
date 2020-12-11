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
# <a name="how-to-handle-the-mousedoubleclick-event-for-each-item-in-a-listview"></a><span data-ttu-id="f7b15-102">Gewusst wie: Behandeln des MouseDoubleClick-Ereignisses für die einzelnen ListView-Einträge</span><span class="sxs-lookup"><span data-stu-id="f7b15-102">How to: Handle the MouseDoubleClick Event for Each Item in a ListView</span></span>
<span data-ttu-id="f7b15-103">Um ein Ereignis für ein Element in einem zu behandeln <xref:System.Windows.Controls.ListView> , müssen Sie jedem einen Ereignishandler hinzufügen <xref:System.Windows.Controls.ListViewItem> .</span><span class="sxs-lookup"><span data-stu-id="f7b15-103">To handle an event for an item in a <xref:System.Windows.Controls.ListView>, you need to add an event handler to each <xref:System.Windows.Controls.ListViewItem>.</span></span> <span data-ttu-id="f7b15-104">Wenn ein <xref:System.Windows.Controls.ListView> an eine Datenquelle gebunden ist, erstellen Sie nicht explizit eine <xref:System.Windows.Controls.ListViewItem> , aber Sie können das-Ereignis für jedes Element behandeln, indem Sie ein einem <xref:System.Windows.EventSetter> Stil von hinzufügen <xref:System.Windows.Controls.ListViewItem> .</span><span class="sxs-lookup"><span data-stu-id="f7b15-104">When a <xref:System.Windows.Controls.ListView> is bound to a data source, you don't explicitly create a <xref:System.Windows.Controls.ListViewItem>, but you can handle the event for each item by adding an <xref:System.Windows.EventSetter> to a style of a <xref:System.Windows.Controls.ListViewItem>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7b15-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7b15-105">Example</span></span>  
 <span data-ttu-id="f7b15-106">Im folgenden Beispiel wird ein Daten gebundenes erstellt <xref:System.Windows.Controls.ListView> und ein erstellt <xref:System.Windows.Style> , um jedem einen Ereignishandler hinzuzufügen <xref:System.Windows.Controls.ListViewItem> .</span><span class="sxs-lookup"><span data-stu-id="f7b15-106">The following example creates a data-bound <xref:System.Windows.Controls.ListView> and creates a <xref:System.Windows.Style> to add an event handler to each <xref:System.Windows.Controls.ListViewItem>.</span></span>  
  
 [!code-xaml[ListViewHowTos#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#1)]  
[!code-xaml[ListViewHowTos#5](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#5)]  
[!code-xaml[ListViewHowTos#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="f7b15-107">Im folgenden Beispiel wird das- <xref:System.Windows.Controls.Control.MouseDoubleClick> Ereignis behandelt.</span><span class="sxs-lookup"><span data-stu-id="f7b15-107">The following example handles the <xref:System.Windows.Controls.Control.MouseDoubleClick> event.</span></span>  
  
 [!code-csharp[ListViewHowTos#6](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml.cs#6)]
 [!code-vb[ListViewHowTos#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewHowTos/VisualBasic/Window1.xaml.vb#6)]  
  
> [!NOTE]
> <span data-ttu-id="f7b15-108">Obwohl es am häufigsten ist, ein <xref:System.Windows.Controls.ListView> an eine Datenquelle zu binden, können Sie einen-Stil verwenden, um jedem in einer nicht Daten gebundenen einen Ereignishandler hinzuzufügen, <xref:System.Windows.Controls.ListViewItem> <xref:System.Windows.Controls.ListView> unabhängig davon, ob Sie explizit ein erstellen <xref:System.Windows.Controls.ListViewItem> .</span><span class="sxs-lookup"><span data-stu-id="f7b15-108">Although it is most common to bind a <xref:System.Windows.Controls.ListView> to a data source, you can use a style to add an event handler to each <xref:System.Windows.Controls.ListViewItem> in a non-data-bound <xref:System.Windows.Controls.ListView> regardless of whether you explicitly create a <xref:System.Windows.Controls.ListViewItem>.</span></span>  <span data-ttu-id="f7b15-109">Weitere Informationen zu explizit und implizit erstellten Steuer <xref:System.Windows.Controls.ListViewItem> Elementen finden Sie unter <xref:System.Windows.Controls.ItemsControl> .</span><span class="sxs-lookup"><span data-stu-id="f7b15-109">For more information about explicitly and implicitly created <xref:System.Windows.Controls.ListViewItem> controls, see <xref:System.Windows.Controls.ItemsControl>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7b15-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7b15-110">See also</span></span>

- <xref:System.Xml.XmlElement>
- [<span data-ttu-id="f7b15-111">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="f7b15-111">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="f7b15-112">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f7b15-112">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="f7b15-113">Binden an XML-Daten mithilfe von XmlDataProvider-und XPath-Abfragen</span><span class="sxs-lookup"><span data-stu-id="f7b15-113">Bind to XML Data Using an XMLDataProvider and XPath Queries</span></span>](../data/how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [<span data-ttu-id="f7b15-114">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="f7b15-114">ListView Overview</span></span>](listview-overview.md)
