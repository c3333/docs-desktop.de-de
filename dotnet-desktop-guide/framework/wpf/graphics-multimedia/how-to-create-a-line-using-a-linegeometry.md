---
title: 'Gewusst wie: Erstellen einer Linie mit einer LineGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], lines
ms.assetid: 41231b22-1f74-4c26-a8e7-a55b29f8f6bd
ms.openlocfilehash: f8c334a54f78aec7af91064a447fd18f23dcfbdc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977408"
---
# <a name="how-to-create-a-line-using-a-linegeometry"></a><span data-ttu-id="0ae9a-102">Gewusst wie: Erstellen einer Linie mit einer LineGeometry</span><span class="sxs-lookup"><span data-stu-id="0ae9a-102">How to: Create a Line Using a LineGeometry</span></span>
<span data-ttu-id="0ae9a-103">In diesem Beispiel wird gezeigt, wie die-Klasse verwendet wird <xref:System.Windows.Media.LineGeometry> , um eine Zeile zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0ae9a-103">This example shows how to use the <xref:System.Windows.Media.LineGeometry> class to describe a line.</span></span> <span data-ttu-id="0ae9a-104">Eine <xref:System.Windows.Media.LineGeometry> wird durch die Start-und Endpunkte definiert.</span><span class="sxs-lookup"><span data-stu-id="0ae9a-104">A <xref:System.Windows.Media.LineGeometry> is defined by its start and end points.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ae9a-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ae9a-105">Example</span></span>  
 <span data-ttu-id="0ae9a-106">Im folgenden Beispiel wird gezeigt, wie ein erstellt und dargestellt wird <xref:System.Windows.Media.LineGeometry> .</span><span class="sxs-lookup"><span data-stu-id="0ae9a-106">The following example shows how to create and render a <xref:System.Windows.Media.LineGeometry>.</span></span>  <span data-ttu-id="0ae9a-107">Ein- <xref:System.Windows.Shapes.Path> Element wird verwendet, um die Zeile zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="0ae9a-107">A <xref:System.Windows.Shapes.Path> element is used to render the line.</span></span>  <span data-ttu-id="0ae9a-108">Da eine Linie keinen Bereich aufweist, <xref:System.Windows.Shapes.Path> wird das Objekt <xref:System.Windows.Shapes.Shape.Fill%2A> nicht angegeben. stattdessen werden die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Shapes.Shape.Stroke%2A> <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ae9a-108">Since a line has no area, the <xref:System.Windows.Shapes.Path> object's <xref:System.Windows.Shapes.Shape.Fill%2A> is not specified; instead the <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> properties are used.</span></span>  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmlinegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmlinegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmlinegeometryexample)]  
  
 <span data-ttu-id="0ae9a-109">![LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")</span><span class="sxs-lookup"><span data-stu-id="0ae9a-109">![A LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")</span></span>  
<span data-ttu-id="0ae9a-110">Eine LineGeometry, gezeichnet von (10,20) bis (100,130)</span><span class="sxs-lookup"><span data-stu-id="0ae9a-110">A LineGeometry drawn from (10,20) to (100,130)</span></span>  
  
 <span data-ttu-id="0ae9a-111">Andere einfache Geometry-Klassen sind <xref:System.Windows.Media.LineGeometry> und <xref:System.Windows.Media.EllipseGeometry> .</span><span class="sxs-lookup"><span data-stu-id="0ae9a-111">Other simple geometry classes include <xref:System.Windows.Media.LineGeometry> and <xref:System.Windows.Media.EllipseGeometry>.</span></span> <span data-ttu-id="0ae9a-112">Diese Geometrien und komplexere können auch mithilfe von oder erstellt werden <xref:System.Windows.Media.PathGeometry> <xref:System.Windows.Media.StreamGeometry> .</span><span class="sxs-lookup"><span data-stu-id="0ae9a-112">These geometries, as well as more complex ones, can also be created using a <xref:System.Windows.Media.PathGeometry> or <xref:System.Windows.Media.StreamGeometry>.</span></span> <span data-ttu-id="0ae9a-113">Weitere Informationen finden Sie in der [Übersicht über die Geometrie](geometry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0ae9a-113">For more information, see the [Geometry Overview](geometry-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ae9a-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ae9a-114">See also</span></span>

- [<span data-ttu-id="0ae9a-115">Übersicht über die Geometrie</span><span class="sxs-lookup"><span data-stu-id="0ae9a-115">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="0ae9a-116">Erstellen einer zusammengesetzten Form</span><span class="sxs-lookup"><span data-stu-id="0ae9a-116">Create a Composite Shape</span></span>](how-to-create-a-composite-shape.md)
- [<span data-ttu-id="0ae9a-117">Erstellen einer Form mithilfe einer PathGeometry</span><span class="sxs-lookup"><span data-stu-id="0ae9a-117">Create a Shape by Using a PathGeometry</span></span>](how-to-create-a-shape-by-using-a-pathgeometry.md)
