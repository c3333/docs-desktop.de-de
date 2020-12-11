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
# <a name="managing-the-state-of-a-graphics-object"></a>Verwalten des Zustands eines Graphics-Objekts
Die <xref:System.Drawing.Graphics> Klasse ist das Herzstück von GDI+. Um etwas zu zeichnen, rufen Sie ein- <xref:System.Drawing.Graphics> Objekt ab, legen seine Eigenschaften fest und rufen die zugehörigen Methoden <xref:System.Drawing.Graphics.DrawLine%2A> , <xref:System.Drawing.Graphics.DrawImage%2A> , <xref:System.Drawing.Graphics.DrawString%2A> und auf.  
  
 Im folgenden Beispiel wird die- <xref:System.Drawing.Graphics.DrawRectangle%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts aufgerufen. Das erste an die-Methode über gegebene Argument <xref:System.Drawing.Graphics.DrawRectangle%2A> ist ein- <xref:System.Drawing.Pen> Objekt.  
  
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
  
## <a name="graphics-state"></a>Grafikzustand  
 Ein <xref:System.Drawing.Graphics> -Objekt bietet mehr als Zeichnungs Methoden, z <xref:System.Drawing.Graphics.DrawLine%2A> . b <xref:System.Drawing.Graphics.DrawRectangle%2A> . und. Ein- <xref:System.Drawing.Graphics> Objekt verwaltet auch den Grafik Zustand, der in die folgenden Kategorien unterteilt werden kann:  
  
- Qualitätseinstellungen  
  
- Transformationen  
  
- Clippingbereich  
  
### <a name="quality-settings"></a>Qualitätseinstellungen  
 Ein- <xref:System.Drawing.Graphics> Objekt verfügt über mehrere Eigenschaften, die die Qualität der Elemente beeinflussen, die gezeichnet werden. Beispielsweise können Sie die-Eigenschaft festlegen, <xref:System.Drawing.Graphics.TextRenderingHint%2A> um den Typ des Antialiasing (sofern vorhanden) anzugeben, der auf Text angewendet wird. Andere Eigenschaften, die die Qualität beeinflussen, sind <xref:System.Drawing.Graphics.SmoothingMode%2A> , <xref:System.Drawing.Graphics.CompositingMode%2A> , <xref:System.Drawing.Graphics.CompositingQuality%2A> und <xref:System.Drawing.Graphics.InterpolationMode%2A> .  
  
 Im folgenden Beispiel werden zwei Ellipsen gezeichnet, von denen eine mit dem Glättungs Modus auf <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> und eine mit dem Glättungs Modus auf festgelegt ist <xref:System.Drawing.Drawing2D.SmoothingMode.HighSpeed> :  
  
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
  
### <a name="transformations"></a>Transformationen  
 Ein- <xref:System.Drawing.Graphics> Objekt verwaltet zwei Transformationen (Welt und Seite), die auf alle Elemente angewendet werden, die von diesem Objekt gezeichnet werden <xref:System.Drawing.Graphics> . Jede affine Transformation kann in der Welt Transformation gespeichert werden. Affine Transformationen umfassen Skalierung, Rotation, Spiegelung, Neigung und Übersetzung. Die Seiten Transformation kann für die Skalierung und für das Ändern von Einheiten (z. b. Pixel in Zoll) verwendet werden. Weitere Informationen finden Sie unter [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md).  
  
 Im folgenden Beispiel werden die Welt-und Seiten Transformationen eines-Objekts festgelegt <xref:System.Drawing.Graphics> . Die Welt Transformation ist auf eine 30-Grad-Drehung festgelegt. Die Seite Transformation wird so festgelegt, dass die an die zweite Zeile über gegebenen Koordinaten <xref:System.Drawing.Graphics.DrawEllipse%2A> als Millimeter anstelle von Pixel behandelt werden. Der Code führt zwei identische Aufrufe an die- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode aus. Die Welt Transformation wird auf den ersten-Befehl angewendet <xref:System.Drawing.Graphics.DrawEllipse%2A> , und beide Transformationen (Welt und Seite) werden auf den zweiten-Befehl angewendet <xref:System.Drawing.Graphics.DrawEllipse%2A> .  
  
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
  
 Die folgende Abbildung zeigt die beiden Ellipsen. Beachten Sie, dass die 30-Grad-Drehung über den Ursprung des Koordinatensystems (obere linke Ecke des Client Bereichs) und nicht über die Mittelpunkte der Ellipsen liegt. Beachten Sie außerdem, dass die Stift Breite 1 für die erste Ellipse 1 Pixel und für die zweite Ellipse 1 Millimeter bedeutet.  
  
 ![Abbildung, die zwei Ellipsen anzeigt: Drehung und Stift Breite.](./media/managing-the-state-of-a-graphics-object/set-rotation-pen-width-drawellipse-method.png)  
  
### <a name="clipping-region"></a>Clippingbereich  
 Ein- <xref:System.Drawing.Graphics> Objekt verwaltet einen Clippingbereich, der für alle von diesem-Objekt gezeichneten Elemente gilt <xref:System.Drawing.Graphics> . Sie können den Clippingbereich festlegen, indem Sie die- <xref:System.Drawing.Graphics.SetClip%2A> Methode aufrufen.  
  
 Im folgenden Beispiel wird ein Plus förmiger Bereich erstellt, indem die Union von zwei Rechtecke gebildet wird. Diese Region wird als Clippingbereich eines-Objekts festgelegt <xref:System.Drawing.Graphics> . Anschließend zeichnet der Code zwei Zeilen, die auf das Innere des Clippingbereichs beschränkt sind.  
  
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
  
 Die folgende Abbildung zeigt die ausgeschnittenen Zeilen:  
  
 ![Diagramm, das den begrenzten Clip Bereich anzeigt.](./media/managing-the-state-of-a-graphics-object/set-clipping-region-setclip-method.png)  
  
## <a name="see-also"></a>Siehe auch

- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Verwenden geschachtelter Grafikcontainer](using-nested-graphics-containers.md)
