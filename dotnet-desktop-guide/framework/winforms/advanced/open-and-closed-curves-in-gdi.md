---
title: Offene und geschlossene Kurven in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- curves [Windows Forms], filling
- GDI+, curves
- curves [Windows Forms], drawing
- curves
ms.assetid: 08d2cc9a-dc9d-4eed-bcbb-2c8e2ca5d3ae
ms.openlocfilehash: 06afdc4549f7c3c9b0636e5c7052dcca87a153f1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976072"
---
# <a name="open-and-closed-curves-in-gdi"></a><span data-ttu-id="f63b1-102">Offene und geschlossene Kurven in GDI+</span><span class="sxs-lookup"><span data-stu-id="f63b1-102">Open and Closed Curves in GDI+</span></span>
<span data-ttu-id="f63b1-103">Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.</span><span class="sxs-lookup"><span data-stu-id="f63b1-103">The following illustration shows two curves: one open and one closed.</span></span>  
  
 <span data-ttu-id="f63b1-104">![Öffnen & geschlossenen Kurven](./media/aboutgdip02-art24.gif "Aboutgdip02_art24")</span><span class="sxs-lookup"><span data-stu-id="f63b1-104">![Open & Closed curves](./media/aboutgdip02-art24.gif "Aboutgdip02_art24")</span></span>  
  
## <a name="managed-interface-for-curves"></a><span data-ttu-id="f63b1-105">Verwaltete Schnittstelle für Kurven</span><span class="sxs-lookup"><span data-stu-id="f63b1-105">Managed Interface for Curves</span></span>  
 <span data-ttu-id="f63b1-106">Geschlossene Kurven verfügen über ein inneres und können daher mit einem Pinsel gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="f63b1-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="f63b1-107">Die <xref:System.Drawing.Graphics> -Klasse in GDI+ bietet die folgenden Methoden zum Auffüllen geschlossener Formen und Kurven: <xref:System.Drawing.Graphics.FillRectangle%2A> , <xref:System.Drawing.Graphics.FillEllipse%2A> , <xref:System.Drawing.Graphics.FillPie%2A> , <xref:System.Drawing.Graphics.FillPolygon%2A> , <xref:System.Drawing.Graphics.FillClosedCurve%2A> , <xref:System.Drawing.Graphics.FillPath%2A> und <xref:System.Drawing.Graphics.FillRegion%2A> .</span><span class="sxs-lookup"><span data-stu-id="f63b1-107">The <xref:System.Drawing.Graphics> class in GDI+ provides the following methods for filling closed shapes and curves: <xref:System.Drawing.Graphics.FillRectangle%2A>, <xref:System.Drawing.Graphics.FillEllipse%2A>, <xref:System.Drawing.Graphics.FillPie%2A>, <xref:System.Drawing.Graphics.FillPolygon%2A>, <xref:System.Drawing.Graphics.FillClosedCurve%2A>, <xref:System.Drawing.Graphics.FillPath%2A>, and <xref:System.Drawing.Graphics.FillRegion%2A>.</span></span> <span data-ttu-id="f63b1-108">Wenn Sie eine dieser Methoden aufzurufen, müssen Sie einen der spezifischen Pinseltypen ( <xref:System.Drawing.SolidBrush> , <xref:System.Drawing.Drawing2D.HatchBrush> , <xref:System.Drawing.TextureBrush> , <xref:System.Drawing.Drawing2D.LinearGradientBrush> oder <xref:System.Drawing.Drawing2D.PathGradientBrush> ) als Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="f63b1-108">Whenever you call one of these methods, you must pass one of the specific brush types (<xref:System.Drawing.SolidBrush>, <xref:System.Drawing.Drawing2D.HatchBrush>, <xref:System.Drawing.TextureBrush>, <xref:System.Drawing.Drawing2D.LinearGradientBrush>, or <xref:System.Drawing.Drawing2D.PathGradientBrush>) as an argument.</span></span>  
  
 <span data-ttu-id="f63b1-109">Die- <xref:System.Drawing.Graphics.FillPie%2A> Methode ist ein begleitende der- <xref:System.Drawing.Graphics.DrawArc%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="f63b1-109">The <xref:System.Drawing.Graphics.FillPie%2A> method is a companion to the <xref:System.Drawing.Graphics.DrawArc%2A> method.</span></span> <span data-ttu-id="f63b1-110">Ebenso wie die- <xref:System.Drawing.Graphics.DrawArc%2A> Methode einen Teil der Gliederung einer Ellipse zeichnet, füllt die- <xref:System.Drawing.Graphics.FillPie%2A> Methode einen Teil des Inneren einer Ellipse aus.</span><span class="sxs-lookup"><span data-stu-id="f63b1-110">Just as the <xref:System.Drawing.Graphics.DrawArc%2A> method draws a portion of the outline of an ellipse, the <xref:System.Drawing.Graphics.FillPie%2A> method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="f63b1-111">Im folgenden Beispiel wird ein Bogen gezeichnet und der entsprechende Teil des Inneren der Ellipse gefüllt:</span><span class="sxs-lookup"><span data-stu-id="f63b1-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#21](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#21)]
 [!code-vb[LinesCurvesAndShapes#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#21)]  
  
 <span data-ttu-id="f63b1-112">Die folgende Abbildung zeigt den Bogen und den gefüllten Kreis.</span><span class="sxs-lookup"><span data-stu-id="f63b1-112">The following illustration shows the arc and the filled pie.</span></span>  
  
 <span data-ttu-id="f63b1-113">![Öffnen & geschlossenen Kurven](./media/aboutgdip02-art25.gif "Aboutgdip02_art25")</span><span class="sxs-lookup"><span data-stu-id="f63b1-113">![Open & Closed curves](./media/aboutgdip02-art25.gif "Aboutgdip02_art25")</span></span>  
  
 <span data-ttu-id="f63b1-114">Die- <xref:System.Drawing.Graphics.FillClosedCurve%2A> Methode ist ein begleitende der- <xref:System.Drawing.Graphics.DrawClosedCurve%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="f63b1-114">The <xref:System.Drawing.Graphics.FillClosedCurve%2A> method is a companion to the <xref:System.Drawing.Graphics.DrawClosedCurve%2A> method.</span></span> <span data-ttu-id="f63b1-115">Beide Methoden schließen die Kurve automatisch, indem Sie den Endpunkt mit dem Ausgangspunkt verbinden.</span><span class="sxs-lookup"><span data-stu-id="f63b1-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="f63b1-116">Im folgenden Beispiel wird eine Kurve gezeichnet, die durchläuft (0,0), (60, 20) und (40, 50).</span><span class="sxs-lookup"><span data-stu-id="f63b1-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="f63b1-117">Anschließend wird die Kurve automatisch geschlossen, indem (40, 50) mit dem Anfangspunkt (0,0) verbunden wird, und das innere wird mit einer voll Tonfarbe gefüllt.</span><span class="sxs-lookup"><span data-stu-id="f63b1-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#22](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#22)]
 [!code-vb[LinesCurvesAndShapes#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#22)]  
  
 <span data-ttu-id="f63b1-118">Die- <xref:System.Drawing.Graphics.FillPath%2A> Methode füllt die Innenbereiche der separaten Teile eines Pfades.</span><span class="sxs-lookup"><span data-stu-id="f63b1-118">The <xref:System.Drawing.Graphics.FillPath%2A> method fills the interiors of the separate pieces of a path.</span></span> <span data-ttu-id="f63b1-119">Wenn ein Teil eines Pfads keine geschlossene Kurve oder Form bildet, schließt die <xref:System.Drawing.Graphics.FillPath%2A> Methode diesen Teil des Pfads automatisch, bevor Sie ihn füllt.</span><span class="sxs-lookup"><span data-stu-id="f63b1-119">If a piece of a path doesn't form a closed curve or shape, the <xref:System.Drawing.Graphics.FillPath%2A> method automatically closes that piece of the path before filling it.</span></span> <span data-ttu-id="f63b1-120">Im folgenden Beispiel wird ein Pfad, der aus einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis besteht, gezeichnet und gefüllt:</span><span class="sxs-lookup"><span data-stu-id="f63b1-120">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#23](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#23)]
 [!code-vb[LinesCurvesAndShapes#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#23)]  
  
 <span data-ttu-id="f63b1-121">In der folgenden Abbildung wird der Pfad mit und ohne das voll Bild Füll Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f63b1-121">The following illustration shows the path with and without the solid fill.</span></span> <span data-ttu-id="f63b1-122">Beachten Sie, dass der Text in der Zeichenfolge von der-Methode beschrieben, aber nicht ausgefüllt wird <xref:System.Drawing.Graphics.DrawPath%2A> .</span><span class="sxs-lookup"><span data-stu-id="f63b1-122">Note that the text in the string is outlined, but not filled, by the <xref:System.Drawing.Graphics.DrawPath%2A> method.</span></span> <span data-ttu-id="f63b1-123">Dabei handelt es sich um die <xref:System.Drawing.Graphics.FillPath%2A> Methode, die das Innere der Zeichen in der Zeichenfolge zeichnet.</span><span class="sxs-lookup"><span data-stu-id="f63b1-123">It is the <xref:System.Drawing.Graphics.FillPath%2A> method that paints the interiors of the characters in the string.</span></span>  
  
 <span data-ttu-id="f63b1-124">![Zeichenfolge in einem Pfad](./media/aboutgdip02-art26.gif "Aboutgdip02_art26")</span><span class="sxs-lookup"><span data-stu-id="f63b1-124">![String in a path](./media/aboutgdip02-art26.gif "Aboutgdip02_art26")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f63b1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f63b1-125">See also</span></span>

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Point?displayProperty=nameWithType>
- [<span data-ttu-id="f63b1-126">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="f63b1-126">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="f63b1-127">Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="f63b1-127">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="f63b1-128">Erstellen und Zeichnen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="f63b1-128">Constructing and Drawing Paths</span></span>](constructing-and-drawing-paths.md)
