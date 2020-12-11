---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einer Zeichnung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], painting with drawings
- painting [WPF], with drawings
- drawings [WPF], painting with
ms.assetid: c10dc4b1-09b1-41e8-ad14-456b5fb377df
ms.openlocfilehash: 6b204ae631912181333e2559ebadcdc37e7693b7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978185"
---
# <a name="how-to-paint-an-area-with-a-drawing"></a><span data-ttu-id="0213a-102">Gewusst wie: Zeichnen eines Bereichs mit einer Zeichnung</span><span class="sxs-lookup"><span data-stu-id="0213a-102">How to: Paint an Area with a Drawing</span></span>
<span data-ttu-id="0213a-103">Dieses Beispiel zeigt, wie Sie einen Bereich mit einer Zeichnung zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0213a-103">This example shows how to paint an area with a drawing.</span></span> <span data-ttu-id="0213a-104">Um einen Bereich mit einer Zeichnung zu zeichnen, verwenden Sie ein <xref:System.Windows.Media.DrawingBrush> -Objekt und ein-Objekt oder mehrere- <xref:System.Windows.Media.Drawing> Objekte.</span><span class="sxs-lookup"><span data-stu-id="0213a-104">To paint an area with a drawing, you use a <xref:System.Windows.Media.DrawingBrush> and one or more <xref:System.Windows.Media.Drawing> objects.</span></span>   <span data-ttu-id="0213a-105">Im folgenden Beispiel wird ein- <xref:System.Windows.Media.DrawingBrush> Objekt verwendet, um ein-Objekt mit einer Zeichnung zweier Ellipsen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0213a-105">The following example uses a <xref:System.Windows.Media.DrawingBrush> to paint an object with a drawing of two ellipses.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0213a-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0213a-106">Example</span></span>  
 [!code-xaml[drawingbrush_snip#DrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_snip/CS/DrawingBrushExample.xaml#drawingbrushexamplewholepage)]  
  
 [!code-csharp[drawingbrush_procedural_snip#DrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_procedural_snip/CSharp/DrawingBrushExample.cs#drawingbrushexamplewholepage)]
 [!code-vb[drawingbrush_procedural_snip#DrawingBrushExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/drawingbrush_procedural_snip/VisualBasic/DrawingBrushExample.vb#drawingbrushexamplewholepage)]  
  
 <span data-ttu-id="0213a-107">Die folgende Abbildung zeigt die Ausgabe des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="0213a-107">The following illustration shows the example's output.</span></span>  
  
 <span data-ttu-id="0213a-108">![Ausgabe von einem DrawingBrush](./media/graphicsmm-drawingbrush-simple.png "graphicsmm_drawingbrush_simple")</span><span class="sxs-lookup"><span data-stu-id="0213a-108">![Output from a DrawingBrush](./media/graphicsmm-drawingbrush-simple.png "graphicsmm_drawingbrush_simple")</span></span>  
  
 <span data-ttu-id="0213a-109">(Der Mittelpunkt der Form ist weiß aus     [den Untersteuern der Füllung einer zusammengesetzten Form](how-to-control-the-fill-of-a-composite-shape.md)beschriebenen Gründen.)</span><span class="sxs-lookup"><span data-stu-id="0213a-109">(The center of the shape is white for reasons described in     [Control the Fill of a Composite Shape](how-to-control-the-fill-of-a-composite-shape.md).)</span></span>  
  
 <span data-ttu-id="0213a-110">Durch Festlegen <xref:System.Windows.Media.DrawingBrush> der Eigenschaften und des-Objekts <xref:System.Windows.Media.TileBrush.Viewport%2A> <xref:System.Windows.Media.TileBrush.TileMode%2A> können Sie ein sich wiederholendes Muster erstellen.</span><span class="sxs-lookup"><span data-stu-id="0213a-110">By setting a <xref:System.Windows.Media.DrawingBrush> object's <xref:System.Windows.Media.TileBrush.Viewport%2A> and <xref:System.Windows.Media.TileBrush.TileMode%2A> properties, you can create a repeating pattern.</span></span> <span data-ttu-id="0213a-111">Im folgenden Beispiel wird ein Objekt mit einem aus einer Zeichnung von zwei Ellipsen erstellten Muster gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0213a-111">The following example paints an object with a pattern created from a drawing of two ellipses.</span></span>  
  
 [!code-xaml[drawingbrush_snip#TiledDrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_snip/CS/TiledDrawingBrushExample.xaml#tileddrawingbrushexamplewholepage)]  
  
 [!code-csharp[drawingbrush_procedural_snip#TiledDrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_procedural_snip/CSharp/TiledDrawingBrushExample.cs#tileddrawingbrushexamplewholepage)]
 [!code-vb[drawingbrush_procedural_snip#TiledDrawingBrushExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/drawingbrush_procedural_snip/VisualBasic/TiledDrawingBrushExample.vb#tileddrawingbrushexamplewholepage)]  
  
 <span data-ttu-id="0213a-112">Die folgende Abbildung zeigt die Kachel <xref:System.Windows.Media.DrawingBrush> Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0213a-112">The following illustration shows the tiled <xref:System.Windows.Media.DrawingBrush> output.</span></span>  
  
 <span data-ttu-id="0213a-113">![Gekachelte Ausgabe von einem DrawingBrush](./media/graphicsmm-drawingbrush-tiled.png "graphicsmm_drawingbrush_tiled")</span><span class="sxs-lookup"><span data-stu-id="0213a-113">![Tiled output from a DrawingBrush](./media/graphicsmm-drawingbrush-tiled.png "graphicsmm_drawingbrush_tiled")</span></span>  
  
 <span data-ttu-id="0213a-114">Weitere Informationen zum Zeichnen von Pinsel finden Sie unterzeichnen [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen.</span><span class="sxs-lookup"><span data-stu-id="0213a-114">For more information about drawing brushes, see [Painting with Images, Drawings, and Visuals](painting-with-images-drawings-and-visuals.md).</span></span> <span data-ttu-id="0213a-115">Weitere Informationen zu <xref:System.Windows.Media.Drawing> Objekten finden Sie unter [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0213a-115">For more information about <xref:System.Windows.Media.Drawing> objects, see the [Drawing Objects Overview](drawing-objects-overview.md).</span></span>
