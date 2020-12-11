---
title: 'Gewusst wie: Erstellen einer zusammengesetzten Zeichnung'
ms.date: 03/30/2017
helpviewer_keywords:
- drawings [WPF], composite
- composite drawings [WPF]
- graphics [WPF], composite drawings
ms.assetid: 066eb0ab-5f0e-439d-85c6-dca60af269fc
ms.openlocfilehash: 0af7fbca593627ebe8cd102a02617a27eac50aa5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978224"
---
# <a name="how-to-create-a-composite-drawing"></a><span data-ttu-id="02b6e-102">Gewusst wie: Erstellen einer zusammengesetzten Zeichnung</span><span class="sxs-lookup"><span data-stu-id="02b6e-102">How to: Create a Composite Drawing</span></span>
<span data-ttu-id="02b6e-103">Dieses Beispiel zeigt, wie Sie mithilfe <xref:System.Windows.Media.DrawingGroup> von komplexe Zeichnungen erstellen, indem Sie mehrere <xref:System.Windows.Media.Drawing> Objekte zu einer einzelnen zusammengesetzten Zeichnung kombinieren.</span><span class="sxs-lookup"><span data-stu-id="02b6e-103">This example shows how to use a <xref:System.Windows.Media.DrawingGroup> to create complex drawings by combining multiple <xref:System.Windows.Media.Drawing> objects into a single composite drawing.</span></span>  
  
## <a name="example"></a><span data-ttu-id="02b6e-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02b6e-104">Example</span></span>  
 <span data-ttu-id="02b6e-105">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.DrawingGroup> , um eine zusammengesetzte Zeichnung aus den <xref:System.Windows.Media.GeometryDrawing> -und-Objekten zu erstellen <xref:System.Windows.Media.ImageDrawing> .</span><span class="sxs-lookup"><span data-stu-id="02b6e-105">The following example uses a <xref:System.Windows.Media.DrawingGroup> to create a composite drawing from the <xref:System.Windows.Media.GeometryDrawing> and <xref:System.Windows.Media.ImageDrawing> objects.</span></span> <span data-ttu-id="02b6e-106">In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="02b6e-106">The following illustration shows the output that this example produces.</span></span>  
  
 <span data-ttu-id="02b6e-107">![Eine DrawingGroup mit mehreren Zeichnungen](./media/graphicsmm-simple.jpg "graphicsmm_simple")</span><span class="sxs-lookup"><span data-stu-id="02b6e-107">![A DrawingGroup with multiple drawings](./media/graphicsmm-simple.jpg "graphicsmm_simple")</span></span>  
<span data-ttu-id="02b6e-108">Eine zusammengesetzte Zeichnung, die mit DrawingGroup erstellt wird</span><span class="sxs-lookup"><span data-stu-id="02b6e-108">A composite drawing that is created by using DrawingGroup</span></span>  
  
 <span data-ttu-id="02b6e-109">Beachten Sie den grauen Rahmen, in dem die Begrenzungen der Zeichnung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="02b6e-109">Note the gray border, which shows the bounds of the drawing.</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMSimpleDrawingGroupExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupExample.cs#graphicsmmsimpledrawinggroupexample)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMSimpleDrawingGroupExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupExample.xaml#graphicsmmsimpledrawinggroupexample)]  
  
 <span data-ttu-id="02b6e-110">Sie können eine verwenden, um eine, die-,-,- <xref:System.Windows.Media.DrawingGroup> <xref:System.Windows.Media.DrawingGroup.Transform%2A> oder- <xref:System.Windows.Media.DrawingGroup.Opacity%2A> Einstellung <xref:System.Windows.Media.DrawingGroup.OpacityMask%2A> <xref:System.Windows.Media.DrawingGroup.BitmapEffect%2A> <xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A> <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> auf die darin enthaltenen Zeichnungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="02b6e-110">You can use a <xref:System.Windows.Media.DrawingGroup> to apply a <xref:System.Windows.Media.DrawingGroup.Transform%2A>, <xref:System.Windows.Media.DrawingGroup.Opacity%2A> setting, <xref:System.Windows.Media.DrawingGroup.OpacityMask%2A>, <xref:System.Windows.Media.DrawingGroup.BitmapEffect%2A>, <xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A>, or <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> to the drawings it contains.</span></span> <span data-ttu-id="02b6e-111">Da ein <xref:System.Windows.Media.DrawingGroup> auch ein ist <xref:System.Windows.Media.Drawing> , kann es andere- <xref:System.Windows.Media.DrawingGroup> Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="02b6e-111">Because a <xref:System.Windows.Media.DrawingGroup> is also a <xref:System.Windows.Media.Drawing>, it can contain other <xref:System.Windows.Media.DrawingGroup> objects.</span></span>  
  
 <span data-ttu-id="02b6e-112">Das folgende Beispiel ähnelt dem vorherigen Beispiel, mit dem Unterschied, dass es zusätzliche <xref:System.Windows.Media.DrawingGroup> -Objekte verwendet, um Bitmapeffekte und eine Deck Kraft Maske auf einige ihrer Zeichnungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="02b6e-112">The following example is similar to the preceding example, except that it uses additional <xref:System.Windows.Media.DrawingGroup> objects to apply bitmap effects and an opacity mask to some of its drawings.</span></span> <span data-ttu-id="02b6e-113">In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="02b6e-113">The following illustration shows the output that this example produces.</span></span>  
  
 <span data-ttu-id="02b6e-114">![Eine DrawingGroup mit mehreren Zeichnungen](./media/graphicsmm-multiple.jpg "graphicsmm_multiple")</span><span class="sxs-lookup"><span data-stu-id="02b6e-114">![A DrawingGroup with multiple drawings](./media/graphicsmm-multiple.jpg "graphicsmm_multiple")</span></span>  
<span data-ttu-id="02b6e-115">Zusammengesetzte Zeichnung mit mehreren DrawingGroup-Objekten</span><span class="sxs-lookup"><span data-stu-id="02b6e-115">Composite drawing that has multiple DrawingGroup objects</span></span>  
  
 <span data-ttu-id="02b6e-116">Beachten Sie den grauen Rahmen, in dem die Begrenzungen der Zeichnung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="02b6e-116">Note the gray border, which shows the bounds of the drawing.</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMMultipleDrawingGroupsExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupExample.cs#graphicsmmmultipledrawinggroupsexample)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMMultipleDrawingGroupsExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupExample.xaml#graphicsmmmultipledrawinggroupsexample)]  
  
 <span data-ttu-id="02b6e-117">Weitere Informationen zu <xref:System.Windows.Media.Drawing> Objekten finden Sie unter [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="02b6e-117">For more information about <xref:System.Windows.Media.Drawing> objects, see [Drawing Objects Overview](drawing-objects-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02b6e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02b6e-118">See also</span></span>

- <xref:System.Windows.Media.DrawingGroup.BitmapEffect%2A>
- <xref:System.Windows.Media.DrawingGroup.Transform%2A>
- <xref:System.Windows.Media.DrawingGroup.OpacityMask%2A>
- <xref:System.Windows.Media.DrawingGroup.Opacity%2A>
- <xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A>
- <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A>
- [<span data-ttu-id="02b6e-119">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="02b6e-119">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
