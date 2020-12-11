---
title: 'Gewusst wie: Erstellen einer GeometryDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], renderable
- renderable shapes [WPF]
- graphics [WPF], GeometryDrawing class
- classes [WPF], GeometryDrawing
ms.assetid: 11d3c096-91ba-4d41-9bba-aeac0db70f97
ms.openlocfilehash: f5cdcfdb68ad8030bcbd6c689f45a8baddd000e1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977607"
---
# <a name="how-to-create-a-geometrydrawing"></a><span data-ttu-id="5eb2d-102">Gewusst wie: Erstellen einer GeometryDrawing</span><span class="sxs-lookup"><span data-stu-id="5eb2d-102">How to: Create a GeometryDrawing</span></span>
<span data-ttu-id="5eb2d-103">In diesem Beispiel wird gezeigt, wie ein erstellt und angezeigt wird <xref:System.Windows.Media.GeometryDrawing> .</span><span class="sxs-lookup"><span data-stu-id="5eb2d-103">This example shows how to create and display a <xref:System.Windows.Media.GeometryDrawing>.</span></span> <span data-ttu-id="5eb2d-104">Mit einem <xref:System.Windows.Media.GeometryDrawing> können Sie eine Form mit einer Füllung und einem Umriss erstellen, indem Sie eine <xref:System.Windows.Media.Pen> und eine <xref:System.Windows.Media.Brush> mit einem verknüpfen <xref:System.Windows.Media.Geometry> .</span><span class="sxs-lookup"><span data-stu-id="5eb2d-104">A <xref:System.Windows.Media.GeometryDrawing> enables you to create shape with a fill and an outline by associating a <xref:System.Windows.Media.Pen> and a <xref:System.Windows.Media.Brush> with a <xref:System.Windows.Media.Geometry>.</span></span> <span data-ttu-id="5eb2d-105">Der <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> beschreibt die Struktur der Form, <xref:System.Windows.Media.GeometryDrawing.Brush%2A> beschreibt die Füllung der Form und <xref:System.Windows.Media.GeometryDrawing.Pen%2A> beschreibt die Kontur der Form.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-105">The <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> describes the shape's structure, the <xref:System.Windows.Media.GeometryDrawing.Brush%2A> describes the shape's fill, and the <xref:System.Windows.Media.GeometryDrawing.Pen%2A> describes the shape's outline.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5eb2d-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5eb2d-106">Example</span></span>  
 <span data-ttu-id="5eb2d-107">Im folgenden Beispiel wird ein-Typ verwendet <xref:System.Windows.Media.GeometryDrawing> , um eine Form zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-107">The following example uses a <xref:System.Windows.Media.GeometryDrawing> to render a shape.</span></span> <span data-ttu-id="5eb2d-108">Die Form wird durch ein <xref:System.Windows.Media.GeometryGroup> und zwei- <xref:System.Windows.Media.EllipseGeometry> Objekte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-108">The shape is described by a <xref:System.Windows.Media.GeometryGroup> and two <xref:System.Windows.Media.EllipseGeometry> objects.</span></span> <span data-ttu-id="5eb2d-109">Das Innere der Form wird mit einem <xref:System.Windows.Media.LinearGradientBrush> gezeichnet, und der Umriss wird mit einem gezeichnet <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen> .</span><span class="sxs-lookup"><span data-stu-id="5eb2d-109">The shape's interior is painted with a <xref:System.Windows.Media.LinearGradientBrush> and its outline is drawn with a <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen>.</span></span> <span data-ttu-id="5eb2d-110">Die <xref:System.Windows.Media.GeometryDrawing> wird mit einem <xref:System.Windows.Media.ImageDrawing> -Element und einem- <xref:System.Windows.Controls.Image> Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-110">The <xref:System.Windows.Media.GeometryDrawing> is displayed using an <xref:System.Windows.Media.ImageDrawing> and an <xref:System.Windows.Controls.Image> element.</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/GeometryDrawingExample.cs#geometrydrawingexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/GeometryDrawingExample.xaml#geometrydrawingexamplewholepage)]  
  
 <span data-ttu-id="5eb2d-111">In der folgenden Abbildung wird das resultierende gezeigt <xref:System.Windows.Media.GeometryDrawing> .</span><span class="sxs-lookup"><span data-stu-id="5eb2d-111">The following illustration shows the resulting <xref:System.Windows.Media.GeometryDrawing>.</span></span>  
  
 <span data-ttu-id="5eb2d-112">![Eine GeometryDrawing von zwei Ellipsen](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span><span class="sxs-lookup"><span data-stu-id="5eb2d-112">![A GeometryDrawing of two ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span></span>  
  
 <span data-ttu-id="5eb2d-113">Um komplexere Zeichnungen zu erstellen, können Sie mehrere Zeichnungsobjekte in einer einzelnen zusammengesetzten Zeichnung mit einem kombinieren <xref:System.Windows.Media.DrawingGroup> .</span><span class="sxs-lookup"><span data-stu-id="5eb2d-113">To create more complex drawings, you can combine multiple drawing objects into a single composite drawing using a <xref:System.Windows.Media.DrawingGroup>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5eb2d-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eb2d-114">See also</span></span>

- <xref:System.Windows.Media.DrawingGroup>
- [<span data-ttu-id="5eb2d-115">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="5eb2d-115">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="5eb2d-116">Übersicht über die Geometrie</span><span class="sxs-lookup"><span data-stu-id="5eb2d-116">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="5eb2d-117">Erstellen einer zusammengesetzten Zeichnung</span><span class="sxs-lookup"><span data-stu-id="5eb2d-117">Create a Composite Drawing</span></span>](how-to-create-a-composite-drawing.md)
