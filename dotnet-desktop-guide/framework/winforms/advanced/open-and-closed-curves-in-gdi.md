---
title: Offene und geschlossene Kurven in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- curves [Windows Forms], filling
- GDI+, curves
- curves [Windows Forms], drawing
- curves
ms.assetid: 08d2cc9a-dc9d-4eed-bcbb-2c8e2ca5d3ae
ms.openlocfilehash: 06afdc4549f7c3c9b0636e5c7052dcca87a153f1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976072"
---
# <a name="open-and-closed-curves-in-gdi"></a>Offene und geschlossene Kurven in GDI+
Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.  
  
 ![Öffnen & geschlossenen Kurven](./media/aboutgdip02-art24.gif "Aboutgdip02_art24")  
  
## <a name="managed-interface-for-curves"></a>Verwaltete Schnittstelle für Kurven  
 Geschlossene Kurven verfügen über ein inneres und können daher mit einem Pinsel gefüllt werden. Die <xref:System.Drawing.Graphics> -Klasse in GDI+ bietet die folgenden Methoden zum Auffüllen geschlossener Formen und Kurven: <xref:System.Drawing.Graphics.FillRectangle%2A> , <xref:System.Drawing.Graphics.FillEllipse%2A> , <xref:System.Drawing.Graphics.FillPie%2A> , <xref:System.Drawing.Graphics.FillPolygon%2A> , <xref:System.Drawing.Graphics.FillClosedCurve%2A> , <xref:System.Drawing.Graphics.FillPath%2A> und <xref:System.Drawing.Graphics.FillRegion%2A> . Wenn Sie eine dieser Methoden aufzurufen, müssen Sie einen der spezifischen Pinseltypen ( <xref:System.Drawing.SolidBrush> , <xref:System.Drawing.Drawing2D.HatchBrush> , <xref:System.Drawing.TextureBrush> , <xref:System.Drawing.Drawing2D.LinearGradientBrush> oder <xref:System.Drawing.Drawing2D.PathGradientBrush> ) als Argument übergeben.  
  
 Die- <xref:System.Drawing.Graphics.FillPie%2A> Methode ist ein begleitende der- <xref:System.Drawing.Graphics.DrawArc%2A> Methode. Ebenso wie die- <xref:System.Drawing.Graphics.DrawArc%2A> Methode einen Teil der Gliederung einer Ellipse zeichnet, füllt die- <xref:System.Drawing.Graphics.FillPie%2A> Methode einen Teil des Inneren einer Ellipse aus. Im folgenden Beispiel wird ein Bogen gezeichnet und der entsprechende Teil des Inneren der Ellipse gefüllt:  
  
 [!code-csharp[LinesCurvesAndShapes#21](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#21)]
 [!code-vb[LinesCurvesAndShapes#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#21)]  
  
 Die folgende Abbildung zeigt den Bogen und den gefüllten Kreis.  
  
 ![Öffnen & geschlossenen Kurven](./media/aboutgdip02-art25.gif "Aboutgdip02_art25")  
  
 Die- <xref:System.Drawing.Graphics.FillClosedCurve%2A> Methode ist ein begleitende der- <xref:System.Drawing.Graphics.DrawClosedCurve%2A> Methode. Beide Methoden schließen die Kurve automatisch, indem Sie den Endpunkt mit dem Ausgangspunkt verbinden. Im folgenden Beispiel wird eine Kurve gezeichnet, die durchläuft (0,0), (60, 20) und (40, 50). Anschließend wird die Kurve automatisch geschlossen, indem (40, 50) mit dem Anfangspunkt (0,0) verbunden wird, und das innere wird mit einer voll Tonfarbe gefüllt.  
  
 [!code-csharp[LinesCurvesAndShapes#22](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#22)]
 [!code-vb[LinesCurvesAndShapes#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#22)]  
  
 Die- <xref:System.Drawing.Graphics.FillPath%2A> Methode füllt die Innenbereiche der separaten Teile eines Pfades. Wenn ein Teil eines Pfads keine geschlossene Kurve oder Form bildet, schließt die <xref:System.Drawing.Graphics.FillPath%2A> Methode diesen Teil des Pfads automatisch, bevor Sie ihn füllt. Im folgenden Beispiel wird ein Pfad, der aus einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis besteht, gezeichnet und gefüllt:  
  
 [!code-csharp[LinesCurvesAndShapes#23](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#23)]
 [!code-vb[LinesCurvesAndShapes#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#23)]  
  
 In der folgenden Abbildung wird der Pfad mit und ohne das voll Bild Füll Diagramm dargestellt. Beachten Sie, dass der Text in der Zeichenfolge von der-Methode beschrieben, aber nicht ausgefüllt wird <xref:System.Drawing.Graphics.DrawPath%2A> . Dabei handelt es sich um die <xref:System.Drawing.Graphics.FillPath%2A> Methode, die das Innere der Zeichen in der Zeichenfolge zeichnet.  
  
 ![Zeichenfolge in einem Pfad](./media/aboutgdip02-art26.gif "Aboutgdip02_art26")  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Point?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md)
- [Erstellen und Zeichnen von Pfaden](constructing-and-drawing-paths.md)
