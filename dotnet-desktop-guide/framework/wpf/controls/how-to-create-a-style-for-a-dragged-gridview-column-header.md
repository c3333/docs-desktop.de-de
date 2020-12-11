---
title: 'Gewusst wie: Erstellen eines Stils für einen gezogenen GridView-Spaltenheader'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 0b999645-0313-4b33-80b9-19ece08b5459
ms.openlocfilehash: dbcdd38e0397b8e637aff962420a2959f33203df
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977655"
---
# <a name="how-to-create-a-style-for-a-dragged-gridview-column-header"></a><span data-ttu-id="82414-102">Gewusst wie: Erstellen eines Stils für einen gezogenen GridView-Spaltenheader</span><span class="sxs-lookup"><span data-stu-id="82414-102">How to: Create a Style for a Dragged GridView Column Header</span></span>
<span data-ttu-id="82414-103">In diesem Beispiel wird gezeigt, wie die Darstellung einer gezogenen geändert wird, <xref:System.Windows.Controls.GridViewColumnHeader> Wenn der Benutzer die Position einer Spalte ändert.</span><span class="sxs-lookup"><span data-stu-id="82414-103">This example shows how to change the appearance of a dragged <xref:System.Windows.Controls.GridViewColumnHeader> when the user changes the position of a column.</span></span>  
  
## <a name="example"></a><span data-ttu-id="82414-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="82414-104">Example</span></span>  
 <span data-ttu-id="82414-105">Wenn Sie einen Spaltenheader an eine andere Position in einer ziehen, die <xref:System.Windows.Controls.ListView> <xref:System.Windows.Controls.GridView> für den Ansichtsmodus verwendet, wird die Spalte an die neue Position verschoben.</span><span class="sxs-lookup"><span data-stu-id="82414-105">When you drag a column header to another location in a <xref:System.Windows.Controls.ListView> that uses <xref:System.Windows.Controls.GridView> for its view mode, the column moves to the new position.</span></span> <span data-ttu-id="82414-106">Beim Ziehen der Spaltenüberschrift wird zusätzlich zum ursprünglichen Header eine Gleit Komma Kopie der Kopfzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82414-106">While you are dragging the column header, a floating copy of the header appears in addition to the original header.</span></span> <span data-ttu-id="82414-107">Eine Spaltenüberschrift in einem <xref:System.Windows.Controls.GridView> wird durch ein- <xref:System.Windows.Controls.GridViewColumnHeader> Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82414-107">A column header in a <xref:System.Windows.Controls.GridView> is represented by a <xref:System.Windows.Controls.GridViewColumnHeader> object.</span></span>  
  
 <span data-ttu-id="82414-108">Um die Darstellung der Gleit Komma-und ursprünglichen Header anzupassen, können Sie festlegen, <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> um zu ändern <xref:System.Windows.Controls.GridViewColumnHeader> <xref:System.Windows.Style> .</span><span class="sxs-lookup"><span data-stu-id="82414-108">To customize the appearance of both the floating and original headers, you can set <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> to modify the <xref:System.Windows.Controls.GridViewColumnHeader> <xref:System.Windows.Style>.</span></span> <span data-ttu-id="82414-109">Diese <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> werden angewendet, wenn der <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> -Eigenschafts Wert `true` und der- <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> Eigenschafts Wert ist <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating> .</span><span class="sxs-lookup"><span data-stu-id="82414-109">These <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> are applied when the <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> property value is `true` and the <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> property value is <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.</span></span>  
  
 <span data-ttu-id="82414-110">Wenn der Benutzer die Maustaste drückt und die Maustaste gedrückt hält, während der Mauszeiger an der angehalten <xref:System.Windows.Controls.GridViewColumnHeader> wird, ändert sich der <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> Eigenschafts Wert in `true` .</span><span class="sxs-lookup"><span data-stu-id="82414-110">When the user presses the mouse button and holds it down while the mouse pauses on the <xref:System.Windows.Controls.GridViewColumnHeader>, the <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> property value changes to `true`.</span></span> <span data-ttu-id="82414-111">Wenn der Benutzer den Zieh Vorgang startet, ändert sich die- <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> Eigenschaft ebenso in <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating> .</span><span class="sxs-lookup"><span data-stu-id="82414-111">Likewise, when the user begins the drag operation, the <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> property changes to <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.</span></span>  
  
 <span data-ttu-id="82414-112">Im folgenden Beispiel wird gezeigt, wie festgelegt wird <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> , um die <xref:System.Windows.Controls.Control.Foreground%2A> <xref:System.Windows.Controls.Control.Background%2A> Farben und der ursprünglichen und gleitenden Header zu ändern, wenn der Benutzer eine Spalte an eine neue Position zieht.</span><span class="sxs-lookup"><span data-stu-id="82414-112">The following example shows how to set <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> to change the <xref:System.Windows.Controls.Control.Foreground%2A> and <xref:System.Windows.Controls.Control.Background%2A> colors of the original and floating headers when the user drags a column to a new position.</span></span>  
  
 [!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplatestart)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersstart)]  
[!code-xaml[ListViewHeaderRoleStyle#IsPressed](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#ispressed)]  
[!code-xaml[ListViewHeaderRoleStyle#Floating](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#floating)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersend)]  
[!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplateend)]  
  
## <a name="see-also"></a><span data-ttu-id="82414-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82414-113">See also</span></span>

- <xref:System.Windows.Controls.GridViewColumnHeader>
- <xref:System.Windows.Controls.GridViewColumnHeaderRole>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="82414-114">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="82414-114">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="82414-115">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="82414-115">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="82414-116">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="82414-116">GridView Overview</span></span>](gridview-overview.md)
