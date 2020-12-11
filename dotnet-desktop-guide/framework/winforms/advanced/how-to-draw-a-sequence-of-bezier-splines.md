---
title: 'Gewusst wie: Zeichnen einer Sequenz von B&#233;Zier-Splines'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- splines [Windows Forms], drawing Bezier
- Bezier splines [Windows Forms], drawing sequence of
ms.assetid: 37a0bedb-20c2-4cf0-91fa-a5509e826b30
ms.openlocfilehash: 976787f5830282a581d05a9c24d1f83dceca4b25
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975942"
---
# <a name="how-to-draw-a-sequence-of-b233zier-splines"></a><span data-ttu-id="8f212-102">Gewusst wie: Zeichnen einer Sequenz von B&#233;Zier-Splines</span><span class="sxs-lookup"><span data-stu-id="8f212-102">How to: Draw a Sequence of B&#233;zier Splines</span></span>
<span data-ttu-id="8f212-103">Mit der- <xref:System.Drawing.Graphics.DrawBeziers%2A> Methode der-Klasse können Sie <xref:System.Drawing.Graphics> eine Sequenz verbundener Bézier-Splines zeichnen.</span><span class="sxs-lookup"><span data-stu-id="8f212-103">You can use the <xref:System.Drawing.Graphics.DrawBeziers%2A> method of the <xref:System.Drawing.Graphics> class to draw a sequence of connected Bézier splines.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8f212-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8f212-104">Example</span></span>  
 <span data-ttu-id="8f212-105">Im folgenden Beispiel wird eine Kurve gezeichnet, die aus zwei verbundenen Bézier-Splines besteht.</span><span class="sxs-lookup"><span data-stu-id="8f212-105">The following example draws a curve that consists of two connected Bézier splines.</span></span> <span data-ttu-id="8f212-106">Der Endpunkt der ersten Bézier-Spline ist der Startpunkt der zweiten Bézier-Spline.</span><span class="sxs-lookup"><span data-stu-id="8f212-106">The endpoint of the first Bézier spline is the start point of the second Bézier spline.</span></span>  
  
 <span data-ttu-id="8f212-107">In der folgenden Abbildung werden die verbundenen Splines zusammen mit den sieben Punkten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="8f212-107">The following illustration shows the connected splines along with the seven points:</span></span>  
  
 ![Grafik, in der die verbundenen Splines zusammen mit sieben Punkten angezeigt werden.](./media/how-to-draw-a-sequence-of-bezier-splines/bezier-spline-seven-points.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="8f212-109">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="8f212-109">Compiling the Code</span></span>  
 <span data-ttu-id="8f212-110">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="8f212-110">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f212-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f212-111">See also</span></span>

- [<span data-ttu-id="8f212-112">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8f212-112">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="8f212-113">Bézier-Splines in GDI+</span><span class="sxs-lookup"><span data-stu-id="8f212-113">Bézier Splines in GDI+</span></span>](bezier-splines-in-gdi.md)
- [<span data-ttu-id="8f212-114">Erstellen und Zeichnen von Kurven</span><span class="sxs-lookup"><span data-stu-id="8f212-114">Constructing and Drawing Curves</span></span>](constructing-and-drawing-curves.md)
