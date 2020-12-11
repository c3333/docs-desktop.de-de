---
title: Struktur der grafischen Oberfläche
ms.date: 03/30/2017
helpviewer_keywords:
- GDI+, using managed interface
- graphics [Windows Forms], class structure
ms.assetid: 010a1e46-656b-40a1-8d5d-87aa05ee1243
ms.openlocfilehash: d3b16249b6bae4a113661f5a3a47097046ba20f1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975250"
---
# <a name="structure-of-the-graphics-interface"></a>Struktur der grafischen Oberfläche
Die verwaltete Klassen Schnittstelle zu GDI+ enthält ungefähr 60 Klassen, 50 Enumerationen und 8 Strukturen. Die- <xref:System.Drawing.Graphics> Klasse ist der Kern der GDI+-Funktionalität. Sie ist die Klasse, die tatsächlich Linien, Kurven, Abbildungen, Bilder und Text zeichnet.  
  
## <a name="important-classes"></a>Wichtige Klassen  
 Viele Klassenarbeiten zusammen mit der- <xref:System.Drawing.Graphics> Klasse. Die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode empfängt z. b <xref:System.Drawing.Pen> . ein-Objekt, das Attribute (Farbe, Breite, Bindestrich und ähnliches) der Linie enthält, die gezeichnet werden soll. Die- <xref:System.Drawing.Graphics.FillRectangle%2A> Methode kann einen Zeiger auf ein- <xref:System.Drawing.Drawing2D.LinearGradientBrush> Objekt erhalten, das mit dem-Objekt verwendet wird, <xref:System.Drawing.Graphics> um ein Rechteck mit einer allmählich veränderlichen Farbe auszufüllen. <xref:System.Drawing.Font> -und- <xref:System.Drawing.StringFormat> Objekte beeinflussen die Methode, mit der ein- <xref:System.Drawing.Graphics> Objekt Text zeichnet Ein <xref:System.Drawing.Drawing2D.Matrix> -Objekt speichert und manipuliert die weltweite Transformation eines- <xref:System.Drawing.Graphics> Objekts, das zum drehen, skalieren und Kippen von Bildern verwendet wird.  
  
 GDI+ stellt mehrere Strukturen (z. b <xref:System.Drawing.Rectangle> <xref:System.Drawing.Point> ., und <xref:System.Drawing.Size> ) zum Organisieren von Grafikdaten bereit. Außerdem dienen bestimmte Klassen primär als strukturierte Datentypen. Beispielsweise ist die <xref:System.Drawing.Imaging.BitmapData> -Klasse ein Hilfsobjekt für die <xref:System.Drawing.Bitmap> -Klasse, und die-Klasse <xref:System.Drawing.Drawing2D.PathData> ist ein Hilfsprogramm für die- <xref:System.Drawing.Drawing2D.GraphicsPath> Klasse.  
  
 GDI+ definiert mehrere Enumerationen, bei denen es sich um Auflistungen verwandter Konstanten handelt. Die <xref:System.Drawing.Drawing2D.LineJoin> -Enumeration enthält z. b. die Elemente, <xref:System.Drawing.Drawing2D.LineJoin.Bevel> <xref:System.Drawing.Drawing2D.LineJoin.Miter> und <xref:System.Drawing.Drawing2D.LineJoin.Round> , mit denen Stile angegeben werden, die zum Verknüpfen von zwei Zeilen verwendet werden können.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Grafiken](graphics-overview-windows-forms.md)
- [Verwalteter Code in GDI+](about-gdi-managed-code.md)
- [Verwenden von verwalteten Grafikklassen](using-managed-graphics-classes.md)
