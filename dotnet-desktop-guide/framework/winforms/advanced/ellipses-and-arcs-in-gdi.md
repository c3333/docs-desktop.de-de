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
# <a name="ellipses-and-arcs-in-gdi"></a>Ellipsen und Bögen in GDI+
Mit der <xref:System.Drawing.Graphics.DrawEllipse%2A> -Methode und der- <xref:System.Drawing.Graphics.DrawArc%2A> Methode der-Klasse können Sie ganz einfach Ellipsen und Bögen zeichnen <xref:System.Drawing.Graphics> .  
  
## <a name="drawing-an-ellipse"></a>Zeichnen einer Ellipse  
 Zum Zeichnen einer Ellipse benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt. Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawEllipse%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute, z. b. "width" und "Color", der zum Rendering der Ellipse verwendeten Zeile. Das- <xref:System.Drawing.Pen> Objekt wird als eines der Argumente an die- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode übermittelt. Die übrigen Argumente, die an die-Methode übergeben werden, <xref:System.Drawing.Graphics.DrawEllipse%2A> geben das Begrenzungs Rechteck für die Ellipse an. In der folgenden Abbildung wird eine Ellipse zusammen mit dem umgebenden Rechteck gezeigt.  
  
 ![Ellipsen und Bögen](./media/aboutgdip02-art05.gif "Aboutgdip02_art05")  
  
 Im folgenden Beispiel wird eine Ellipse gezeichnet. das umgebende Rechteck hat eine Breite von 80, eine Höhe von 40 und eine linke obere Ecke von (100, 50):  
  
 [!code-csharp[LinesCurvesAndShapes#51](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#51)]
 [!code-vb[LinesCurvesAndShapes#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#51)]  
  
 <xref:System.Drawing.Graphics.DrawEllipse%2A> ist eine überladene Methode der- <xref:System.Drawing.Graphics> Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen. Beispielsweise können Sie einen erstellen <xref:System.Drawing.Rectangle> und <xref:System.Drawing.Rectangle> an die- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode als Argument übergeben:  
  
 [!code-csharp[LinesCurvesAndShapes#52](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#52)]
 [!code-vb[LinesCurvesAndShapes#52](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#52)]  
  
## <a name="drawing-an-arc"></a>Zeichnen eines Bogens  
 Ein Bogen ist ein Teil einer Ellipse. Um einen Bogen zu zeichnen, wird die- <xref:System.Drawing.Graphics.DrawArc%2A> Methode der- <xref:System.Drawing.Graphics> Klasse aufgerufen. Die Parameter der- <xref:System.Drawing.Graphics.DrawArc%2A> Methode sind identisch mit den Parametern der- <xref:System.Drawing.Graphics.DrawEllipse%2A> Methode, mit dem Unterschied, dass <xref:System.Drawing.Graphics.DrawArc%2A> einen Anfangs Winkel und einen Pfeil Winkel erfordert. Im folgenden Beispiel wird ein Bogen mit einem Anfangs Winkel von 30 Grad und einem Mittelpunktswinkel von 180 Grad gezeichnet:  
  
 [!code-csharp[LinesCurvesAndShapes#53](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#53)]
 [!code-vb[LinesCurvesAndShapes#53](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#53)]  
  
 Die folgende Abbildung zeigt den Bogen, die Ellipse und das umgebende Rechteck.  
  
 ![Ellipsen und Bögen](./media/aboutgdip02-art06.gif "Aboutgdip02_art06")  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md)
- [Vorgehensweise: Erstellen eines Stifts](how-to-create-a-pen.md)
- [Vorgehensweise: Zeichnen der Kontur einer Form](how-to-draw-an-outlined-shape.md)
