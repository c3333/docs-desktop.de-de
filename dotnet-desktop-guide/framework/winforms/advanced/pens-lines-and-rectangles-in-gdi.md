---
title: Stifte, Linien und Rechtecke in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines
- GDI+, lines
- drawing [Windows Forms], rectangles
- rectangles
- drawing [Windows Forms], lines
- GDI+, pens
- examples [Windows Forms], drawing lines and shapes
- examples [Windows Forms], pens
- GDI+, rectangles
- examples [Windows Forms], GDI+
- lines [Windows Forms], dashed
ms.assetid: 30b25aae-e3eb-4479-bdb8-187cf651fc84
ms.openlocfilehash: 06d2351ffa7d7f009d7b049f4689df7038b4d202
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976071"
---
# <a name="pens-lines-and-rectangles-in-gdi"></a><span data-ttu-id="756c0-102">Stifte, Linien und Rechtecke in GDI+</span><span class="sxs-lookup"><span data-stu-id="756c0-102">Pens, Lines, and Rectangles in GDI+</span></span>
<span data-ttu-id="756c0-103">Zum Zeichnen von Linien mit GDI+ müssen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="756c0-103">To draw lines with GDI+ you need to create a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="756c0-104">Das <xref:System.Drawing.Graphics> -Objekt stellt die Methoden bereit, die die Zeichnung tatsächlich ausführen, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute, wie z. b. Linien Farbe, Breite und Stil.</span><span class="sxs-lookup"><span data-stu-id="756c0-104">The <xref:System.Drawing.Graphics> object provides the methods that actually do the drawing, and the <xref:System.Drawing.Pen> object stores attributes, such as line color, width, and style.</span></span>  
  
## <a name="drawing-a-line"></a><span data-ttu-id="756c0-105">Zeichnen einer Linie</span><span class="sxs-lookup"><span data-stu-id="756c0-105">Drawing a Line</span></span>  
 <span data-ttu-id="756c0-106">Um eine Linie zu zeichnen, müssen Sie die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode des- <xref:System.Drawing.Graphics> Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="756c0-106">To draw a line, call the <xref:System.Drawing.Graphics.DrawLine%2A> method of the <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="756c0-107">Das- <xref:System.Drawing.Pen> Objekt wird als eines der Argumente an die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="756c0-107">The <xref:System.Drawing.Pen> object is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawLine%2A> method.</span></span> <span data-ttu-id="756c0-108">Im folgenden Beispiel wird eine Linie vom Punkt (4, 2) bis zum Punkt (12, 6) gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="756c0-108">The following example draws a line from the point (4, 2) to the point (12, 6):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#41](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#41)]
 [!code-vb[LinesCurvesAndShapes#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#41)]  
  
 <span data-ttu-id="756c0-109"><xref:System.Drawing.Graphics.DrawLine%2A> ist eine überladene Methode der- <xref:System.Drawing.Graphics> Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="756c0-109"><xref:System.Drawing.Graphics.DrawLine%2A> is an overloaded method of the <xref:System.Drawing.Graphics> class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="756c0-110">Beispielsweise können Sie zwei <xref:System.Drawing.Point> -Objekte erstellen und die- <xref:System.Drawing.Point> Objekte als Argumente an die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode übergeben:</span><span class="sxs-lookup"><span data-stu-id="756c0-110">For example, you can construct two <xref:System.Drawing.Point> objects and pass the <xref:System.Drawing.Point> objects as arguments to the <xref:System.Drawing.Graphics.DrawLine%2A> method:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#42](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#42)]
 [!code-vb[LinesCurvesAndShapes#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#42)]  
  
## <a name="constructing-a-pen"></a><span data-ttu-id="756c0-111">Erstellen eines Stifts</span><span class="sxs-lookup"><span data-stu-id="756c0-111">Constructing a Pen</span></span>  
 <span data-ttu-id="756c0-112">Sie können bestimmte Attribute angeben, wenn Sie ein- <xref:System.Drawing.Pen> Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="756c0-112">You can specify certain attributes when you construct a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="756c0-113">Beispielsweise `Pen` können Sie mit einem Konstruktor Farbe und Breite angeben.</span><span class="sxs-lookup"><span data-stu-id="756c0-113">For example, one `Pen` constructor allows you to specify color and width.</span></span> <span data-ttu-id="756c0-114">Im folgenden Beispiel wird eine blaue Linie der Breite 2 von (0,0) bis (60, 30) gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="756c0-114">The following example draws a blue line of width 2 from (0, 0) to (60, 30):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#43](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#43)]
 [!code-vb[LinesCurvesAndShapes#43](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#43)]  
  
## <a name="dashed-lines-and-line-caps"></a><span data-ttu-id="756c0-115">Gestrichelte Linien und Linien Kappen</span><span class="sxs-lookup"><span data-stu-id="756c0-115">Dashed Lines and Line Caps</span></span>  
 <span data-ttu-id="756c0-116">Das- <xref:System.Drawing.Pen> Objekt macht auch Eigenschaften verfügbar, wie z <xref:System.Drawing.Pen.DashStyle%2A> . b., mit denen Sie Features der Zeile angeben können.</span><span class="sxs-lookup"><span data-stu-id="756c0-116">The <xref:System.Drawing.Pen> object also exposes properties, such as <xref:System.Drawing.Pen.DashStyle%2A>, that you can use to specify features of the line.</span></span> <span data-ttu-id="756c0-117">Im folgenden Beispiel wird eine gestrichelte Linie von (100, 50) nach (300, 80) gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="756c0-117">The following example draws a dashed line from (100, 50) to (300, 80):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#44](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#44)]
 [!code-vb[LinesCurvesAndShapes#44](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#44)]  
  
 <span data-ttu-id="756c0-118">Sie können die Eigenschaften des- <xref:System.Drawing.Pen> Objekts verwenden, um viele weitere Attribute der Zeile festzulegen.</span><span class="sxs-lookup"><span data-stu-id="756c0-118">You can use the properties of the <xref:System.Drawing.Pen> object to set many more attributes of the line.</span></span> <span data-ttu-id="756c0-119">Die <xref:System.Drawing.Pen.StartCap%2A> <xref:System.Drawing.Pen.EndCap%2A> Eigenschaften und geben die Darstellung der Zeilenenden an. die enden können flach, quadratisch, gerundet, dreieckig oder eine benutzerdefinierte Form sein.</span><span class="sxs-lookup"><span data-stu-id="756c0-119">The <xref:System.Drawing.Pen.StartCap%2A> and <xref:System.Drawing.Pen.EndCap%2A> properties specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="756c0-120">Mithilfe der- <xref:System.Drawing.Pen.LineJoin%2A> Eigenschaft können Sie angeben, ob verbundene Linien gezippt (mit spitzen Ecken verknüpft), geglättet, gerundet oder abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="756c0-120">The <xref:System.Drawing.Pen.LineJoin%2A> property lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="756c0-121">In der folgenden Abbildung werden Zeilen mit verschiedenen Obergrenzen und joinstilen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="756c0-121">The following illustration shows lines with various cap and join styles.</span></span>  
  
 <span data-ttu-id="756c0-122">![Linien](./media/aboutgdip02-art04.gif "Aboutgdip02_art04")</span><span class="sxs-lookup"><span data-stu-id="756c0-122">![Lines](./media/aboutgdip02-art04.gif "Aboutgdip02_art04")</span></span>  
  
## <a name="drawing-a-rectangle"></a><span data-ttu-id="756c0-123">Zeichnen eines Rechtecks</span><span class="sxs-lookup"><span data-stu-id="756c0-123">Drawing a Rectangle</span></span>  
 <span data-ttu-id="756c0-124">Zeichnungs Rechtecke mit GDI+ ähneln Zeichnungslinien.</span><span class="sxs-lookup"><span data-stu-id="756c0-124">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="756c0-125">Zum Zeichnen eines Rechtecks benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt.</span><span class="sxs-lookup"><span data-stu-id="756c0-125">To draw a rectangle, you need a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="756c0-126">Das <xref:System.Drawing.Graphics> -Objekt stellt eine <xref:System.Drawing.Graphics.DrawRectangle%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute, wie z. b. Linienstärke und Farbe.</span><span class="sxs-lookup"><span data-stu-id="756c0-126">The <xref:System.Drawing.Graphics> object provides a <xref:System.Drawing.Graphics.DrawRectangle%2A> method, and the <xref:System.Drawing.Pen> object stores attributes, such as line width and color.</span></span> <span data-ttu-id="756c0-127">Das- <xref:System.Drawing.Pen> Objekt wird als eines der Argumente an die- <xref:System.Drawing.Graphics.DrawRectangle%2A> Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="756c0-127">The <xref:System.Drawing.Pen> object is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawRectangle%2A> method.</span></span> <span data-ttu-id="756c0-128">Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (100, 50), einer Breite von 80 und einer Höhe von 40 gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="756c0-128">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#45](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#45)]
 [!code-vb[LinesCurvesAndShapes#45](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#45)]  
  
 <span data-ttu-id="756c0-129"><xref:System.Drawing.Graphics.DrawRectangle%2A> ist eine überladene Methode der- <xref:System.Drawing.Graphics> Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="756c0-129"><xref:System.Drawing.Graphics.DrawRectangle%2A> is an overloaded method of the <xref:System.Drawing.Graphics> class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="756c0-130">Beispielsweise können Sie ein <xref:System.Drawing.Rectangle> -Objekt erstellen und das- <xref:System.Drawing.Rectangle> Objekt als Argument an die- <xref:System.Drawing.Graphics.DrawRectangle%2A> Methode übergeben:</span><span class="sxs-lookup"><span data-stu-id="756c0-130">For example, you can construct a <xref:System.Drawing.Rectangle> object and pass the <xref:System.Drawing.Rectangle> object to the <xref:System.Drawing.Graphics.DrawRectangle%2A> method as an argument:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#46](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#46)]
 [!code-vb[LinesCurvesAndShapes#46](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#46)]  
  
 <span data-ttu-id="756c0-131">Ein- <xref:System.Drawing.Rectangle> Objekt verfügt über Methoden und Eigenschaften zum Bearbeiten und Sammeln von Informationen über das Rechteck.</span><span class="sxs-lookup"><span data-stu-id="756c0-131">A <xref:System.Drawing.Rectangle> object has methods and properties for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="756c0-132">Die <xref:System.Drawing.Rectangle.Inflate%2A> -Methode und die- <xref:System.Drawing.Rectangle.Offset%2A> Methode ändern z. b. die Größe und Position des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="756c0-132">For example, the <xref:System.Drawing.Rectangle.Inflate%2A> and <xref:System.Drawing.Rectangle.Offset%2A> methods change the size and position of the rectangle.</span></span> <span data-ttu-id="756c0-133">Die <xref:System.Drawing.Rectangle.IntersectsWith%2A> -Methode gibt Aufschluss darüber, ob das Rechteck ein anderes angegebenes Rechteck überschneidet und <xref:System.Drawing.Rectangle.Contains%2A> ob sich ein angegebener Punkt innerhalb des Rechtecks befindet.</span><span class="sxs-lookup"><span data-stu-id="756c0-133">The <xref:System.Drawing.Rectangle.IntersectsWith%2A> method tells you whether the rectangle intersects another given rectangle, and the <xref:System.Drawing.Rectangle.Contains%2A> method tells you whether a given point is inside the rectangle.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="756c0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="756c0-134">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Rectangle?displayProperty=nameWithType>
- [<span data-ttu-id="756c0-135">Vorgehensweise: Erstellen eines Stifts</span><span class="sxs-lookup"><span data-stu-id="756c0-135">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
- [<span data-ttu-id="756c0-136">Vorgehensweise: Zeichnen einer Linie in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="756c0-136">How to: Draw a Line on a Windows Form</span></span>](how-to-draw-a-line-on-a-windows-form.md)
- [<span data-ttu-id="756c0-137">Vorgehensweise: Zeichnen der Kontur einer Form</span><span class="sxs-lookup"><span data-stu-id="756c0-137">How to: Draw an Outlined Shape</span></span>](how-to-draw-an-outlined-shape.md)
