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
# <a name="b233zier-splines-in-gdi"></a>B&#233;Zier-Splines in GDI+
Eine Bézier-Spline ist eine Kurve, die von vier Punkten angegeben wird: zwei Endpunkte (P1 und P2) und zwei Kontrollpunkte (C1 und C2). Die Kurve beginnt bei P1 und endet bei P2. Die Kurve übergibt nicht die Steuerungs Punkte, aber die Steuerungs Punkte fungieren als Magnete, ziehen die Kurve in bestimmte Richtungen und beeinflussen die Kurven Kurven. In der folgenden Abbildung wird eine Bézier-Kurve zusammen mit den zugehörigen Endpunkten und Steuerungs Punkten dargestellt.  
  
 ![Bezier-Splines](./media/aboutgdip02-art11a.gif "Aboutgdip02_art11a")  
  
 Die Kurve beginnt bei P1 und wechselt zur Steuerungspunkt C1. Die Tangente an der Kurve bei P1 ist die Linie, die von P1 bis C1 gezeichnet wird. Die Tangente-Linie am Endpunkt P2 ist die Linie, die von C2 bis P2 gezeichnet wird.  
  
## <a name="drawing-bzier-splines"></a>Zeichnen von Bézier-Splines  
 Zum Zeichnen eines Bézier-Spline benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse und eine-Klasse <xref:System.Drawing.Pen> . Die Instanz der <xref:System.Drawing.Graphics> -Klasse stellt die <xref:System.Drawing.Graphics.DrawBezier%2A> -Methode bereit, und <xref:System.Drawing.Pen> speichert Attribute wie "width" und "Color" der zum Rendering der Kurve verwendeten Zeile. <xref:System.Drawing.Pen>Wird als eines der Argumente an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawBezier%2A> . Die übrigen Argumente, die an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawBezier%2A> werden, sind die Endpunkte und die Steuerungs Punkte. Im folgenden Beispiel wird eine Bézier-Spline mit einem Startpunkt (0,0), Steuerungs Punkten (40, 20) und (80, 150) und einem Endpunkt (100, 10) gezeichnet:  
  
 [!code-csharp[LinesCurvesAndShapes#71](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#71)]
 [!code-vb[LinesCurvesAndShapes#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#71)]  
  
 In der folgenden Abbildung sind die Kurve, die Kontrollpunkte und zwei Tangenten Linien dargestellt.  
  
 ![Bezier-Splines](./media/aboutgdip02-art12.gif "Aboutgdip02_art12")  
  
 Die Bézier-Splines wurden ursprünglich von Pierre Bézier zum Entwerfen in der Automobilindustrie entwickelt. Sie haben sich in vielen Arten von computergestütztem Design bewährt und werden auch verwendet, um die Umschriften von Schriftarten zu definieren. Die Bézier-Splines können eine Vielzahl von Formen ergeben, von denen einige in der folgenden Abbildung dargestellt sind.  
  
 ![Paths](./media/aboutgdip02-art13.gif "Aboutgdip02_art13")  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Erstellen und Zeichnen von Kurven](constructing-and-drawing-curves.md)
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md)
- [Vorgehensweise: Erstellen eines Stifts](how-to-create-a-pen.md)
