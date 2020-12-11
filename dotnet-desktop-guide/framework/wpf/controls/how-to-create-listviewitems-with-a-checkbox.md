---
title: 'Gewusst wie: Erstellen von ListViewItems mit einem Kontrollkästchen'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], ListView
- controls [WPF], CheckBox
- ListView controls [WPF], CheckBox controls
- CheckBox control [WPF], ListView control
ms.assetid: f6d66c7f-906c-4f65-a55a-0ede9d00e26a
ms.openlocfilehash: b09d5ad11b0961febf524cec1e19cb1e59832e44
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977819"
---
# <a name="how-to-create-listviewitems-with-a-checkbox"></a><span data-ttu-id="b4228-102">Gewusst wie: Erstellen von ListViewItems mit einem Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="b4228-102">How to: Create ListViewItems with a CheckBox</span></span>
<span data-ttu-id="b4228-103">In diesem Beispiel wird gezeigt, wie eine Spalte von <xref:System.Windows.Controls.CheckBox> Steuerelementen in einem-Steuerelement angezeigt wird <xref:System.Windows.Controls.ListView> , das einen verwendet <xref:System.Windows.Controls.GridView> .</span><span class="sxs-lookup"><span data-stu-id="b4228-103">This example shows how to display a column of <xref:System.Windows.Controls.CheckBox> controls in a <xref:System.Windows.Controls.ListView> control that uses a <xref:System.Windows.Controls.GridView>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b4228-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4228-104">Example</span></span>  
 <span data-ttu-id="b4228-105">Um eine Spalte zu erstellen, die Steuer <xref:System.Windows.Controls.CheckBox> Elemente in einem enthält <xref:System.Windows.Controls.ListView> , erstellen Sie eine <xref:System.Windows.DataTemplate> , die eine enthält <xref:System.Windows.Controls.CheckBox> .</span><span class="sxs-lookup"><span data-stu-id="b4228-105">To create a column that contains <xref:System.Windows.Controls.CheckBox> controls in a <xref:System.Windows.Controls.ListView>, create a <xref:System.Windows.DataTemplate> that contains a <xref:System.Windows.Controls.CheckBox>.</span></span> <span data-ttu-id="b4228-106">Legen Sie dann die <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> eines <xref:System.Windows.Controls.GridViewColumn> auf die fest <xref:System.Windows.DataTemplate> .</span><span class="sxs-lookup"><span data-stu-id="b4228-106">Then set the <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> of a <xref:System.Windows.Controls.GridViewColumn> to the <xref:System.Windows.DataTemplate>.</span></span>  
  
 <span data-ttu-id="b4228-107">Das folgende Beispiel zeigt eine <xref:System.Windows.DataTemplate> , die eine enthält <xref:System.Windows.Controls.CheckBox> .</span><span class="sxs-lookup"><span data-stu-id="b4228-107">The following example shows a <xref:System.Windows.DataTemplate> that contains a <xref:System.Windows.Controls.CheckBox>.</span></span> <span data-ttu-id="b4228-108">Im Beispiel wird die- <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> Eigenschaft des- <xref:System.Windows.Controls.CheckBox> Objekts an den- <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> Eigenschafts Wert des-Objekts gebunden, das <xref:System.Windows.Controls.ListViewItem> es enthält.</span><span class="sxs-lookup"><span data-stu-id="b4228-108">The example binds the <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> property of the <xref:System.Windows.Controls.CheckBox> to the <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> property value of the <xref:System.Windows.Controls.ListViewItem> that contains it.</span></span> <span data-ttu-id="b4228-109">Wenn die, die <xref:System.Windows.Controls.ListViewItem> das enthält <xref:System.Windows.Controls.CheckBox> , ausgewählt ist, wird daher der <xref:System.Windows.Controls.CheckBox> aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b4228-109">Therefore, when the <xref:System.Windows.Controls.ListViewItem> that contains the <xref:System.Windows.Controls.CheckBox> is selected, the <xref:System.Windows.Controls.CheckBox> is checked.</span></span>  
  
 [!code-xaml[ListViewChkBox#CheckBoxDataTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#checkboxdatatemplate)]  
  
 <span data-ttu-id="b4228-110">Im folgenden Beispiel wird gezeigt, wie eine Spalte von-Steuerelementen erstellt wird <xref:System.Windows.Controls.CheckBox> .</span><span class="sxs-lookup"><span data-stu-id="b4228-110">The following example shows how to create a column of <xref:System.Windows.Controls.CheckBox> controls.</span></span> <span data-ttu-id="b4228-111">Um die Spalte zu erstellen, wird im Beispiel die- <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> Eigenschaft von auf festgelegt <xref:System.Windows.Controls.GridViewColumn> <xref:System.Windows.DataTemplate> .</span><span class="sxs-lookup"><span data-stu-id="b4228-111">To make the column, the example sets the <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> property of the <xref:System.Windows.Controls.GridViewColumn> to the <xref:System.Windows.DataTemplate>.</span></span>  
  
 [!code-xaml[ListViewChkBox#GridViewColumnCheckBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#gridviewcolumncheckbox)]  
  
## <a name="see-also"></a><span data-ttu-id="b4228-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4228-112">See also</span></span>

- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="b4228-113">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="b4228-113">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="b4228-114">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="b4228-114">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="b4228-115">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="b4228-115">GridView Overview</span></span>](gridview-overview.md)
