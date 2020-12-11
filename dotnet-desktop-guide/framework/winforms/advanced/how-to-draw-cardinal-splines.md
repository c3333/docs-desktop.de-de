---
title: 'Vorgehensweise: Zeichnen von kardinalen Splines'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cardinal splines [Windows Forms], drawing
- drawing [Windows Forms], cardinal splines
- graphics [Windows Forms], cardinal splines
ms.assetid: a4a41e80-4461-4b47-b6bd-2c5e68881994
ms.openlocfilehash: 12e938567d529b33ead93e081d380a650a803f23
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975931"
---
# <a name="how-to-draw-cardinal-splines"></a><span data-ttu-id="0bce1-102">Vorgehensweise: Zeichnen von kardinalen Splines</span><span class="sxs-lookup"><span data-stu-id="0bce1-102">How to: Draw Cardinal Splines</span></span>
<span data-ttu-id="0bce1-103">Eine kardinale Splinekurve ist eine Kurve, die durch einen bestimmten Satz von Punkten reibungslos verläuft.</span><span class="sxs-lookup"><span data-stu-id="0bce1-103">A cardinal spline is a curve that passes smoothly through a given set of points.</span></span> <span data-ttu-id="0bce1-104">Um einen kardinalspline zu zeichnen, erstellen Sie ein <xref:System.Drawing.Graphics> -Objekt, und übergeben Sie die Adresse eines Arrays von Punkten an die- <xref:System.Drawing.Graphics.DrawCurve%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="0bce1-104">To draw a cardinal spline, create a <xref:System.Drawing.Graphics> object and pass the address of an array of points to the <xref:System.Drawing.Graphics.DrawCurve%2A> method.</span></span>  
  
### <a name="drawing-a-bell-shaped-cardinal-spline"></a><span data-ttu-id="0bce1-105">Zeichnen eines Bell-Shaped kardinalspline</span><span class="sxs-lookup"><span data-stu-id="0bce1-105">Drawing a Bell-Shaped Cardinal Spline</span></span>  
  
- <span data-ttu-id="0bce1-106">Im folgenden Beispiel wird ein glockenförmiger kardinaler Spline gezeichnet, der fünf festgelegte Punkte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="0bce1-106">The following example draws a bell-shaped cardinal spline that passes through five designated points.</span></span> <span data-ttu-id="0bce1-107">In der folgenden Abbildung werden die Kurve und fünf Punkte dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0bce1-107">The following illustration shows the curve and five points.</span></span>  
  
     ![Diagramm, das einen glockenförmigen kardinalspline anzeigt.](./media/how-to-draw-cardinal-splines/bell-shaped-cardinal-spline.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#21)]  
  
### <a name="drawing-a-closed-cardinal-spline"></a><span data-ttu-id="0bce1-109">Zeichnen einer geschlossenen kardinalspline</span><span class="sxs-lookup"><span data-stu-id="0bce1-109">Drawing a Closed Cardinal Spline</span></span>  
  
- <span data-ttu-id="0bce1-110">Verwenden Sie die- <xref:System.Drawing.Graphics.DrawClosedCurve%2A> Methode der- <xref:System.Drawing.Graphics> Klasse, um einen geschlossenen kardinalspline zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0bce1-110">Use the <xref:System.Drawing.Graphics.DrawClosedCurve%2A> method of the <xref:System.Drawing.Graphics> class to draw a closed cardinal spline.</span></span> <span data-ttu-id="0bce1-111">In einer geschlossenen kardinalsplinekurve wird die Kurve bis zum letzten Punkt im Array fortgesetzt und stellt eine Verbindung mit dem ersten Punkt im Array her.</span><span class="sxs-lookup"><span data-stu-id="0bce1-111">In a closed cardinal spline, the curve continues through the last point in the array and connects with the first point in the array.</span></span> <span data-ttu-id="0bce1-112">Im folgenden Beispiel wird eine geschlossene kardinale Spline gezeichnet, die sechs festgelegte Punkte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="0bce1-112">The following example draws a closed cardinal spline that passes through six designated points.</span></span> <span data-ttu-id="0bce1-113">Die folgende Abbildung zeigt den geschlossenen Spline zusammen mit den sechs Punkten:</span><span class="sxs-lookup"><span data-stu-id="0bce1-113">The following illustration shows the closed spline along with the six points:</span></span>  
  
 ![Diagramm, das einen geschlossenen kardinalspline anzeigt.](./media/how-to-draw-cardinal-splines/closed-cardinal-spine.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#22)]  
  
### <a name="changing-the-bend-of-a-cardinal-spline"></a><span data-ttu-id="0bce1-115">Ändern der Kurve eines kardinalen Spline</span><span class="sxs-lookup"><span data-stu-id="0bce1-115">Changing the Bend of a Cardinal Spline</span></span>  
  
- <span data-ttu-id="0bce1-116">Ändern Sie die Art und Weise, in der sich ein kardinaler Spline mit einem Spannungs Argument an die <xref:System.Drawing.Graphics.DrawCurve%2A> Methode beugt.</span><span class="sxs-lookup"><span data-stu-id="0bce1-116">Change the way a cardinal spline bends by passing a tension argument to the <xref:System.Drawing.Graphics.DrawCurve%2A> method.</span></span> <span data-ttu-id="0bce1-117">Im folgenden Beispiel werden drei kardinale Splines gezeichnet, die denselben Satz von Punkten durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0bce1-117">The following example draws three cardinal splines that pass through the same set of points.</span></span> <span data-ttu-id="0bce1-118">Die folgende Abbildung zeigt die drei Splines zusammen mit Ihren Spannungswerten.</span><span class="sxs-lookup"><span data-stu-id="0bce1-118">The following illustration shows the three splines along with their tension values.</span></span> <span data-ttu-id="0bce1-119">Beachten Sie, dass die Punkte durch gerade Linien verbunden sind, wenn die Spannung den Wert 0 hat.</span><span class="sxs-lookup"><span data-stu-id="0bce1-119">Note that when the tension is 0, the points are connected by straight lines.</span></span>  
  
 ![Diagramm, das drei kardinale Splines anzeigt.](./media/how-to-draw-cardinal-splines/three-cardinal-splines.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#23)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#23)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0bce1-121">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="0bce1-121">Compiling the Code</span></span>  
 <span data-ttu-id="0bce1-122">Die vorhergehenden Beispiele sind für die Verwendung mit Windows Forms konzipiert und erfordern <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="0bce1-122">The preceding examples are designed for use with Windows Forms, and they require <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bce1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bce1-123">See also</span></span>

- [<span data-ttu-id="0bce1-124">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="0bce1-124">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="0bce1-125">Erstellen und Zeichnen von Kurven</span><span class="sxs-lookup"><span data-stu-id="0bce1-125">Constructing and Drawing Curves</span></span>](constructing-and-drawing-curves.md)
