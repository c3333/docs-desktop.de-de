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
# <a name="graphics-paths-in-gdi"></a>Grafikpfade in GDI+
Pfade werden gebildet, indem Linien, Rechtecke und einfache Kurven kombiniert werden. Erinnern Sie sich aus der [Übersicht über Vektorgrafiken](vector-graphics-overview.md) , dass die folgenden grundlegenden Bausteine sich als besonders nützlich für das Zeichnen von Bildern erwiesen haben:  
  
- Linien  
  
- Rechtecke  
  
- Ellipsen  
  
- Bögen  
  
- Polygone  
  
- Kardinale Splines  
  
- Bézier-Splines  
  
 In GDI+ können Sie mit dem- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt eine Sequenz dieser Bausteine in einer einzelnen Einheit erfassen. Die gesamte Sequenz von Linien, Rechtecke, Polygonen und Kurven kann dann mit einem Rückruf der- <xref:System.Drawing.Graphics.DrawPath%2A> Methode der-Klasse gezeichnet werden <xref:System.Drawing.Graphics> . Die folgende Abbildung zeigt einen Pfad, der durch das Kombinieren einer Linie, eines Bogens, eines Bézier-Spline und eines kardinaler Spline erstellt wurde.  
  
 ![Pfad](./media/aboutgdip02-art14.gif "Aboutgdip02_art14")  
  
## <a name="using-a-path"></a>Verwenden eines Pfads  
 Die <xref:System.Drawing.Drawing2D.GraphicsPath> -Klasse stellt die folgenden Methoden zum Erstellen einer Sequenz von Elementen bereit, die gezeichnet werden sollen: <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangle%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddEllipse%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddPolygon%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> (für Kardinal-Splines) und <xref:System.Drawing.Drawing2D.GraphicsPath.AddBezier%2A> . Jede dieser Methoden ist überladen. Das heißt, jede Methode unterstützt mehrere verschiedene Parameterlisten. Beispielsweise empfängt eine Variation der- <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> Methode vier ganze Zahlen, und eine andere Variation der- <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> Methode empfängt zwei- <xref:System.Drawing.Point> Objekte.  
  
 Die Methoden zum Hinzufügen von Linien, Rechtecke und Bézier-Splines zu einem Pfad verfügen über Plural-Begleit Methoden, mit denen dem Pfad in einem einzelnen-Befehl mehrere Elemente hinzugefügt werden: <xref:System.Drawing.Drawing2D.GraphicsPath.AddLines%2A> , <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangles%2A> und <xref:System.Drawing.Drawing2D.GraphicsPath.AddBeziers%2A> . Außerdem verfügen die <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> -Methode und die- <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A> Methode über die-und-Methoden, die <xref:System.Drawing.Drawing2D.GraphicsPath.AddClosedCurve%2A> <xref:System.Drawing.Drawing2D.GraphicsPath.AddPie%2A> dem Pfad eine geschlossene Kurve oder einen Kreis hinzufügen.  
  
 Um einen Pfad zu zeichnen, benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt, ein <xref:System.Drawing.Pen> -Objekt und ein- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt. Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawPath%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute wie "width" und "Color" der zum Rendering des Pfads verwendeten Zeile. Das <xref:System.Drawing.Drawing2D.GraphicsPath> -Objekt speichert die Sequenz von Linien und Kurven, die den Pfad bilden. Das <xref:System.Drawing.Pen> -Objekt und das- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt werden als Argumente an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawPath%2A> . Im folgenden Beispiel wird ein Pfad gezeichnet, der aus einer Zeile, einer Ellipse und einem Bézier-Spline besteht:  
  
 [!code-csharp[LinesCurvesAndShapes#101](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#101)]
 [!code-vb[LinesCurvesAndShapes#101](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#101)]  
  
 In der folgenden Abbildung ist der Pfad dargestellt.  
  
 ![Pfad](./media/aboutgdip02-art15.gif "Aboutgdip02_art15")  
  
 Zusätzlich zum Hinzufügen von Linien, Rechtecke und Kurven zu einem Pfad können Sie Pfade zu einem Pfad hinzufügen. Dies ermöglicht Ihnen das Kombinieren vorhandener Pfade, um große und komplexe Pfade zu bilden.  
  
 [!code-csharp[LinesCurvesAndShapes#102](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#102)]
 [!code-vb[LinesCurvesAndShapes#102](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#102)]  
  
 Es gibt zwei weitere Elemente, die Sie einem Pfad hinzufügen können: Strings und Pies. Ein Kreis ist ein Teil des Inneren einer Ellipse. Im folgenden Beispiel wird ein Pfad aus einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis erstellt:  
  
 [!code-csharp[LinesCurvesAndShapes#103](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#103)]
 [!code-vb[LinesCurvesAndShapes#103](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#103)]  
  
 In der folgenden Abbildung ist der Pfad dargestellt. Beachten Sie, dass für einen Pfad keine Verbindung hergestellt werden muss. der Bogen, der kardinalspline, die Zeichenfolge und der Kreis werden getrennt.  
  
 ![Paths](./media/aboutgdip02-art16.gif "Aboutgdip02_Art16")  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- <xref:System.Drawing.Point?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md)
- [Erstellen und Zeichnen von Pfaden](constructing-and-drawing-paths.md)
