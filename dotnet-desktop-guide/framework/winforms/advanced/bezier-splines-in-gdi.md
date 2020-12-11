---
title: B&#233;Zier-Splines in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines
- splines [Windows Forms], Bezier
- GDI+, Bezier splines
ms.assetid: 5774ce1e-87d4-4bc7-88c4-4862052781b8
ms.openlocfilehash: ff4e9eb18610b70c88e057d3d44020321bbb9f4f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972412"
---
# <a name="b233zier-splines-in-gdi"></a><span data-ttu-id="62533-102">B&#233;Zier-Splines in GDI+</span><span class="sxs-lookup"><span data-stu-id="62533-102">B&#233;zier Splines in GDI+</span></span>
<span data-ttu-id="62533-103">Eine Bézier-Spline ist eine Kurve, die von vier Punkten angegeben wird: zwei Endpunkte (P1 und P2) und zwei Kontrollpunkte (C1 und C2).</span><span class="sxs-lookup"><span data-stu-id="62533-103">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="62533-104">Die Kurve beginnt bei P1 und endet bei P2.</span><span class="sxs-lookup"><span data-stu-id="62533-104">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="62533-105">Die Kurve übergibt nicht die Steuerungs Punkte, aber die Steuerungs Punkte fungieren als Magnete, ziehen die Kurve in bestimmte Richtungen und beeinflussen die Kurven Kurven.</span><span class="sxs-lookup"><span data-stu-id="62533-105">The curve does not pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="62533-106">In der folgenden Abbildung wird eine Bézier-Kurve zusammen mit den zugehörigen Endpunkten und Steuerungs Punkten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="62533-106">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>  
  
 <span data-ttu-id="62533-107">![Bezier-Splines](./media/aboutgdip02-art11a.gif "Aboutgdip02_art11a")</span><span class="sxs-lookup"><span data-stu-id="62533-107">![Bezier Splines](./media/aboutgdip02-art11a.gif "Aboutgdip02_art11a")</span></span>  
  
 <span data-ttu-id="62533-108">Die Kurve beginnt bei P1 und wechselt zur Steuerungspunkt C1.</span><span class="sxs-lookup"><span data-stu-id="62533-108">The curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="62533-109">Die Tangente an der Kurve bei P1 ist die Linie, die von P1 bis C1 gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="62533-109">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="62533-110">Die Tangente-Linie am Endpunkt P2 ist die Linie, die von C2 bis P2 gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="62533-110">The tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>  
  
## <a name="drawing-bzier-splines"></a><span data-ttu-id="62533-111">Zeichnen von Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="62533-111">Drawing Bézier Splines</span></span>  
 <span data-ttu-id="62533-112">Zum Zeichnen eines Bézier-Spline benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse und eine-Klasse <xref:System.Drawing.Pen> .</span><span class="sxs-lookup"><span data-stu-id="62533-112">To draw a Bézier spline, you need an instance of the <xref:System.Drawing.Graphics> class and a <xref:System.Drawing.Pen>.</span></span> <span data-ttu-id="62533-113">Die Instanz der <xref:System.Drawing.Graphics> -Klasse stellt die <xref:System.Drawing.Graphics.DrawBezier%2A> -Methode bereit, und <xref:System.Drawing.Pen> speichert Attribute wie "width" und "Color" der zum Rendering der Kurve verwendeten Zeile.</span><span class="sxs-lookup"><span data-stu-id="62533-113">The instance of the <xref:System.Drawing.Graphics> class provides the <xref:System.Drawing.Graphics.DrawBezier%2A> method, and the <xref:System.Drawing.Pen> stores attributes, such as width and color, of the line used to render the curve.</span></span> <span data-ttu-id="62533-114"><xref:System.Drawing.Pen>Wird als eines der Argumente an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawBezier%2A> .</span><span class="sxs-lookup"><span data-stu-id="62533-114">The <xref:System.Drawing.Pen> is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawBezier%2A> method.</span></span> <span data-ttu-id="62533-115">Die übrigen Argumente, die an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawBezier%2A> werden, sind die Endpunkte und die Steuerungs Punkte.</span><span class="sxs-lookup"><span data-stu-id="62533-115">The remaining arguments passed to the <xref:System.Drawing.Graphics.DrawBezier%2A> method are the endpoints and the control points.</span></span> <span data-ttu-id="62533-116">Im folgenden Beispiel wird eine Bézier-Spline mit einem Startpunkt (0,0), Steuerungs Punkten (40, 20) und (80, 150) und einem Endpunkt (100, 10) gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="62533-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#71](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#71)]
 [!code-vb[LinesCurvesAndShapes#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#71)]  
  
 <span data-ttu-id="62533-117">In der folgenden Abbildung sind die Kurve, die Kontrollpunkte und zwei Tangenten Linien dargestellt.</span><span class="sxs-lookup"><span data-stu-id="62533-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>  
  
 <span data-ttu-id="62533-118">![Bezier-Splines](./media/aboutgdip02-art12.gif "Aboutgdip02_art12")</span><span class="sxs-lookup"><span data-stu-id="62533-118">![Bezier Splines](./media/aboutgdip02-art12.gif "Aboutgdip02_art12")</span></span>  
  
 <span data-ttu-id="62533-119">Die Bézier-Splines wurden ursprünglich von Pierre Bézier zum Entwerfen in der Automobilindustrie entwickelt.</span><span class="sxs-lookup"><span data-stu-id="62533-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="62533-120">Sie haben sich in vielen Arten von computergestütztem Design bewährt und werden auch verwendet, um die Umschriften von Schriftarten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="62533-120">They have since proven to be useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="62533-121">Die Bézier-Splines können eine Vielzahl von Formen ergeben, von denen einige in der folgenden Abbildung dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="62533-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>  
  
 <span data-ttu-id="62533-122">![Paths](./media/aboutgdip02-art13.gif "Aboutgdip02_art13")</span><span class="sxs-lookup"><span data-stu-id="62533-122">![Paths](./media/aboutgdip02-art13.gif "Aboutgdip02_art13")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62533-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62533-123">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [<span data-ttu-id="62533-124">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="62533-124">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="62533-125">Erstellen und Zeichnen von Kurven</span><span class="sxs-lookup"><span data-stu-id="62533-125">Constructing and Drawing Curves</span></span>](constructing-and-drawing-curves.md)
- [<span data-ttu-id="62533-126">Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="62533-126">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="62533-127">Vorgehensweise: Erstellen eines Stifts</span><span class="sxs-lookup"><span data-stu-id="62533-127">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
