---
title: Ellipsen und Bögen in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- arcs
- GDI+, arcs
- drawing [Windows Forms], ellipses
- GDI+, ellipses
- ellipses
- drawing [Windows Forms], arcs
ms.assetid: 34f35133-a835-4ca4-81f6-0dfedee8b683
ms.openlocfilehash: 8bbc2eda6450128eac55576259880e83f07099ab
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975276"
---
# <a name="ellipses-and-arcs-in-gdi"></a><span data-ttu-id="5c577-102">Ellipsen und Bögen in GDI+</span><span class="sxs-lookup"><span data-stu-id="5c577-102">Ellipses and Arcs in GDI+</span></span>
<span data-ttu-id="5c577-103">Mit der <xref:System.Drawing.Graphics.DrawEllipse%2A> -Methode und der- <xref:System.Drawing.Graphics.DrawArc%2A> Methode der-Klasse können Sie ganz einfach Ellipsen und Bögen zeichnen <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="5c577-103">You can easily draw ellipses and arcs using the <xref:System.Drawing.Graphics.DrawEllipse%2A> and <xref:System.Drawing.Graphics.DrawArc%2A> methods of the <xref:System.Drawing.Graphics> class.</span></span>  
  
## <a name="drawing-an-ellipse"></a><span data-ttu-id="5c577-104">Zeichnen einer Ellipse</span><span class="sxs-lookup"><span data-stu-id="5c577-104">Drawing an Ellipse</span></span>  
 <span data-ttu-id="5c577-105">Zum Zeichnen einer Ellipse benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c577-105">To draw an ellipse, you need a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="5c577-106">Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawEllipse%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute, z. b. "width" und "Color", der zum Rendering der Ellipse verwendeten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5c577-106">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawEllipse%2A> method, and the <xref:System.Drawing.Pen> object stores attributes, such as width and color, of the line used to render the ellipse.</span></span> <span data-ttu-id="5c577-107">Das- <xref:System.Drawing.Pen> Objekt wird als eines der Argumente an die- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5c577-107">The <xref:System.Drawing.Pen> object is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawEllipse%2A> method.</span></span> <span data-ttu-id="5c577-108">Die übrigen Argumente, die an die-Methode übergeben werden, <xref:System.Drawing.Graphics.DrawEllipse%2A> geben das Begrenzungs Rechteck für die Ellipse an.</span><span class="sxs-lookup"><span data-stu-id="5c577-108">The remaining arguments passed to the <xref:System.Drawing.Graphics.DrawEllipse%2A> method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="5c577-109">In der folgenden Abbildung wird eine Ellipse zusammen mit dem umgebenden Rechteck gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c577-109">The following illustration shows an ellipse along with its bounding rectangle.</span></span>  
  
 <span data-ttu-id="5c577-110">![Ellipsen und Bögen](./media/aboutgdip02-art05.gif "Aboutgdip02_art05")</span><span class="sxs-lookup"><span data-stu-id="5c577-110">![Ellipses and arcs](./media/aboutgdip02-art05.gif "Aboutgdip02_art05")</span></span>  
  
 <span data-ttu-id="5c577-111">Im folgenden Beispiel wird eine Ellipse gezeichnet. das umgebende Rechteck hat eine Breite von 80, eine Höhe von 40 und eine linke obere Ecke von (100, 50):</span><span class="sxs-lookup"><span data-stu-id="5c577-111">The following example draws an ellipse; the bounding rectangle has a width of 80, a height of 40, and an upper-left corner of (100, 50):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#51](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#51)]
 [!code-vb[LinesCurvesAndShapes#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#51)]  
  
 <span data-ttu-id="5c577-112"><xref:System.Drawing.Graphics.DrawEllipse%2A> ist eine überladene Methode der- <xref:System.Drawing.Graphics> Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5c577-112"><xref:System.Drawing.Graphics.DrawEllipse%2A> is an overloaded method of the <xref:System.Drawing.Graphics> class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="5c577-113">Beispielsweise können Sie einen erstellen <xref:System.Drawing.Rectangle> und <xref:System.Drawing.Rectangle> an die- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode als Argument übergeben:</span><span class="sxs-lookup"><span data-stu-id="5c577-113">For example, you can construct a <xref:System.Drawing.Rectangle> and pass the <xref:System.Drawing.Rectangle> to the <xref:System.Drawing.Graphics.DrawEllipse%2A> method as an argument:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#52](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#52)]
 [!code-vb[LinesCurvesAndShapes#52](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#52)]  
  
## <a name="drawing-an-arc"></a><span data-ttu-id="5c577-114">Zeichnen eines Bogens</span><span class="sxs-lookup"><span data-stu-id="5c577-114">Drawing an Arc</span></span>  
 <span data-ttu-id="5c577-115">Ein Bogen ist ein Teil einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="5c577-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="5c577-116">Um einen Bogen zu zeichnen, wird die- <xref:System.Drawing.Graphics.DrawArc%2A> Methode der- <xref:System.Drawing.Graphics> Klasse aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5c577-116">To draw an arc, you call the <xref:System.Drawing.Graphics.DrawArc%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="5c577-117">Die Parameter der- <xref:System.Drawing.Graphics.DrawArc%2A> Methode sind identisch mit den Parametern der- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode, mit dem Unterschied, dass <xref:System.Drawing.Graphics.DrawArc%2A> einen Anfangs Winkel und einen Pfeil Winkel erfordert.</span><span class="sxs-lookup"><span data-stu-id="5c577-117">The parameters of the <xref:System.Drawing.Graphics.DrawArc%2A> method are the same as the parameters of the <xref:System.Drawing.Graphics.DrawEllipse%2A> method, except that <xref:System.Drawing.Graphics.DrawArc%2A> requires a starting angle and sweep angle.</span></span> <span data-ttu-id="5c577-118">Im folgenden Beispiel wird ein Bogen mit einem Anfangs Winkel von 30 Grad und einem Mittelpunktswinkel von 180 Grad gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="5c577-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#53](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#53)]
 [!code-vb[LinesCurvesAndShapes#53](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#53)]  
  
 <span data-ttu-id="5c577-119">Die folgende Abbildung zeigt den Bogen, die Ellipse und das umgebende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="5c577-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>  
  
 <span data-ttu-id="5c577-120">![Ellipsen und Bögen](./media/aboutgdip02-art06.gif "Aboutgdip02_art06")</span><span class="sxs-lookup"><span data-stu-id="5c577-120">![Ellipses and arcs](./media/aboutgdip02-art06.gif "Aboutgdip02_art06")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c577-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c577-121">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [<span data-ttu-id="5c577-122">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="5c577-122">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="5c577-123">Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="5c577-123">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="5c577-124">Vorgehensweise: Erstellen eines Stifts</span><span class="sxs-lookup"><span data-stu-id="5c577-124">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
- [<span data-ttu-id="5c577-125">Vorgehensweise: Zeichnen der Kontur einer Form</span><span class="sxs-lookup"><span data-stu-id="5c577-125">How to: Draw an Outlined Shape</span></span>](how-to-draw-an-outlined-shape.md)
