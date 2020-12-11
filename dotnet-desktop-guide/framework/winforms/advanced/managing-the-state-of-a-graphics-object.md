---
title: Verwalten des Zustands eines Graphics-Objekts
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], managing state
- graphics [Windows Forms], clipping
ms.assetid: 6207cad1-7a34-4bd6-bfc1-db823ca7a73e
ms.openlocfilehash: d1e7e6eac775ca779fb68605adcc9bc2b9915e49
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975841"
---
# <a name="managing-the-state-of-a-graphics-object"></a><span data-ttu-id="26674-102">Verwalten des Zustands eines Graphics-Objekts</span><span class="sxs-lookup"><span data-stu-id="26674-102">Managing the State of a Graphics Object</span></span>
<span data-ttu-id="26674-103">Die <xref:System.Drawing.Graphics> Klasse ist das Herzstück von GDI+.</span><span class="sxs-lookup"><span data-stu-id="26674-103">The <xref:System.Drawing.Graphics> class is at the heart of GDI+.</span></span> <span data-ttu-id="26674-104">Um etwas zu zeichnen, rufen Sie ein- <xref:System.Drawing.Graphics> Objekt ab, legen seine Eigenschaften fest und rufen die zugehörigen Methoden <xref:System.Drawing.Graphics.DrawLine%2A> , <xref:System.Drawing.Graphics.DrawImage%2A> , <xref:System.Drawing.Graphics.DrawString%2A> und auf.</span><span class="sxs-lookup"><span data-stu-id="26674-104">To draw anything, you obtain a <xref:System.Drawing.Graphics> object, set its properties, and call its methods <xref:System.Drawing.Graphics.DrawLine%2A>, <xref:System.Drawing.Graphics.DrawImage%2A>, <xref:System.Drawing.Graphics.DrawString%2A>, and the like).</span></span>  
  
 <span data-ttu-id="26674-105">Im folgenden Beispiel wird die- <xref:System.Drawing.Graphics.DrawRectangle%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="26674-105">The following example calls the <xref:System.Drawing.Graphics.DrawRectangle%2A> method of a <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="26674-106">Das erste an die-Methode über gegebene Argument <xref:System.Drawing.Graphics.DrawRectangle%2A> ist ein- <xref:System.Drawing.Pen> Objekt.</span><span class="sxs-lookup"><span data-stu-id="26674-106">The first argument passed to the <xref:System.Drawing.Graphics.DrawRectangle%2A> method is a <xref:System.Drawing.Pen> object.</span></span>  
  
```vb  
Dim graphics As Graphics = e.Graphics  
Dim pen As New Pen(Color.Blue) ' Opaque blue  
graphics.DrawRectangle(pen, 10, 10, 200, 100)  
```  
  
```csharp  
Graphics graphics = e.Graphics;  
Pen pen = new Pen(Color.Blue);  // Opaque blue  
graphics.DrawRectangle(pen, 10, 10, 200, 100);  
```  
  
## <a name="graphics-state"></a><span data-ttu-id="26674-107">Grafikzustand</span><span class="sxs-lookup"><span data-stu-id="26674-107">Graphics State</span></span>  
 <span data-ttu-id="26674-108">Ein <xref:System.Drawing.Graphics> -Objekt bietet mehr als Zeichnungs Methoden, z <xref:System.Drawing.Graphics.DrawLine%2A> . b <xref:System.Drawing.Graphics.DrawRectangle%2A> . und.</span><span class="sxs-lookup"><span data-stu-id="26674-108">A <xref:System.Drawing.Graphics> object does more than provide drawing methods, such as <xref:System.Drawing.Graphics.DrawLine%2A> and <xref:System.Drawing.Graphics.DrawRectangle%2A>.</span></span> <span data-ttu-id="26674-109">Ein- <xref:System.Drawing.Graphics> Objekt verwaltet auch den Grafik Zustand, der in die folgenden Kategorien unterteilt werden kann:</span><span class="sxs-lookup"><span data-stu-id="26674-109">A <xref:System.Drawing.Graphics> object also maintains graphics state, which can be divided into the following categories:</span></span>  
  
- <span data-ttu-id="26674-110">Qualitätseinstellungen</span><span class="sxs-lookup"><span data-stu-id="26674-110">Quality settings</span></span>  
  
- <span data-ttu-id="26674-111">Transformationen</span><span class="sxs-lookup"><span data-stu-id="26674-111">Transformations</span></span>  
  
- <span data-ttu-id="26674-112">Clippingbereich</span><span class="sxs-lookup"><span data-stu-id="26674-112">Clipping region</span></span>  
  
### <a name="quality-settings"></a><span data-ttu-id="26674-113">Qualitätseinstellungen</span><span class="sxs-lookup"><span data-stu-id="26674-113">Quality Settings</span></span>  
 <span data-ttu-id="26674-114">Ein- <xref:System.Drawing.Graphics> Objekt verfügt über mehrere Eigenschaften, die die Qualität der Elemente beeinflussen, die gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="26674-114">A <xref:System.Drawing.Graphics> object has several properties that influence the quality of the items that are drawn.</span></span> <span data-ttu-id="26674-115">Beispielsweise können Sie die-Eigenschaft festlegen, <xref:System.Drawing.Graphics.TextRenderingHint%2A> um den Typ des Antialiasing (sofern vorhanden) anzugeben, der auf Text angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="26674-115">For example, you can set the <xref:System.Drawing.Graphics.TextRenderingHint%2A> property to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="26674-116">Andere Eigenschaften, die die Qualität beeinflussen, sind <xref:System.Drawing.Graphics.SmoothingMode%2A> , <xref:System.Drawing.Graphics.CompositingMode%2A> , <xref:System.Drawing.Graphics.CompositingQuality%2A> und <xref:System.Drawing.Graphics.InterpolationMode%2A> .</span><span class="sxs-lookup"><span data-stu-id="26674-116">Other properties that influence quality are <xref:System.Drawing.Graphics.SmoothingMode%2A>, <xref:System.Drawing.Graphics.CompositingMode%2A>, <xref:System.Drawing.Graphics.CompositingQuality%2A>, and <xref:System.Drawing.Graphics.InterpolationMode%2A>.</span></span>  
  
 <span data-ttu-id="26674-117">Im folgenden Beispiel werden zwei Ellipsen gezeichnet, von denen eine mit dem Glättungs Modus auf <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> und eine mit dem Glättungs Modus auf festgelegt ist <xref:System.Drawing.Drawing2D.SmoothingMode.HighSpeed> :</span><span class="sxs-lookup"><span data-stu-id="26674-117">The following example draws two ellipses, one with the smoothing mode set to <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> and one with the smoothing mode set to <xref:System.Drawing.Drawing2D.SmoothingMode.HighSpeed>:</span></span>  
  
```vb  
Dim graphics As Graphics = e.Graphics  
Dim pen As New Pen(Color.Blue)  
  
graphics.SmoothingMode = SmoothingMode.AntiAlias  
graphics.DrawEllipse(pen, 0, 0, 200, 100)  
graphics.SmoothingMode = SmoothingMode.HighSpeed  
graphics.DrawEllipse(pen, 0, 150, 200, 100)  
```  
  
```csharp  
Graphics graphics = e.Graphics;  
Pen pen = new Pen(Color.Blue);  
  
graphics.SmoothingMode = SmoothingMode.AntiAlias;  
graphics.DrawEllipse(pen, 0, 0, 200, 100);  
graphics.SmoothingMode = SmoothingMode.HighSpeed;  
graphics.DrawEllipse(pen, 0, 150, 200, 100);  
```  
  
### <a name="transformations"></a><span data-ttu-id="26674-118">Transformationen</span><span class="sxs-lookup"><span data-stu-id="26674-118">Transformations</span></span>  
 <span data-ttu-id="26674-119">Ein- <xref:System.Drawing.Graphics> Objekt verwaltet zwei Transformationen (Welt und Seite), die auf alle Elemente angewendet werden, die von diesem Objekt gezeichnet werden <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="26674-119">A <xref:System.Drawing.Graphics> object maintains two transformations (world and page) that are applied to all items drawn by that <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="26674-120">Jede affine Transformation kann in der Welt Transformation gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="26674-120">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="26674-121">Affine Transformationen umfassen Skalierung, Rotation, Spiegelung, Neigung und Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="26674-121">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="26674-122">Die Seiten Transformation kann für die Skalierung und für das Ändern von Einheiten (z. b. Pixel in Zoll) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26674-122">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="26674-123">Weitere Informationen finden Sie unter [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="26674-123">For more information, see [Coordinate Systems and Transformations](coordinate-systems-and-transformations.md).</span></span>  
  
 <span data-ttu-id="26674-124">Im folgenden Beispiel werden die Welt-und Seiten Transformationen eines-Objekts festgelegt <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="26674-124">The following example sets the world and page transformations of a <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="26674-125">Die Welt Transformation ist auf eine 30-Grad-Drehung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26674-125">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="26674-126">Die Seite Transformation wird so festgelegt, dass die an die zweite Zeile über gegebenen Koordinaten <xref:System.Drawing.Graphics.DrawEllipse%2A> als Millimeter anstelle von Pixel behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="26674-126">The page transformation is set so that the coordinates passed to the second <xref:System.Drawing.Graphics.DrawEllipse%2A> will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="26674-127">Der Code führt zwei identische Aufrufe an die- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode aus.</span><span class="sxs-lookup"><span data-stu-id="26674-127">The code makes two identical calls to the <xref:System.Drawing.Graphics.DrawEllipse%2A> method.</span></span> <span data-ttu-id="26674-128">Die Welt Transformation wird auf den ersten-Befehl angewendet <xref:System.Drawing.Graphics.DrawEllipse%2A> , und beide Transformationen (Welt und Seite) werden auf den zweiten-Befehl angewendet <xref:System.Drawing.Graphics.DrawEllipse%2A> .</span><span class="sxs-lookup"><span data-stu-id="26674-128">The world transformation is applied to the first <xref:System.Drawing.Graphics.DrawEllipse%2A> call, and both transformations (world and page) are applied to the second <xref:System.Drawing.Graphics.DrawEllipse%2A> call.</span></span>  
  
```vb  
Dim graphics As Graphics = e.Graphics  
Dim pen As New Pen(Color.Red)  
  
graphics.ResetTransform()  
graphics.RotateTransform(30) ' world transformation  
graphics.DrawEllipse(pen, 0, 0, 100, 50)  
graphics.PageUnit = GraphicsUnit.Millimeter ' page transformation  
graphics.DrawEllipse(pen, 0, 0, 100, 50)  
```  
  
```csharp  
Graphics graphics = e.Graphics;  
Pen pen = new Pen(Color.Red);
  
graphics.ResetTransform();  
graphics.RotateTransform(30);                    // world transformation  
graphics.DrawEllipse(pen, 0, 0, 100, 50);  
graphics.PageUnit = GraphicsUnit.Millimeter;     // page transformation  
graphics.DrawEllipse(pen, 0, 0, 100, 50);  
```  
  
 <span data-ttu-id="26674-129">Die folgende Abbildung zeigt die beiden Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="26674-129">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="26674-130">Beachten Sie, dass die 30-Grad-Drehung über den Ursprung des Koordinatensystems (obere linke Ecke des Client Bereichs) und nicht über die Mittelpunkte der Ellipsen liegt.</span><span class="sxs-lookup"><span data-stu-id="26674-130">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="26674-131">Beachten Sie außerdem, dass die Stift Breite 1 für die erste Ellipse 1 Pixel und für die zweite Ellipse 1 Millimeter bedeutet.</span><span class="sxs-lookup"><span data-stu-id="26674-131">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>  
  
 ![Abbildung, die zwei Ellipsen anzeigt: Drehung und Stift Breite.](./media/managing-the-state-of-a-graphics-object/set-rotation-pen-width-drawellipse-method.png)  
  
### <a name="clipping-region"></a><span data-ttu-id="26674-133">Clippingbereich</span><span class="sxs-lookup"><span data-stu-id="26674-133">Clipping Region</span></span>  
 <span data-ttu-id="26674-134">Ein- <xref:System.Drawing.Graphics> Objekt verwaltet einen Clippingbereich, der für alle von diesem-Objekt gezeichneten Elemente gilt <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="26674-134">A <xref:System.Drawing.Graphics> object maintains a clipping region that applies to all items drawn by that <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="26674-135">Sie können den Clippingbereich festlegen, indem Sie die- <xref:System.Drawing.Graphics.SetClip%2A> Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="26674-135">You can set the clipping region by calling the <xref:System.Drawing.Graphics.SetClip%2A> method.</span></span>  
  
 <span data-ttu-id="26674-136">Im folgenden Beispiel wird ein Plus förmiger Bereich erstellt, indem die Union von zwei Rechtecke gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="26674-136">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="26674-137">Diese Region wird als Clippingbereich eines-Objekts festgelegt <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="26674-137">That region is designated as the clipping region of a <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="26674-138">Anschließend zeichnet der Code zwei Zeilen, die auf das Innere des Clippingbereichs beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="26674-138">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>  
  
```vb  
Dim graphics As Graphics = e.Graphics  
  
' Opaque red, width 5  
Dim pen As New Pen(Color.Red, 5)  
  
' Opaque aqua  
Dim brush As New SolidBrush(Color.FromArgb(255, 180, 255, 255))  
  
' Create a plus-shaped region by forming the union of two rectangles.  
Dim [region] As New [Region](New Rectangle(50, 0, 50, 150))  
[region].Union(New Rectangle(0, 50, 150, 50))  
graphics.FillRegion(brush, [region])  
  
' Set the clipping region.  
graphics.SetClip([region], CombineMode.Replace)  
  
' Draw two clipped lines.  
graphics.DrawLine(pen, 0, 30, 150, 160)  
graphics.DrawLine(pen, 40, 20, 190, 150)  
```  
  
```csharp  
Graphics graphics = e.Graphics;  
  
// Opaque red, width 5  
Pen pen = new Pen(Color.Red, 5);
  
// Opaque aqua  
SolidBrush brush = new SolidBrush(Color.FromArgb(255, 180, 255, 255));
  
// Create a plus-shaped region by forming the union of two rectangles.  
Region region = new Region(new Rectangle(50, 0, 50, 150));  
region.Union(new Rectangle(0, 50, 150, 50));  
graphics.FillRegion(brush, region);  
  
// Set the clipping region.  
graphics.SetClip(region, CombineMode.Replace);  
  
// Draw two clipped lines.  
graphics.DrawLine(pen, 0, 30, 150, 160);  
graphics.DrawLine(pen, 40, 20, 190, 150);  
```  
  
 <span data-ttu-id="26674-139">Die folgende Abbildung zeigt die ausgeschnittenen Zeilen:</span><span class="sxs-lookup"><span data-stu-id="26674-139">The following illustration shows the clipped lines:</span></span>  
  
 ![Diagramm, das den begrenzten Clip Bereich anzeigt.](./media/managing-the-state-of-a-graphics-object/set-clipping-region-setclip-method.png)  
  
## <a name="see-also"></a><span data-ttu-id="26674-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26674-141">See also</span></span>

- [<span data-ttu-id="26674-142">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26674-142">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="26674-143">Verwenden geschachtelter Grafikcontainer</span><span class="sxs-lookup"><span data-stu-id="26674-143">Using Nested Graphics Containers</span></span>](using-nested-graphics-containers.md)
