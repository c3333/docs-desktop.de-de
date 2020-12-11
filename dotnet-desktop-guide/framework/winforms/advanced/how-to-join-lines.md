---
title: 'Vorgehensweise: Verknüpfen von Linien'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- miter line join style
- bevel line join style
- line join
- drawing [Windows Forms], joining lines
- GraphicsPath object
- round line join style
- lines [Windows Forms], joining
- graphics [Windows Forms], joining lines
ms.assetid: 9fc480c2-3c75-4fd1-8ab5-296a99e820e2
ms.openlocfilehash: 362ce0c701d6e5f640fecd143a60cf471045629c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976156"
---
# <a name="how-to-join-lines"></a><span data-ttu-id="2da65-102">Vorgehensweise: Verknüpfen von Linien</span><span class="sxs-lookup"><span data-stu-id="2da65-102">How to: Join Lines</span></span>
<span data-ttu-id="2da65-103">Ein Zeilen Beitritt ist der gemeinsame Bereich, der durch zwei Zeilen gebildet wird, deren enden sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="2da65-103">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="2da65-104">GDI+ bietet drei zeilige joinstile: Miter, Abschrägung und Round.</span><span class="sxs-lookup"><span data-stu-id="2da65-104">GDI+ provides three line join styles: miter, bevel, and round.</span></span> <span data-ttu-id="2da65-105">Der linienjoinstil ist eine Eigenschaft der- <xref:System.Drawing.Pen> Klasse.</span><span class="sxs-lookup"><span data-stu-id="2da65-105">Line join style is a property of the <xref:System.Drawing.Pen> class.</span></span> <span data-ttu-id="2da65-106">Wenn Sie einen linienjoinstil für ein- <xref:System.Drawing.Pen> Objekt angeben, wird dieser joinstil auf alle verbundenen Linien in jedem Objekt angewendet, das <xref:System.Drawing.Drawing2D.GraphicsPath> mit diesem Stift gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2da65-106">When you specify a line join style for a <xref:System.Drawing.Pen> object, that join style will be applied to all the connected lines in any <xref:System.Drawing.Drawing2D.GraphicsPath> object drawn using that pen.</span></span>  
  
 <span data-ttu-id="2da65-107">In der folgenden Abbildung sind die Ergebnisse des Beispiels für ein gepuffertes Zeilen Verknüpfungs Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2da65-107">The following illustration shows the results of the beveled line join example.</span></span>  
  
 ![Abbildung, in der joinlinien angezeigt werden.](./media/how-to-join-lines/joined-beveled-lines.gif)  
  
## <a name="example"></a><span data-ttu-id="2da65-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2da65-109">Example</span></span>  
 <span data-ttu-id="2da65-110">Sie können den linienjoinstil mithilfe der- <xref:System.Drawing.Pen.LineJoin%2A> Eigenschaft der- <xref:System.Drawing.Pen> Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="2da65-110">You can specify the line join style by using the <xref:System.Drawing.Pen.LineJoin%2A> property of the <xref:System.Drawing.Pen> class.</span></span> <span data-ttu-id="2da65-111">Das Beispiel veranschaulicht einen gevelten Zeilen Beitritt zwischen einer horizontalen Linie und einer vertikalen Linie.</span><span class="sxs-lookup"><span data-stu-id="2da65-111">The example demonstrates a beveled line join between a horizontal line and a vertical line.</span></span> <span data-ttu-id="2da65-112">Im folgenden Code ist der Wert, der <xref:System.Drawing.Drawing2D.LineJoin.Bevel> der- <xref:System.Drawing.Pen.LineJoin%2A> Eigenschaft zugewiesen ist, ein Member der- <xref:System.Drawing.Drawing2D.LineJoin> Enumeration.</span><span class="sxs-lookup"><span data-stu-id="2da65-112">In the following code, the value <xref:System.Drawing.Drawing2D.LineJoin.Bevel> assigned to the <xref:System.Drawing.Pen.LineJoin%2A> property is a member of the <xref:System.Drawing.Drawing2D.LineJoin> enumeration.</span></span> <span data-ttu-id="2da65-113">Die anderen Member der <xref:System.Drawing.Drawing2D.LineJoin> -Enumeration sind <xref:System.Drawing.Drawing2D.LineJoin.Miter> und <xref:System.Drawing.Drawing2D.LineJoin.Round> .</span><span class="sxs-lookup"><span data-stu-id="2da65-113">The other members of the <xref:System.Drawing.Drawing2D.LineJoin> enumeration are <xref:System.Drawing.Drawing2D.LineJoin.Miter> and <xref:System.Drawing.Drawing2D.LineJoin.Round>.</span></span>  
  
 [!code-csharp[System.Drawing.UsingAPen#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingAPen#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2da65-114">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="2da65-114">Compiling the Code</span></span>  
 <span data-ttu-id="2da65-115">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="2da65-115">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2da65-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2da65-116">See also</span></span>

- [<span data-ttu-id="2da65-117">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="2da65-117">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
