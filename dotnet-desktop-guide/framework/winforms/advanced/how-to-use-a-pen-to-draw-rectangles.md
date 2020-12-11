---
title: 'Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Rechtecken'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- rectangles [Windows Forms], drawing
- pens [Windows Forms], drawing rectangles
ms.assetid: 54a7fa14-3ad8-4d64-b424-2a12005b250c
ms.openlocfilehash: cd5d965f8b92d15cdeb3049330d9b3cc0de893b2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975855"
---
# <a name="how-to-use-a-pen-to-draw-rectangles"></a><span data-ttu-id="fe831-102">Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Rechtecken</span><span class="sxs-lookup"><span data-stu-id="fe831-102">How to: Use a Pen to Draw Rectangles</span></span>
<span data-ttu-id="fe831-103">Um Rechtecke zu zeichnen, benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt.</span><span class="sxs-lookup"><span data-stu-id="fe831-103">To draw rectangles, you need a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="fe831-104">Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawRectangle%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Funktionen der Zeile, z. b. Farbe und Breite.</span><span class="sxs-lookup"><span data-stu-id="fe831-104">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawRectangle%2A> method, and the <xref:System.Drawing.Pen> object stores features of the line, such as color and width.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fe831-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fe831-105">Example</span></span>  
 <span data-ttu-id="fe831-106">Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (10, 10) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fe831-106">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="fe831-107">Das Rechteck hat eine Breite von 100 und eine Höhe von 50.</span><span class="sxs-lookup"><span data-stu-id="fe831-107">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="fe831-108">Das zweite Argument, das an den <xref:System.Drawing.Pen.%23ctor%2A> Konstruktor übergeben wird, gibt an, dass die Stift Breite 5 Pixel beträgt.</span><span class="sxs-lookup"><span data-stu-id="fe831-108">The second argument passed to the <xref:System.Drawing.Pen.%23ctor%2A> constructor indicates that the pen width is 5 pixels.</span></span>  
  
 <span data-ttu-id="fe831-109">Wenn das Rechteck gezeichnet wird, wird der Stift auf die Begrenzung des Rechtecks zentriert.</span><span class="sxs-lookup"><span data-stu-id="fe831-109">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="fe831-110">Da die Stift Breite 5 beträgt, werden die Seiten des Rechtecks 5 Pixel breit gezeichnet, sodass 1 Pixel an der Grenze selbst gezeichnet wird, 2 Pixel im inneren gezeichnet werden und 2 Pixel auf der Außenseite gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="fe831-110">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="fe831-111">Weitere Informationen zur Ausrichtung von Pen finden Sie unter Gewusst [wie: Festlegen der Stift Breite und-Ausrichtung](how-to-set-pen-width-and-alignment.md).</span><span class="sxs-lookup"><span data-stu-id="fe831-111">For more details on pen alignment, see [How to: Set Pen Width and Alignment](how-to-set-pen-width-and-alignment.md).</span></span>  
  
 <span data-ttu-id="fe831-112">Die folgende Abbildung zeigt das resultierende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="fe831-112">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="fe831-113">Die gepunkteten Linien zeigen an, wo das Rechteck gezeichnet worden wäre, wenn die Stift Breite ein Pixel gewesen wäre.</span><span class="sxs-lookup"><span data-stu-id="fe831-113">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="fe831-114">Die erweiterte Ansicht der oberen linken Ecke des Rechtecks zeigt, dass die dicken schwarzen Linien auf diese gepunkteten Linien zentriert sind.</span><span class="sxs-lookup"><span data-stu-id="fe831-114">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>  
  
 ![Screenshot, der das gezeichnete Rechteck mit schwarzen und gepunkteten Linien anzeigt](./media/how-to-use-a-pen-to-draw-rectangles/drawn-rectangle-black-lines-dotted-lines.gif)  
  
 [!code-csharp[System.Drawing.UsingAPen#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.UsingAPen#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fe831-116">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="fe831-116">Compiling the Code</span></span>  
 <span data-ttu-id="fe831-117">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="fe831-117">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe831-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe831-118">See also</span></span>

- [<span data-ttu-id="fe831-119">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="fe831-119">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
