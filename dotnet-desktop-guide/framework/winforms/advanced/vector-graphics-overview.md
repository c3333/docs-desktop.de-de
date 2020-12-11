---
title: Übersicht über Vektorgrafiken
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- inclusive-inclusive endpoints
- coordinate systems
- graphics [Windows Forms], vector graphics
ms.assetid: 0195df81-66be-452d-bb53-5a582ebfdc09
ms.openlocfilehash: 6f405f5ffc67a0cdb13fe83f4dd36b70769a4cd9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975829"
---
# <a name="vector-graphics-overview"></a>Übersicht über Vektorgrafiken
GDI+ zeichnet Linien, Rechtecke und andere Formen in einem Koordinatensystem. Sie können aus einer Vielzahl von Koordinatensystemen auswählen, aber das Standard Koordinatensystem hat den Ursprung in der oberen linken Ecke, wobei die x-Achse nach rechts und die y-Achse nach unten zeigt. Die Maßeinheit im Standard Koordinatensystem ist das Pixel.  
  
## <a name="the-building-blocks-of-gdi"></a>Die Bausteine von GDI+  
 ![Vektorgrafik](./media/aboutgdip02-art01.gif "AboutGdip02_Art01")  
  
 Ein Computermonitor erstellt seine Anzeige auf einem rechteckigen Array von Punkten, die als Bildelemente oder Pixel bezeichnet werden. Die Anzahl der Pixel, die auf dem Bildschirm angezeigt werden, variiert von einem Monitor zum nächsten, und die Anzahl der Pixel, die auf einem einzelnen Monitor angezeigt werden, kann normalerweise in gewissem Umfang vom Benutzer konfiguriert werden.  
  
 ![Vektorgrafik](./media/aboutgdip02-art02.gif "AboutGdip02_Art02")  
  
 Wenn Sie GDI+ zum Zeichnen einer Linie, eines Rechtecks oder einer Kurve verwenden, stellen Sie bestimmte Schlüsselinformationen über das zu zeichnende Element bereit. Sie können z. b. eine Zeile angeben, indem Sie zwei Punkte bereitstellen, und Sie können ein Rechteck angeben, indem Sie einen Punkt, eine Höhe und eine Breite angeben. GDI+ funktioniert in Verbindung mit der Anzeigetreiber Software, um zu bestimmen, welche Pixel eingeschaltet werden müssen, um die Linie, das Rechteck oder die Kurve anzuzeigen. Die folgende Abbildung zeigt die Pixel, die aktiviert werden, um eine Linie vom Punkt (4, 2) bis zum Punkt (12, 8) anzuzeigen.  
  
 ![Vektorgrafik](./media/aboutgdip02-art03.gif "AboutGdip02_Art03")  
  
 Im Laufe der Zeit haben sich bestimmte grundlegende Bausteine als besonders hilfreich für das Erstellen zweidimensionaler Bilder bewährt. Diese Bausteine, die alle von GDI+ unterstützt werden, sind in der folgenden Liste aufgeführt:  
  
- Linien  
  
- Rechtecke  
  
- Ellipsen  
  
- Bögen  
  
- Polygone  
  
- Kardinale Splines  
  
- Béziersplinekurven  
  
## <a name="methods-for-drawing-with-a-graphics-object"></a>Methoden zum Zeichnen mit einem Grafik Objekt  
 Die <xref:System.Drawing.Graphics> -Klasse in GDI+ bietet die folgenden Methoden zum Zeichnen der Elemente in der vorherigen Liste: <xref:System.Drawing.Graphics.DrawLine%2A> , <xref:System.Drawing.Graphics.DrawRectangle%2A> , <xref:System.Drawing.Graphics.DrawEllipse%2A> , <xref:System.Drawing.Graphics.DrawPolygon%2A> , <xref:System.Drawing.Graphics.DrawArc%2A> , <xref:System.Drawing.Graphics.DrawCurve%2A> (für Kardinal-Splines) und <xref:System.Drawing.Graphics.DrawBezier%2A> . Jede dieser Methoden ist überladen. Das heißt, jede Methode unterstützt mehrere verschiedene Parameterlisten. Beispielsweise empfängt eine Variation der <xref:System.Drawing.Graphics.DrawLine%2A> -Methode ein <xref:System.Drawing.Pen> -Objekt und vier ganze Zahlen, während eine andere Variation der <xref:System.Drawing.Graphics.DrawLine%2A> -Methode ein <xref:System.Drawing.Pen> -Objekt und zwei- <xref:System.Drawing.Point> Objekte empfängt.  
  
 Die Methoden zum Zeichnen von Linien, Rechtecke und Bézier-Splines verfügen über Plural-Begleit Methoden, die mehrere Elemente in einem einzelnen-Befehl zeichnen: <xref:System.Drawing.Graphics.DrawLines%2A> , <xref:System.Drawing.Graphics.DrawRectangles%2A> und <xref:System.Drawing.Graphics.DrawBeziers%2A> . Außerdem verfügt die- <xref:System.Drawing.Graphics.DrawCurve%2A> Methode über eine Begleit Methode, <xref:System.Drawing.Graphics.DrawClosedCurve%2A> , die eine Kurve schließt, indem der Endpunkt der Kurve mit dem Ausgangspunkt verbunden wird.  
  
 Alle Zeichnungs Methoden der- <xref:System.Drawing.Graphics> Klasse funktionieren in Verbindung mit einem- <xref:System.Drawing.Pen> Objekt. Um etwas zu zeichnen, müssen Sie mindestens zwei Objekte erstellen: ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt. Das- <xref:System.Drawing.Pen> Objekt speichert Attribute, z. b. Linienstärke und Farbe, des zu Zeichenden Elements. Das <xref:System.Drawing.Pen> Objekt wird als eines der Argumente an die Zeichnungs Methode übermittelt. Beispielsweise empfängt eine Variation der <xref:System.Drawing.Graphics.DrawLine%2A> -Methode ein <xref:System.Drawing.Pen> -Objekt und vier ganze Zahlen, wie im folgenden Beispiel gezeigt, das ein Rechteck mit einer Breite von 100, eine Höhe von 50 und eine obere linke Ecke von (20, 10) zeichnet:  
  
 [!code-csharp[LinesCurvesAndShapes#11](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#11)]
 [!code-vb[LinesCurvesAndShapes#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#11)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md)
