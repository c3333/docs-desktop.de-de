---
title: 'Gewusst wie: Erstellen von unterschiedlichen Kachelmustern mit einem TileBrush'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TileBrush [WPF], creating tile patterns
- tile patterns [WPF], creating
- creating [WPF], tile patterns with TileBrush
ms.assetid: 5aa46632-3527-4668-9d8d-0375c8af28aa
ms.openlocfilehash: c1051b234961eee9ae740af2abac3d64c523656c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976933"
---
# <a name="how-to-create-different-tile-patterns-with-a-tilebrush"></a><span data-ttu-id="0cc69-102">Gewusst wie: Erstellen von unterschiedlichen Kachelmustern mit einem TileBrush</span><span class="sxs-lookup"><span data-stu-id="0cc69-102">How to: Create Different Tile Patterns with a TileBrush</span></span>
<span data-ttu-id="0cc69-103">In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft eines verwendet wird <xref:System.Windows.Media.TileBrush> , um ein Muster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0cc69-103">This example shows how to use the <xref:System.Windows.Media.TileBrush.TileMode%2A> property of a <xref:System.Windows.Media.TileBrush> to create a pattern.</span></span>  
  
 <span data-ttu-id="0cc69-104">Mithilfe der- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft können Sie angeben, wie der Inhalt einer <xref:System.Windows.Media.TileBrush> wiederholt wird, d. h., Sie können einen Ausgabebereich ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="0cc69-104">The <xref:System.Windows.Media.TileBrush.TileMode%2A> property enables you to specify how the content of a <xref:System.Windows.Media.TileBrush> is repeated, that is, tiled to fill an output area.</span></span> <span data-ttu-id="0cc69-105">Zum Erstellen eines Musters legen Sie den <xref:System.Windows.Media.TileBrush.TileMode%2A> auf <xref:System.Windows.Media.TileMode.Tile> , <xref:System.Windows.Media.TileMode.FlipX> , oder fest <xref:System.Windows.Media.TileMode.FlipY> <xref:System.Windows.Media.TileMode.FlipXY> .</span><span class="sxs-lookup"><span data-stu-id="0cc69-105">To create a pattern, you set the <xref:System.Windows.Media.TileBrush.TileMode%2A> to <xref:System.Windows.Media.TileMode.Tile>, <xref:System.Windows.Media.TileMode.FlipX>, <xref:System.Windows.Media.TileMode.FlipY>, or <xref:System.Windows.Media.TileMode.FlipXY>.</span></span> <span data-ttu-id="0cc69-106">Sie müssen auch die <xref:System.Windows.Media.TileBrush.Viewport%2A> der- <xref:System.Windows.Media.TileBrush> Klasse so festlegen, dass Sie kleiner ist als der Bereich, den Sie zeichnen. andernfalls wird nur eine einzelne Kachel erstellt, unabhängig von der Einstellung, die <xref:System.Windows.Media.TileBrush.TileMode%2A> Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="0cc69-106">You must also set the <xref:System.Windows.Media.TileBrush.Viewport%2A> of the <xref:System.Windows.Media.TileBrush> so that it is smaller than the area that you are painting; otherwise, only a single tile is produced, regardless which <xref:System.Windows.Media.TileBrush.TileMode%2A> setting you use.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0cc69-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0cc69-107">Example</span></span>  
 <span data-ttu-id="0cc69-108">Im folgenden Beispiel werden fünf- <xref:System.Windows.Media.DrawingBrush> Objekte erstellt, die jeweils eine andere <xref:System.Windows.Media.TileBrush.TileMode%2A> Einstellung erhält und zum Zeichnen von fünf Rechtecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cc69-108">The following example creates five <xref:System.Windows.Media.DrawingBrush> objects, gives them each a different <xref:System.Windows.Media.TileBrush.TileMode%2A> setting, and uses them to paint five rectangles.</span></span> <span data-ttu-id="0cc69-109">Obwohl in diesem Beispiel die- <xref:System.Windows.Media.DrawingBrush> Klasse verwendet <xref:System.Windows.Media.TileBrush.TileMode%2A> wird, um das Verhalten zu veranschaulichen, funktioniert die- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft identisch für alle- <xref:System.Windows.Media.TileBrush> Objekte, d. h <xref:System.Windows.Media.ImageBrush> . für, <xref:System.Windows.Media.VisualBrush> und <xref:System.Windows.Media.DrawingBrush> .</span><span class="sxs-lookup"><span data-stu-id="0cc69-109">Although this example uses the <xref:System.Windows.Media.DrawingBrush> class to demonstrate <xref:System.Windows.Media.TileBrush.TileMode%2A> behavior, the <xref:System.Windows.Media.TileBrush.TileMode%2A> property works identically for all the <xref:System.Windows.Media.TileBrush> objects, that is, for <xref:System.Windows.Media.ImageBrush>, <xref:System.Windows.Media.VisualBrush>, and <xref:System.Windows.Media.DrawingBrush>.</span></span>  
  
 <span data-ttu-id="0cc69-110">In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0cc69-110">The following illustration shows the output that this example produces.</span></span>  
  
 <span data-ttu-id="0cc69-111">![TileBrush-Kachelbeispiel-Ausgabe](./media/graphicsmm-drawingbrushtilemodeexample.png "graphicsmm_DrawingBrushTileModeExample")</span><span class="sxs-lookup"><span data-stu-id="0cc69-111">![TileBrush tiling example output](./media/graphicsmm-drawingbrushtilemodeexample.png "graphicsmm_DrawingBrushTileModeExample")</span></span>  
<span data-ttu-id="0cc69-112">Mit der TileMode-Eigenschaft erstellte Kachel Muster</span><span class="sxs-lookup"><span data-stu-id="0cc69-112">Tile patterns created with the TileMode property</span></span>  
  
 [!code-csharp[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/TileModeExample.cs#graphicsmmdrawingbrushtilemodeexample)]
 [!code-vb[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/tilemodeexample.vb#graphicsmmdrawingbrushtilemodeexample)]
 [!code-xaml[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/TileModeExample.xaml#graphicsmmdrawingbrushtilemodeexample)]  
  
## <a name="see-also"></a><span data-ttu-id="0cc69-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cc69-113">See also</span></span>

- [<span data-ttu-id="0cc69-114">Festlegen der Kachelgröße für einen TileBrush</span><span class="sxs-lookup"><span data-stu-id="0cc69-114">Set the Tile Size for a TileBrush</span></span>](how-to-set-the-tile-size-for-a-tilebrush.md)
- [<span data-ttu-id="0cc69-115">Zeichnen mit Bildern, Zeichnungen und visuellen Elementen</span><span class="sxs-lookup"><span data-stu-id="0cc69-115">Painting with Images, Drawings, and Visuals</span></span>](painting-with-images-drawings-and-visuals.md)
