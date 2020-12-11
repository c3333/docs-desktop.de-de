---
title: 'Gewusst wie: Zeichnen eines einzelnen B-&#233;Zier-Spline'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines [Windows Forms], drawing
- drawing [Windows Forms], Bezier splines
ms.assetid: f4f3fe30-f0a6-4743-ac91-11310cebea9f
ms.openlocfilehash: ebb53e7df979a553ed4a44deba34345c9ecac772
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975941"
---
# <a name="how-to-draw-a-single-b233zier-spline"></a><span data-ttu-id="90de2-102">Gewusst wie: Zeichnen eines einzelnen B-&#233;Zier-Spline</span><span class="sxs-lookup"><span data-stu-id="90de2-102">How to: Draw a Single B&#233;zier Spline</span></span>
<span data-ttu-id="90de2-103">Eine Bézier-Spline wird von vier Punkten definiert: einem Startpunkt, zwei Kontrollpunkten und einem Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="90de2-103">A Bézier spline is defined by four points: a start point, two control points, and an endpoint.</span></span>  
  
## <a name="example"></a><span data-ttu-id="90de2-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="90de2-104">Example</span></span>  
 <span data-ttu-id="90de2-105">Im folgenden Beispiel wird eine Bézier-Spline mit dem Startpunkt (10, 100) und dem Endpunkt (200, 100) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="90de2-105">The following example draws a Bézier spline with start point (10, 100) and endpoint (200, 100).</span></span> <span data-ttu-id="90de2-106">Die Kontrollpunkte lauten (100, 10) und (150, 150).</span><span class="sxs-lookup"><span data-stu-id="90de2-106">The control points are (100, 10) and (150, 150).</span></span>  
  
 <span data-ttu-id="90de2-107">In der folgenden Abbildung wird der resultierende Bézier-Spline zusammen mit dem Startpunkt, den Kontrollpunkten und dem Endpunkt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="90de2-107">The following illustration shows the resulting Bézier spline along with its start point, control points, and endpoint.</span></span> <span data-ttu-id="90de2-108">Die Abbildung zeigt auch die zusammen Geviert-Hülle des Splines, bei der es sich um ein Polygon handelt, das durch Verbinden der vier Punkte mit geraden Linien gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="90de2-108">The illustration also shows the spline's convex hull, which is a polygon formed by connecting the four points with straight lines.</span></span>  
  
 ![Abbildung einer Bezier-Spline.](./media/how-to-draw-a-single-bezier-spline/bezier-spline-illustration.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="90de2-110">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="90de2-110">Compiling the Code</span></span>  
 <span data-ttu-id="90de2-111">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="90de2-111">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90de2-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90de2-112">See also</span></span>

- <xref:System.Drawing.Graphics.DrawBezier%2A>
- [<span data-ttu-id="90de2-113">Bézier-Splines in GDI+</span><span class="sxs-lookup"><span data-stu-id="90de2-113">Bézier Splines in GDI+</span></span>](bezier-splines-in-gdi.md)
- [<span data-ttu-id="90de2-114">Vorgehensweise: Zeichnen einer Folge von Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="90de2-114">How to: Draw a Sequence of Bézier Splines</span></span>](how-to-draw-a-sequence-of-bezier-splines.md)
