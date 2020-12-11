---
title: Grafikpfade in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], paths
- GDI+, drawing paths
- paths [Windows Forms], drawing
- drawing [Windows Forms], paths
ms.assetid: a5500dec-666c-41fd-9da3-2169dd89c5eb
ms.openlocfilehash: 8e06032d145eb8c1aaf9bfcd1f205f8c6583634a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972387"
---
# <a name="graphics-paths-in-gdi"></a><span data-ttu-id="9ad86-102">Grafikpfade in GDI+</span><span class="sxs-lookup"><span data-stu-id="9ad86-102">Graphics Paths in GDI+</span></span>
<span data-ttu-id="9ad86-103">Pfade werden gebildet, indem Linien, Rechtecke und einfache Kurven kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9ad86-103">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="9ad86-104">Erinnern Sie sich aus der [Übersicht über Vektorgrafiken](vector-graphics-overview.md) , dass die folgenden grundlegenden Bausteine sich als besonders nützlich für das Zeichnen von Bildern erwiesen haben:</span><span class="sxs-lookup"><span data-stu-id="9ad86-104">Recall from the [Vector Graphics Overview](vector-graphics-overview.md) that the following basic building blocks have proven to be the most useful for drawing pictures:</span></span>  
  
- <span data-ttu-id="9ad86-105">Linien</span><span class="sxs-lookup"><span data-stu-id="9ad86-105">Lines</span></span>  
  
- <span data-ttu-id="9ad86-106">Rechtecke</span><span class="sxs-lookup"><span data-stu-id="9ad86-106">Rectangles</span></span>  
  
- <span data-ttu-id="9ad86-107">Ellipsen</span><span class="sxs-lookup"><span data-stu-id="9ad86-107">Ellipses</span></span>  
  
- <span data-ttu-id="9ad86-108">Bögen</span><span class="sxs-lookup"><span data-stu-id="9ad86-108">Arcs</span></span>  
  
- <span data-ttu-id="9ad86-109">Polygone</span><span class="sxs-lookup"><span data-stu-id="9ad86-109">Polygons</span></span>  
  
- <span data-ttu-id="9ad86-110">Kardinale Splines</span><span class="sxs-lookup"><span data-stu-id="9ad86-110">Cardinal splines</span></span>  
  
- <span data-ttu-id="9ad86-111">Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="9ad86-111">Bézier splines</span></span>  
  
 <span data-ttu-id="9ad86-112">In GDI+ können Sie mit dem- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt eine Sequenz dieser Bausteine in einer einzelnen Einheit erfassen.</span><span class="sxs-lookup"><span data-stu-id="9ad86-112">In GDI+, the <xref:System.Drawing.Drawing2D.GraphicsPath> object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="9ad86-113">Die gesamte Sequenz von Linien, Rechtecke, Polygonen und Kurven kann dann mit einem Rückruf der- <xref:System.Drawing.Graphics.DrawPath%2A> Methode der-Klasse gezeichnet werden <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="9ad86-113">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the <xref:System.Drawing.Graphics.DrawPath%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="9ad86-114">Die folgende Abbildung zeigt einen Pfad, der durch das Kombinieren einer Linie, eines Bogens, eines Bézier-Spline und eines kardinaler Spline erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9ad86-114">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>  
  
 <span data-ttu-id="9ad86-115">![Pfad](./media/aboutgdip02-art14.gif "Aboutgdip02_art14")</span><span class="sxs-lookup"><span data-stu-id="9ad86-115">![Path](./media/aboutgdip02-art14.gif "Aboutgdip02_art14")</span></span>  
  
## <a name="using-a-path"></a><span data-ttu-id="9ad86-116">Verwenden eines Pfads</span><span class="sxs-lookup"><span data-stu-id="9ad86-116">Using a Path</span></span>  
 <span data-ttu-id="9ad86-117">Die <xref:System.Drawing.Drawing2D.GraphicsPath> -Klasse stellt die folgenden Methoden zum Erstellen einer Sequenz von Elementen bereit, die gezeichnet werden sollen: <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangle%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddEllipse%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddPolygon%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> (für Kardinal-Splines) und <xref:System.Drawing.Drawing2D.GraphicsPath.AddBezier%2A> .</span><span class="sxs-lookup"><span data-stu-id="9ad86-117">The <xref:System.Drawing.Drawing2D.GraphicsPath> class provides the following methods for creating a sequence of items to be drawn: <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangle%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddEllipse%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddPolygon%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> (for cardinal splines), and <xref:System.Drawing.Drawing2D.GraphicsPath.AddBezier%2A>.</span></span> <span data-ttu-id="9ad86-118">Jede dieser Methoden ist überladen. Das heißt, jede Methode unterstützt mehrere verschiedene Parameterlisten.</span><span class="sxs-lookup"><span data-stu-id="9ad86-118">Each of these methods is overloaded; that is, each method supports several different parameter lists.</span></span> <span data-ttu-id="9ad86-119">Beispielsweise empfängt eine Variation der- <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> Methode vier ganze Zahlen, und eine andere Variation der- <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> Methode empfängt zwei- <xref:System.Drawing.Point> Objekte.</span><span class="sxs-lookup"><span data-stu-id="9ad86-119">For example, one variation of the <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> method receives four integers, and another variation of the <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> method receives two <xref:System.Drawing.Point> objects.</span></span>  
  
 <span data-ttu-id="9ad86-120">Die Methoden zum Hinzufügen von Linien, Rechtecke und Bézier-Splines zu einem Pfad verfügen über Plural-Begleit Methoden, mit denen dem Pfad in einem einzelnen-Befehl mehrere Elemente hinzugefügt werden: <xref:System.Drawing.Drawing2D.GraphicsPath.AddLines%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangles%2A> und <xref:System.Drawing.Drawing2D.GraphicsPath.AddBeziers%2A> .</span><span class="sxs-lookup"><span data-stu-id="9ad86-120">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: <xref:System.Drawing.Drawing2D.GraphicsPath.AddLines%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangles%2A>, and <xref:System.Drawing.Drawing2D.GraphicsPath.AddBeziers%2A>.</span></span> <span data-ttu-id="9ad86-121">Außerdem verfügen die <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> -Methode und die- <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A> Methode über die-und-Methoden, die <xref:System.Drawing.Drawing2D.GraphicsPath.AddClosedCurve%2A> <xref:System.Drawing.Drawing2D.GraphicsPath.AddPie%2A> dem Pfad eine geschlossene Kurve oder einen Kreis hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ad86-121">Also, the <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> and <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A> methods have companion methods, <xref:System.Drawing.Drawing2D.GraphicsPath.AddClosedCurve%2A> and <xref:System.Drawing.Drawing2D.GraphicsPath.AddPie%2A>, that add a closed curve or pie to the path.</span></span>  
  
 <span data-ttu-id="9ad86-122">Um einen Pfad zu zeichnen, benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt, ein <xref:System.Drawing.Pen> -Objekt und ein- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt.</span><span class="sxs-lookup"><span data-stu-id="9ad86-122">To draw a path, you need a <xref:System.Drawing.Graphics> object, a <xref:System.Drawing.Pen> object, and a <xref:System.Drawing.Drawing2D.GraphicsPath> object.</span></span> <span data-ttu-id="9ad86-123">Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawPath%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute wie "width" und "Color" der zum Rendering des Pfads verwendeten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9ad86-123">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawPath%2A> method, and the <xref:System.Drawing.Pen> object stores attributes, such as width and color, of the line used to render the path.</span></span> <span data-ttu-id="9ad86-124">Das <xref:System.Drawing.Drawing2D.GraphicsPath> -Objekt speichert die Sequenz von Linien und Kurven, die den Pfad bilden.</span><span class="sxs-lookup"><span data-stu-id="9ad86-124">The <xref:System.Drawing.Drawing2D.GraphicsPath> object stores the sequence of lines and curves that make up the path.</span></span> <span data-ttu-id="9ad86-125">Das <xref:System.Drawing.Pen> -Objekt und das- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt werden als Argumente an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawPath%2A> .</span><span class="sxs-lookup"><span data-stu-id="9ad86-125">The <xref:System.Drawing.Pen> object and the <xref:System.Drawing.Drawing2D.GraphicsPath> object are passed as arguments to the <xref:System.Drawing.Graphics.DrawPath%2A> method.</span></span> <span data-ttu-id="9ad86-126">Im folgenden Beispiel wird ein Pfad gezeichnet, der aus einer Zeile, einer Ellipse und einem Bézier-Spline besteht:</span><span class="sxs-lookup"><span data-stu-id="9ad86-126">The following example draws a path that consists of a line, an ellipse, and a Bézier spline:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#101](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#101)]
 [!code-vb[LinesCurvesAndShapes#101](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#101)]  
  
 <span data-ttu-id="9ad86-127">In der folgenden Abbildung ist der Pfad dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9ad86-127">The following illustration shows the path.</span></span>  
  
 <span data-ttu-id="9ad86-128">![Pfad](./media/aboutgdip02-art15.gif "Aboutgdip02_art15")</span><span class="sxs-lookup"><span data-stu-id="9ad86-128">![Path](./media/aboutgdip02-art15.gif "Aboutgdip02_art15")</span></span>  
  
 <span data-ttu-id="9ad86-129">Zusätzlich zum Hinzufügen von Linien, Rechtecke und Kurven zu einem Pfad können Sie Pfade zu einem Pfad hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ad86-129">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="9ad86-130">Dies ermöglicht Ihnen das Kombinieren vorhandener Pfade, um große und komplexe Pfade zu bilden.</span><span class="sxs-lookup"><span data-stu-id="9ad86-130">This allows you to combine existing paths to form large, complex paths.</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#102](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#102)]
 [!code-vb[LinesCurvesAndShapes#102](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#102)]  
  
 <span data-ttu-id="9ad86-131">Es gibt zwei weitere Elemente, die Sie einem Pfad hinzufügen können: Strings und Pies.</span><span class="sxs-lookup"><span data-stu-id="9ad86-131">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="9ad86-132">Ein Kreis ist ein Teil des Inneren einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="9ad86-132">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="9ad86-133">Im folgenden Beispiel wird ein Pfad aus einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis erstellt:</span><span class="sxs-lookup"><span data-stu-id="9ad86-133">The following example creates a path from an arc, a cardinal spline, a string, and a pie:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#103](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#103)]
 [!code-vb[LinesCurvesAndShapes#103](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#103)]  
  
 <span data-ttu-id="9ad86-134">In der folgenden Abbildung ist der Pfad dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9ad86-134">The following illustration shows the path.</span></span> <span data-ttu-id="9ad86-135">Beachten Sie, dass für einen Pfad keine Verbindung hergestellt werden muss. der Bogen, der kardinalspline, die Zeichenfolge und der Kreis werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="9ad86-135">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>  
  
 <span data-ttu-id="9ad86-136">![Paths](./media/aboutgdip02-art16.gif "Aboutgdip02_Art16")</span><span class="sxs-lookup"><span data-stu-id="9ad86-136">![Paths](./media/aboutgdip02-art16.gif "Aboutgdip02_Art16")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ad86-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ad86-137">See also</span></span>

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- <xref:System.Drawing.Point?displayProperty=nameWithType>
- [<span data-ttu-id="9ad86-138">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="9ad86-138">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="9ad86-139">Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="9ad86-139">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="9ad86-140">Erstellen und Zeichnen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="9ad86-140">Constructing and Drawing Paths</span></span>](constructing-and-drawing-paths.md)
