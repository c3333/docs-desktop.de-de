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
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-data"></a><span data-ttu-id="0d163-102">Gewusst wie: Verwenden des Master/Detail-Musters mit hierarchischen Daten</span><span class="sxs-lookup"><span data-stu-id="0d163-102">How to: Use the Master-Detail Pattern with Hierarchical Data</span></span>
<span data-ttu-id="0d163-103">Dieses Beispiel zeigt, wie das Master/Detail-Szenario implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="0d163-103">This example shows how to implement the master-detail scenario.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0d163-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d163-104">Example</span></span>  
 <span data-ttu-id="0d163-105">In diesem Beispiel `LeagueList` ist eine Auflistung von `Leagues` .</span><span class="sxs-lookup"><span data-stu-id="0d163-105">In this example, `LeagueList` is a collection of `Leagues`.</span></span> <span data-ttu-id="0d163-106">Jede `League` verfügt über eine `Name` -und eine-Auflistung von `Divisions` , und jede `Division` verfügt über einen Namen und eine Auflistung von `Teams` .</span><span class="sxs-lookup"><span data-stu-id="0d163-106">Each `League` has a `Name` and a collection of `Divisions`, and each `Division` has a name and a collection of `Teams`.</span></span> <span data-ttu-id="0d163-107">Jede `Team` verfügt über einen Teamnamen.</span><span class="sxs-lookup"><span data-stu-id="0d163-107">Each `Team` has a team name.</span></span>  
  
 [!code-xaml[MasterDetail#HowTo1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto1)]  
[!code-xaml[MasterDetail#HowTo2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto2)]  
  
 <span data-ttu-id="0d163-108">Im Folgenden finden Sie ein Bildschirmfoto des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="0d163-108">The following is a screenshot of the example.</span></span> <span data-ttu-id="0d163-109">Die `Divisions` <xref:System.Windows.Controls.ListBox> Auswahl in wird von automatisch nachverfolgt, `Leagues` <xref:System.Windows.Controls.ListBox> und die entsprechenden Daten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d163-109">The `Divisions` <xref:System.Windows.Controls.ListBox> automatically tracks selections in the `Leagues` <xref:System.Windows.Controls.ListBox> and display the corresponding data.</span></span> <span data-ttu-id="0d163-110">Der `Teams` <xref:System.Windows.Controls.ListBox> verfolgt die Auswahl in den anderen zwei-Steuer <xref:System.Windows.Controls.ListBox> Elementen.</span><span class="sxs-lookup"><span data-stu-id="0d163-110">The `Teams` <xref:System.Windows.Controls.ListBox> tracks selections in the other two <xref:System.Windows.Controls.ListBox> controls.</span></span>  
  
 ![Screenshot, der ein Beispiel für ein Master&#45;Detail Szenario zeigt.](./media/how-to-use-the-master-detail-pattern-with-hierarchical-data/databinding-master-detail-scenario.png)  
  
 <span data-ttu-id="0d163-112">In diesem Beispiel sind die folgenden zwei Punkte zu beachten:</span><span class="sxs-lookup"><span data-stu-id="0d163-112">The two things to notice in this example are:</span></span>  
  
1. <span data-ttu-id="0d163-113">Die drei Steuer <xref:System.Windows.Controls.ListBox> Elemente werden an dieselbe Quelle gebunden.</span><span class="sxs-lookup"><span data-stu-id="0d163-113">The three <xref:System.Windows.Controls.ListBox> controls bind to the same source.</span></span> <span data-ttu-id="0d163-114">Legen Sie die- <xref:System.Windows.Data.Binding.Path%2A> Eigenschaft der Bindung auf fest, um anzugeben, welche Datenebene <xref:System.Windows.Controls.ListBox> angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d163-114">You set the <xref:System.Windows.Data.Binding.Path%2A> property of the binding to specify which level of data you want the <xref:System.Windows.Controls.ListBox> to display.</span></span>  
  
2. <span data-ttu-id="0d163-115">Sie müssen die- <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> Eigenschaft für die Steuerelemente, deren Auswahl Sie nachverfolgen, auf festlegen `true` <xref:System.Windows.Controls.ListBox> .</span><span class="sxs-lookup"><span data-stu-id="0d163-115">You must set the <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> property to `true` on the <xref:System.Windows.Controls.ListBox> controls of which the selection you are tracking.</span></span> <span data-ttu-id="0d163-116">Durch Festlegen dieser Eigenschaft wird sichergestellt, dass das ausgewählte Element immer als festgelegt ist <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A> .</span><span class="sxs-lookup"><span data-stu-id="0d163-116">Setting this property ensures that the selected item is always set as the <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>.</span></span> <span data-ttu-id="0d163-117">Wenn die <xref:System.Windows.Controls.ListBox> Daten aus einem abruft, werden die <xref:System.Windows.Data.CollectionViewSource> Auswahl und die Währung Alternativ automatisch synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0d163-117">Alternatively, if the <xref:System.Windows.Controls.ListBox> gets it data from a <xref:System.Windows.Data.CollectionViewSource>, it synchronizes selection and currency automatically.</span></span>  
  
 <span data-ttu-id="0d163-118">Das Verfahren unterscheidet sich geringfügig bei der Verwendung von XML-Daten.</span><span class="sxs-lookup"><span data-stu-id="0d163-118">The technique is slightly different when you are using XML data.</span></span> <span data-ttu-id="0d163-119">Ein Beispiel finden Sie unter [Verwenden des Master-Detail Musters mit hierarchischen XML-Daten](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md).</span><span class="sxs-lookup"><span data-stu-id="0d163-119">For an example, see [Use the Master-Detail Pattern with Hierarchical XML Data](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d163-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d163-120">See also</span></span>

- <xref:System.Windows.HierarchicalDataTemplate>
- [<span data-ttu-id="0d163-121">Binden an eine Sammlung und Anzeigen von Informationen auf Grundlage der Auswahl</span><span class="sxs-lookup"><span data-stu-id="0d163-121">Bind to a Collection and Display Information Based on Selection</span></span>](how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [<span data-ttu-id="0d163-122">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="0d163-122">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="0d163-123">Übersicht über Datenvorlagen</span><span class="sxs-lookup"><span data-stu-id="0d163-123">Data Templating Overview</span></span>](data-templating-overview.md)
- [<span data-ttu-id="0d163-124">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="0d163-124">How-to Topics</span></span>](data-binding-how-to-topics.md)
