---
title: 'Gewusst wie: Erstellen einer zusammengesetzten Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- shapes [WPF], composite
- composite shapes [WPF]
- graphics [WPF], composite shapes
ms.assetid: 8e5c7ef4-d7ed-4c43-afc9-ca01325c300b
ms.openlocfilehash: c56053f2b07d6055deac5097a68fd7b80ad704ba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977608"
---
# <a name="how-to-create-a-composite-shape"></a><span data-ttu-id="78a62-102">Gewusst wie: Erstellen einer zusammengesetzten Form</span><span class="sxs-lookup"><span data-stu-id="78a62-102">How to: Create a Composite Shape</span></span>
<span data-ttu-id="78a62-103">In diesem Beispiel wird gezeigt, wie zusammengesetzte Formen mithilfe von <xref:System.Windows.Media.Geometry> Objekten erstellt und mit einem-Element angezeigt werden <xref:System.Windows.Shapes.Path> .</span><span class="sxs-lookup"><span data-stu-id="78a62-103">This example shows how to create composite shapes using <xref:System.Windows.Media.Geometry> objects and display them using a <xref:System.Windows.Shapes.Path> element.</span></span> <span data-ttu-id="78a62-104">Im folgenden Beispiel <xref:System.Windows.Media.LineGeometry> <xref:System.Windows.Media.EllipseGeometry> werden, und mit einem verwendet, <xref:System.Windows.Media.RectangleGeometry> <xref:System.Windows.Media.GeometryGroup> um eine zusammengesetzte Form zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78a62-104">In the following example, a <xref:System.Windows.Media.LineGeometry>, <xref:System.Windows.Media.EllipseGeometry>, and a <xref:System.Windows.Media.RectangleGeometry> are used with a <xref:System.Windows.Media.GeometryGroup> to create a composite shape.</span></span> <span data-ttu-id="78a62-105">Die Geometrien werden dann mit einem- <xref:System.Windows.Shapes.Path> Element gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="78a62-105">The geometries are then drawn using a <xref:System.Windows.Shapes.Path> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78a62-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="78a62-106">Example</span></span>  
 [!code-xaml[GeometrySample#19](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#19)]  
  
 [!code-csharp[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/CSharp/CompositeShapeExample.cs#compositeshapecodeexampleinline1)]
 [!code-vb[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/visualbasic/compositeshapeexample.vb#compositeshapecodeexampleinline1)]  
  
 <span data-ttu-id="78a62-107">Die folgende Abbildung zeigt die im vorherigen Beispiel erstellte Form.</span><span class="sxs-lookup"><span data-stu-id="78a62-107">The following illustration shows the shape created in the previous example.</span></span>  
  
 <span data-ttu-id="78a62-108">![Eine zusammengesetzte Geometrie, die mit einer GeometryGroup erstellt wird](./media/wcpsdk-graphicsmm-compositegeometryexample1.jpg "wcpsdk_graphicsmm_compositegeometryexample1")</span><span class="sxs-lookup"><span data-stu-id="78a62-108">![A composite geometry created using a GeometryGroup](./media/wcpsdk-graphicsmm-compositegeometryexample1.jpg "wcpsdk_graphicsmm_compositegeometryexample1")</span></span>  
<span data-ttu-id="78a62-109">Zusammengesetzte Geometrie</span><span class="sxs-lookup"><span data-stu-id="78a62-109">Composite Geometry</span></span>  
  
 <span data-ttu-id="78a62-110">Komplexere Formen (z. b. Polygone und Formen mit gekrümmten Segmenten) können mithilfe von erstellt werden <xref:System.Windows.Media.PathGeometry> .</span><span class="sxs-lookup"><span data-stu-id="78a62-110">More complex shapes, such as polygons and shapes with curved segments, may be created using a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="78a62-111">Ein Beispiel, das zeigt, wie eine Form mithilfe <xref:System.Windows.Media.PathGeometry> von erstellt wird, finden Sie unter [Erstellen einer Form mithilfe von PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md).</span><span class="sxs-lookup"><span data-stu-id="78a62-111">For an example showing how to create a shape using a <xref:System.Windows.Media.PathGeometry>, see [Create a Shape by Using a PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md).</span></span>  <span data-ttu-id="78a62-112">Obwohl in diesem Beispiel eine Form mit einem-Element auf dem Bildschirm gerendert <xref:System.Windows.Shapes.Path> wird, <xref:System.Windows.Media.Geometry> können-Objekte auch verwendet werden, um den Inhalt einer <xref:System.Windows.Media.GeometryDrawing> oder einer zu beschreiben <xref:System.Windows.Media.DrawingContext> .</span><span class="sxs-lookup"><span data-stu-id="78a62-112">Although this example renders a shape to the screen using a <xref:System.Windows.Shapes.Path> element, <xref:System.Windows.Media.Geometry> objects may also be used to describe the contents of a <xref:System.Windows.Media.GeometryDrawing> or a <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="78a62-113">Sie können auch für Clipping-und Treffer Tests verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78a62-113">They may also be used for clipping and hit-testing.</span></span>  
  
 <span data-ttu-id="78a62-114">Dieses Beispiel ist Teil eines größeren Beispiels. Das vollständige Beispiel finden Sie unter [Beispiel für Geometrien](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Geometry).</span><span class="sxs-lookup"><span data-stu-id="78a62-114">This example is part of larger sample; for the complete sample, see the [Geometries Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Geometry).</span></span>
