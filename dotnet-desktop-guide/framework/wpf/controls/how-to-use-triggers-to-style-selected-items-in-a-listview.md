---
title: 'Gewusst wie: Verwenden von Triggern zum Formatieren ausgewählter Elemente in einem ListView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 1e2bdce0-afe8-4507-9b18-f33de43de25a
ms.openlocfilehash: ad64382b871bae9114a1e63257de3f8595376923
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977084"
---
# <a name="how-to-use-triggers-to-style-selected-items-in-a-listview"></a><span data-ttu-id="6e381-102">Gewusst wie: Verwenden von Triggern zum Formatieren ausgewählter Elemente in einem ListView</span><span class="sxs-lookup"><span data-stu-id="6e381-102">How to: Use Triggers to Style Selected Items in a ListView</span></span>
<span data-ttu-id="6e381-103">In diesem Beispiel wird gezeigt, wie <xref:System.Windows.Style.Triggers%2A> für ein Steuerelement definiert <xref:System.Windows.Controls.ListViewItem> wird, sodass bei einer Änderung des Eigenschafts Werts eine der <xref:System.Windows.Controls.ListViewItem> <xref:System.Windows.Style> <xref:System.Windows.Controls.ListViewItem> Änderungen in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6e381-103">This example shows how to define <xref:System.Windows.Style.Triggers%2A> for a <xref:System.Windows.Controls.ListViewItem> control so that when a property value of a <xref:System.Windows.Controls.ListViewItem> changes, the <xref:System.Windows.Style> of the <xref:System.Windows.Controls.ListViewItem> changes in response.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6e381-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e381-104">Example</span></span>  
 <span data-ttu-id="6e381-105">Wenn Sie möchten <xref:System.Windows.Style> , dass sich die eines <xref:System.Windows.Controls.ListViewItem> in Reaktion auf Eigenschafts Änderungen ändert, definieren Sie <xref:System.Windows.Style.Triggers%2A> für die <xref:System.Windows.Style> Änderung.</span><span class="sxs-lookup"><span data-stu-id="6e381-105">If you want the <xref:System.Windows.Style> of a <xref:System.Windows.Controls.ListViewItem> to change in response to property changes, define <xref:System.Windows.Style.Triggers%2A> for the <xref:System.Windows.Style> change.</span></span>  
  
 <span data-ttu-id="6e381-106">Im folgenden Beispiel wird ein definiert <xref:System.Windows.Trigger> , mit dem die <xref:System.Windows.Controls.Control.Foreground%2A> -Eigenschaft auf festgelegt wird <xref:System.Windows.Media.Brushes.Blue%2A> und der geändert wird <xref:System.Windows.FrameworkElement.Cursor%2A> , <xref:System.Windows.Input.CursorType.Hand> Wenn die- <xref:System.Windows.UIElement.IsMouseOver%2A> Eigenschaft in geändert wird `true` .</span><span class="sxs-lookup"><span data-stu-id="6e381-106">The following example defines a <xref:System.Windows.Trigger> that sets the <xref:System.Windows.Controls.Control.Foreground%2A> property to <xref:System.Windows.Media.Brushes.Blue%2A> and changes the <xref:System.Windows.FrameworkElement.Cursor%2A> to display a <xref:System.Windows.Input.CursorType.Hand> when the <xref:System.Windows.UIElement.IsMouseOver%2A> property changes to `true`.</span></span>  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#Trigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#trigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
 <span data-ttu-id="6e381-107">Im folgenden Beispiel wird ein definiert <xref:System.Windows.MultiTrigger> , mit dem die <xref:System.Windows.Controls.Control.Foreground%2A> -Eigenschaft eines auf festgelegt <xref:System.Windows.Controls.ListViewItem> wird, <xref:System.Windows.Media.Brushes.Yellow%2A> Wenn das <xref:System.Windows.Controls.ListViewItem> das ausgewählte Element ist und über den Tastaturfokus verfügt.</span><span class="sxs-lookup"><span data-stu-id="6e381-107">The following example defines a <xref:System.Windows.MultiTrigger> that sets the <xref:System.Windows.Controls.Control.Foreground%2A> property of a <xref:System.Windows.Controls.ListViewItem> to <xref:System.Windows.Media.Brushes.Yellow%2A> when the <xref:System.Windows.Controls.ListViewItem> is the selected item and has keyboard focus.</span></span>  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#MultiTrigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#multitrigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
## <a name="see-also"></a><span data-ttu-id="6e381-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e381-108">See also</span></span>

- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="6e381-109">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="6e381-109">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="6e381-110">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="6e381-110">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="6e381-111">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="6e381-111">GridView Overview</span></span>](gridview-overview.md)
