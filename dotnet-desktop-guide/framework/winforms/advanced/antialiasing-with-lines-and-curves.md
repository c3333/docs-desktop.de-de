---
title: Antialiasing bei Linien und Kurven
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- antialiasing
- antialiasing [Windows Forms], smoothing modes
- GDI+, antialiasing
ms.assetid: 810da1a4-c136-4abf-88df-68e49efdd8d4
ms.openlocfilehash: 871c5cb3cd9356f677633acb04fe82021a9787c5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974899"
---
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="9ae6e-102">Antialiasing bei Linien und Kurven</span><span class="sxs-lookup"><span data-stu-id="9ae6e-102">Antialiasing with Lines and Curves</span></span>
<span data-ttu-id="9ae6e-103">Wenn Sie GDI+ zum Zeichnen einer Linie verwenden, geben Sie den Ausgangspunkt und den Endpunkt der Zeile an, aber Sie müssen keine Informationen über die einzelnen Pixel in der Zeile angeben.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-103">When you use GDI+ to draw a line, you provide the starting point and ending point of the line, but you do not have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="9ae6e-104">GDI+ funktioniert in Verbindung mit der Anzeigetreiber Software, um zu bestimmen, welche Pixel eingeschaltet werden, um die Zeile auf einem bestimmten Anzeigegerät anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-104">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>  
  
## <a name="aliasing"></a><span data-ttu-id="9ae6e-105">Aliase</span><span class="sxs-lookup"><span data-stu-id="9ae6e-105">Aliasing</span></span>  
 <span data-ttu-id="9ae6e-106">Angenommen, die gerade rote Linie wechselt vom Punkt (4, 2) bis zum Punkt (16, 10).</span><span class="sxs-lookup"><span data-stu-id="9ae6e-106">Consider the straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="9ae6e-107">Angenommen, das Koordinatensystem hat seinen Ursprung in der oberen linken Ecke, und die Maßeinheit ist das Pixel.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="9ae6e-108">Nehmen Sie auch an, dass die x-Achse nach rechts und die y-Achse nach unten zeigt.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="9ae6e-109">Die folgende Abbildung zeigt eine vergrößerte Ansicht der roten Linie, die auf einem mehrfarbigen Hintergrund gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>  
  
 <span data-ttu-id="9ae6e-110">![Linie ohne Antialiasing](./media/aboutgdip02-art33.gif "AboutGdip02_Art33")</span><span class="sxs-lookup"><span data-stu-id="9ae6e-110">![Line, no antialiasing](./media/aboutgdip02-art33.gif "AboutGdip02_Art33")</span></span>  
  
 <span data-ttu-id="9ae6e-111">Die zum Rendering der Linie verwendeten roten Pixel sind nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-111">The red pixels used to render the line are opaque.</span></span> <span data-ttu-id="9ae6e-112">Es gibt keine teilweise transparenten Pixel in der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-112">There are no partially transparent pixels in the line.</span></span> <span data-ttu-id="9ae6e-113">Diese Art von Zeilen Rendering gibt der Linie eine verzweigte Darstellung, und die Linie sieht in etwa wie eine Treppe aus.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-113">This type of line rendering gives the line a jagged appearance, and the line looks somewhat like a staircase.</span></span> <span data-ttu-id="9ae6e-114">Diese Methode zum Darstellen einer Linie mit einer Treppe wird als Aliasing bezeichnet. die Treppe ist ein Alias für die theoretische Zeile.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>  
  
## <a name="antialiasing"></a><span data-ttu-id="9ae6e-115">Antialiasing</span><span class="sxs-lookup"><span data-stu-id="9ae6e-115">Antialiasing</span></span>  
 <span data-ttu-id="9ae6e-116">Ein anspruchsvolleres Verfahren zum Rendern einer Linie besteht darin, teilweise transparente Pixel zusammen mit nicht transparenten Pixeln zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-116">A more sophisticated technique for rendering a line involves using partially transparent pixels along with opaque pixels.</span></span> <span data-ttu-id="9ae6e-117">Pixel sind auf rein rot oder auf eine Mischung aus roter und der Hintergrundfarbe festgelegt, je nachdem, wie nah Sie auf die Linie sind.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-117">Pixels are set to pure red, or to some blend of red and the background color, depending on how close they are to the line.</span></span> <span data-ttu-id="9ae6e-118">Diese Art des Renderings wird als Antialiasing bezeichnet und führt zu einer Zeile, die das menschliche Auge als nahtloser ansieht.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-118">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="9ae6e-119">In der folgenden Abbildung wird gezeigt, wie bestimmte Pixel mit dem Hintergrund kombiniert werden, um eine Zeile mit einem-oder-Alias zu bilden.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-119">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>  
  
 <span data-ttu-id="9ae6e-120">![Antialiasing bei einer Linie](./media/aboutgdip02-art34.gif "AboutGdip02_Art34")</span><span class="sxs-lookup"><span data-stu-id="9ae6e-120">![Antialiasing a Line](./media/aboutgdip02-art34.gif "AboutGdip02_Art34")</span></span>  
  
 <span data-ttu-id="9ae6e-121">Antialiasing, auch als Glättung bezeichnet, kann auch auf Kurven angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-121">Antialiasing, also called smoothing, can also be applied to curves.</span></span> <span data-ttu-id="9ae6e-122">Die folgende Abbildung zeigt eine vergrößerte Ansicht einer gegläten Ellipse.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-122">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>  
  
 <span data-ttu-id="9ae6e-123">![Antialiasing bei Kurven](./media/aboutgdip02-art35.gif "AboutGdip02_Art35")</span><span class="sxs-lookup"><span data-stu-id="9ae6e-123">![Antialiasing Curves](./media/aboutgdip02-art35.gif "AboutGdip02_Art35")</span></span>  
  
 <span data-ttu-id="9ae6e-124">In der folgenden Abbildung wird die gleiche Ellipse in der tatsächlichen Größe angezeigt, einmal ohne Antialiasing und einmal mit Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="9ae6e-124">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>  
  
 <span data-ttu-id="9ae6e-125">![Antialiasingbeispiel](./media/aboutgdip02-art36.gif "AboutGdip02_Art36")</span><span class="sxs-lookup"><span data-stu-id="9ae6e-125">![Antialiasing example](./media/aboutgdip02-art36.gif "AboutGdip02_Art36")</span></span>  
  
 <span data-ttu-id="9ae6e-126">Zum Zeichnen von Linien und Kurven, die Antialiasing verwenden, erstellen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse, und legen Sie die zugehörige- <xref:System.Drawing.Graphics.SmoothingMode%2A> Eigenschaft auf <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> oder fest <xref:System.Drawing.Drawing2D.SmoothingMode.HighQuality> .</span><span class="sxs-lookup"><span data-stu-id="9ae6e-126">To draw lines and curves that use antialiasing, create an instance of the <xref:System.Drawing.Graphics> class and set its <xref:System.Drawing.Graphics.SmoothingMode%2A> property to <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> or <xref:System.Drawing.Drawing2D.SmoothingMode.HighQuality>.</span></span> <span data-ttu-id="9ae6e-127">Anschließend wird eine der Zeichnungs Methoden der gleichen Klasse aufgerufen <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="9ae6e-127">Then call one of the drawing methods of that same <xref:System.Drawing.Graphics> class.</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#81](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#81)]
 [!code-vb[LinesCurvesAndShapes#81](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#81)]  
  
## <a name="see-also"></a><span data-ttu-id="9ae6e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ae6e-128">See also</span></span>

- <xref:System.Drawing.Drawing2D.SmoothingMode?displayProperty=nameWithType>
- [<span data-ttu-id="9ae6e-129">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="9ae6e-129">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="9ae6e-130">Vorgehensweise: Verwenden der Bildkantenglättung mit Text</span><span class="sxs-lookup"><span data-stu-id="9ae6e-130">How to: Use Antialiasing with Text</span></span>](how-to-use-antialiasing-with-text.md)
