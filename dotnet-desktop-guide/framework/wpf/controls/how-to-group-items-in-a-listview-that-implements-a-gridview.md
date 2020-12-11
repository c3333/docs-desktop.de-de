---
title: 'Gewusst wie: Gruppieren von Elementen in einem ListView, in dem ein GridView implementiert ist'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], grouping items with GridViews
- grouping items in ListViews implementing GridViews [WPF]
- GridView controls [WPF], grouping items
ms.assetid: eebef25b-ddc6-424e-a66d-ea228d1bf33d
ms.openlocfilehash: b3dd6891976a942b299c87fca25e430e9ee59a51
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975499"
---
# <a name="how-to-group-items-in-a-listview-that-implements-a-gridview"></a><span data-ttu-id="8ef47-102">Gewusst wie: Gruppieren von Elementen in einem ListView, in dem ein GridView implementiert ist</span><span class="sxs-lookup"><span data-stu-id="8ef47-102">How to: Group Items in a ListView That Implements a GridView</span></span>
<span data-ttu-id="8ef47-103">In diesem Beispiel wird gezeigt, wie Gruppen von Elementen im <xref:System.Windows.Controls.GridView> Ansichtsmodus eines-Steuer Elements angezeigt werden <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="8ef47-103">This example shows how to display groups of items in the <xref:System.Windows.Controls.GridView> view mode of a <xref:System.Windows.Controls.ListView> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8ef47-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ef47-104">Example</span></span>  
 <span data-ttu-id="8ef47-105">Um Gruppen von Elementen in einer anzuzeigen <xref:System.Windows.Controls.ListView> , definieren Sie eine <xref:System.Windows.Data.CollectionViewSource> .</span><span class="sxs-lookup"><span data-stu-id="8ef47-105">To display groups of items in a <xref:System.Windows.Controls.ListView>, define a <xref:System.Windows.Data.CollectionViewSource>.</span></span> <span data-ttu-id="8ef47-106">Das folgende Beispiel zeigt <xref:System.Windows.Data.CollectionViewSource> , wie Datenelemente gemäß dem Wert des `Catalog` Datenfelds gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="8ef47-106">The following example shows a <xref:System.Windows.Data.CollectionViewSource> that groups data items according to the value of the `Catalog` data field.</span></span>  
  
 [!code-xaml[GridViewWithGroups#GroupingCollectionViewSource](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#groupingcollectionviewsource)]  
  
 <span data-ttu-id="8ef47-107">Im folgenden Beispiel wird der <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> für den <xref:System.Windows.Controls.ListView> auf den festgelegt <xref:System.Windows.Data.CollectionViewSource> , der im vorherigen Beispiel definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8ef47-107">The following example sets the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> for the <xref:System.Windows.Controls.ListView> to the <xref:System.Windows.Data.CollectionViewSource> that the previous example defines.</span></span> <span data-ttu-id="8ef47-108">Im Beispiel wird auch ein definiert <xref:System.Windows.Controls.ItemsControl.GroupStyle%2A> , das ein-Steuerelement implementiert <xref:System.Windows.Controls.Expander> .</span><span class="sxs-lookup"><span data-stu-id="8ef47-108">The example also defines a <xref:System.Windows.Controls.ItemsControl.GroupStyle%2A> that implements an <xref:System.Windows.Controls.Expander> control.</span></span>  
  
 [!code-xaml[GridViewWithGroups#ListViewGroups](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewgroups)]  
[!code-xaml[GridViewWithGroups#ListViewEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewend)]  
  
## <a name="see-also"></a><span data-ttu-id="8ef47-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ef47-109">See also</span></span>

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="8ef47-110">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="8ef47-110">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="8ef47-111">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="8ef47-111">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="8ef47-112">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="8ef47-112">GridView Overview</span></span>](gridview-overview.md)
