---
title: 'Gewusst wie: Formatieren eines ListView-Steuerelements mit einem GridView mithilfe von Vorlagen'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 94bf964b-96c8-4bdf-a0c3-f5271b7cb565
ms.openlocfilehash: 1caa652c4a2a3a7d0a8d40fe703df7a3e8038c9b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974659"
---
# <a name="how-to-use-templates-to-style-a-listview-that-uses-gridview"></a><span data-ttu-id="82b17-102">Gewusst wie: Formatieren eines ListView-Steuerelements mit einem GridView mithilfe von Vorlagen</span><span class="sxs-lookup"><span data-stu-id="82b17-102">How to: Use Templates to Style a ListView That Uses GridView</span></span>
<span data-ttu-id="82b17-103">Dieses Beispiel zeigt, wie das <xref:System.Windows.DataTemplate> -Objekt und das-Objekt verwendet werden, <xref:System.Windows.Style> um die Darstellung eines Steuer Elements anzugeben <xref:System.Windows.Controls.ListView> , das einen <xref:System.Windows.Controls.GridView> Ansichtsmodus verwendet.</span><span class="sxs-lookup"><span data-stu-id="82b17-103">This example shows how to use the <xref:System.Windows.DataTemplate> and <xref:System.Windows.Style> objects to specify the appearance of a <xref:System.Windows.Controls.ListView> control that uses a <xref:System.Windows.Controls.GridView> view mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="82b17-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="82b17-104">Example</span></span>  
 <span data-ttu-id="82b17-105">In den folgenden Beispielen werden <xref:System.Windows.Style> -Objekte und-Objekte gezeigt, die die Darstellung eines <xref:System.Windows.DataTemplate> Spalten Headers für einen anpassen <xref:System.Windows.Controls.GridViewColumn> .</span><span class="sxs-lookup"><span data-stu-id="82b17-105">The following examples show <xref:System.Windows.Style> and <xref:System.Windows.DataTemplate> objects that customize the appearance of a column header for a <xref:System.Windows.Controls.GridViewColumn>.</span></span>  
  
 [!code-xaml[ListViewTemplate#GridViewHeaderStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewheaderstyle)]  
  
 [!code-xaml[ListViewTemplate#GridViewHeaderTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewheadertemplate)]  
  
 <span data-ttu-id="82b17-106">Im folgenden Beispiel wird gezeigt, wie diese <xref:System.Windows.Style> -und- <xref:System.Windows.DataTemplate> Objekte zum Festlegen der <xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A> -Eigenschaft und der-Eigenschaft eines verwendet werden <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> <xref:System.Windows.Controls.GridViewColumn> .</span><span class="sxs-lookup"><span data-stu-id="82b17-106">The following example shows how to use these <xref:System.Windows.Style> and <xref:System.Windows.DataTemplate> objects to set the <xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A> and <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> properties of a <xref:System.Windows.Controls.GridViewColumn>.</span></span> <span data-ttu-id="82b17-107">Die- <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> Eigenschaft definiert den Inhalt der Spalten Zellen.</span><span class="sxs-lookup"><span data-stu-id="82b17-107">The <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> property defines the content of the column cells.</span></span>  
  
 [!code-xaml[ListViewTemplate#GridViewColumnTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewcolumntemplate)]  
  
 <span data-ttu-id="82b17-108"><xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A>Und <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> sind nur zwei verschiedene Eigenschaften, die Sie verwenden können, um die Darstellung der Spalten Kopfzeile für ein-Steuerelement anzupassen <xref:System.Windows.Controls.GridView> .</span><span class="sxs-lookup"><span data-stu-id="82b17-108">The <xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A> and <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> are only two of several properties that you can use to customize column header appearance for a <xref:System.Windows.Controls.GridView> control.</span></span> <span data-ttu-id="82b17-109">Weitere Informationen finden Sie unter [Übersicht über GridView-Spaltenheaderstile und -Spaltenheadervorlagen](gridview-column-header-styles-and-templates-overview.md).</span><span class="sxs-lookup"><span data-stu-id="82b17-109">For more information, see [GridView Column Header Styles and Templates Overview](gridview-column-header-styles-and-templates-overview.md).</span></span>  
  
 <span data-ttu-id="82b17-110">Im folgenden Beispiel wird gezeigt, wie ein definiert wird <xref:System.Windows.DataTemplate> , das die Darstellung der Zellen in einem anpasst <xref:System.Windows.Controls.GridViewColumn> .</span><span class="sxs-lookup"><span data-stu-id="82b17-110">The following example shows how to define a <xref:System.Windows.DataTemplate> that customizes the appearance of the cells in a <xref:System.Windows.Controls.GridViewColumn>.</span></span>  
  
 [!code-xaml[ListViewTemplate#GridViewCellTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewcelltemplate)]  
  
 <span data-ttu-id="82b17-111">Im folgenden Beispiel wird gezeigt, wie diese verwendet wird <xref:System.Windows.DataTemplate> , um den Inhalt einer Zelle zu definieren <xref:System.Windows.Controls.GridViewColumn> .</span><span class="sxs-lookup"><span data-stu-id="82b17-111">The following example shows how to use this <xref:System.Windows.DataTemplate> to define the content of a <xref:System.Windows.Controls.GridViewColumn> cell.</span></span> <span data-ttu-id="82b17-112">Diese Vorlage wird anstelle der Eigenschaft verwendet <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> , die im vorherigen Beispiel dargestellt wurde <xref:System.Windows.Controls.GridViewColumn> .</span><span class="sxs-lookup"><span data-stu-id="82b17-112">This template is used instead of the <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> property that is shown in the previous <xref:System.Windows.Controls.GridViewColumn> example.</span></span>  
  
 [!code-xaml[ListViewTemplate#CellTemplateProperty](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#celltemplateproperty)]  
  
## <a name="see-also"></a><span data-ttu-id="82b17-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82b17-113">See also</span></span>

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="82b17-114">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="82b17-114">GridView Overview</span></span>](gridview-overview.md)
- [<span data-ttu-id="82b17-115">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="82b17-115">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="82b17-116">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="82b17-116">ListView Overview</span></span>](listview-overview.md)
