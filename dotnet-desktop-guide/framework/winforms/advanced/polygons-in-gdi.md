---
title: Polygone in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- polygons
- drawing [Windows Forms], polygons
- GDI+, polygons
ms.assetid: a72213d2-d69a-4c2b-a75c-be7b20390c13
ms.openlocfilehash: 2b1e3d387e4d056d9187c54dcef560544206c370
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975253"
---
# <a name="polygons-in-gdi"></a><span data-ttu-id="330c8-102">Polygone in GDI+</span><span class="sxs-lookup"><span data-stu-id="330c8-102">Polygons in GDI+</span></span>
<span data-ttu-id="330c8-103">Ein Polygon ist eine geschlossene Form mit drei oder mehr geraden Seiten.</span><span class="sxs-lookup"><span data-stu-id="330c8-103">A polygon is a closed shape with three or more straight sides.</span></span> <span data-ttu-id="330c8-104">Ein Dreieck ist beispielsweise ein Polygon mit drei Seiten, ein Rechteck ist ein Polygon mit vier Seiten, und ein Pentagon ist ein Polygon mit fünf Seiten.</span><span class="sxs-lookup"><span data-stu-id="330c8-104">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="330c8-105">Die folgende Abbildung zeigt mehrere Polygone.</span><span class="sxs-lookup"><span data-stu-id="330c8-105">The following illustration shows several polygons.</span></span>  
  
 <span data-ttu-id="330c8-106">![Polygone](./media/aboutgdip02-art07.gif "Aboutgdip02_art07")</span><span class="sxs-lookup"><span data-stu-id="330c8-106">![Polygons](./media/aboutgdip02-art07.gif "Aboutgdip02_art07")</span></span>  
  
## <a name="drawing-a-polygon"></a><span data-ttu-id="330c8-107">Zeichnen eines Polygons</span><span class="sxs-lookup"><span data-stu-id="330c8-107">Drawing a Polygon</span></span>  
 <span data-ttu-id="330c8-108">Zum Zeichnen eines Polygons benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt, ein <xref:System.Drawing.Pen> -Objekt und ein Array von- <xref:System.Drawing.Point> Objekten (oder <xref:System.Drawing.PointF> ).</span><span class="sxs-lookup"><span data-stu-id="330c8-108">To draw a polygon, you need a <xref:System.Drawing.Graphics> object, a <xref:System.Drawing.Pen> object, and an array of <xref:System.Drawing.Point> (or <xref:System.Drawing.PointF>) objects.</span></span> <span data-ttu-id="330c8-109">Das- <xref:System.Drawing.Graphics> Objekt stellt die- <xref:System.Drawing.Graphics.DrawPolygon%2A> Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="330c8-109">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawPolygon%2A> method.</span></span> <span data-ttu-id="330c8-110">Das <xref:System.Drawing.Pen> Objekt speichert Attribute, z. b. "width" und "Color", der zum Rendering des Polygons verwendeten Zeile, und das Array von- <xref:System.Drawing.Point> Objekten speichert die Punkte, die durch gerade Linien verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="330c8-110">The <xref:System.Drawing.Pen> object stores attributes, such as width and color, of the line used to render the polygon, and the array of <xref:System.Drawing.Point> objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="330c8-111">Das <xref:System.Drawing.Pen> -Objekt und das Array von- <xref:System.Drawing.Point> Objekten werden als Argumente an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawPolygon%2A> .</span><span class="sxs-lookup"><span data-stu-id="330c8-111">The <xref:System.Drawing.Pen> object and the array of <xref:System.Drawing.Point> objects are passed as arguments to the <xref:System.Drawing.Graphics.DrawPolygon%2A> method.</span></span> <span data-ttu-id="330c8-112">Im folgenden Beispiel wird ein dreiseitiges Polygon gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="330c8-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="330c8-113">Beachten Sie, dass es nur drei Punkte in gibt `myPointArray` : (0,0), (50, 30) und (30, 60).</span><span class="sxs-lookup"><span data-stu-id="330c8-113">Note that there are only three points in `myPointArray`: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="330c8-114">Die- <xref:System.Drawing.Graphics.DrawPolygon%2A> Methode schließt das Polygon automatisch durch Zeichnen einer Linie von (30, 60) zurück zum Startpunkt (0,0).</span><span class="sxs-lookup"><span data-stu-id="330c8-114">The <xref:System.Drawing.Graphics.DrawPolygon%2A> method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0).</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#111](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#111)]
 [!code-vb[LinesCurvesAndShapes#111](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#111)]  
  
 <span data-ttu-id="330c8-115">Die folgende Abbildung zeigt das Polygon.</span><span class="sxs-lookup"><span data-stu-id="330c8-115">The following illustration shows the polygon.</span></span>  
  
 <span data-ttu-id="330c8-116">![Polygon](./media/aboutgdip02-art08.gif "Aboutgdip02_art08")</span><span class="sxs-lookup"><span data-stu-id="330c8-116">![Polygon](./media/aboutgdip02-art08.gif "Aboutgdip02_art08")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="330c8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="330c8-117">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [<span data-ttu-id="330c8-118">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="330c8-118">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="330c8-119">Vorgehensweise: Erstellen eines Stifts</span><span class="sxs-lookup"><span data-stu-id="330c8-119">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
