---
title: Kardinale Splines in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- splines [Windows Forms], cardinal
- GDI+, cardinal splines
- cardinal splines
ms.assetid: 09b3797a-6294-422d-9adf-a5a0a7695c0c
ms.openlocfilehash: 4588f6f606f0f479aeae1d143f23175ec4be32a5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975060"
---
# <a name="cardinal-splines-in-gdi"></a>Kardinale Splines in GDI+
Bei einem kardinalspline handelt es sich um eine Sequenz von einzelnen Kurven, die mit einer größeren Kurve verknüpft sind. Der Spline wird durch ein Array von Punkten und einen Tension-Parameter angegeben. Ein kardinaler Spline verläuft nahtlos durch jeden Punkt im Array. Es sind keine spitzen Ecken und keine abrupten Änderungen in der Genauigkeit der Kurve vorhanden. Die folgende Abbildung zeigt einen Satz von Punkten und einen kardinalspline, der die einzelnen Punkte im Satz durchläuft.  
  
 ![Kardinale Spline](./media/aboutgdip02-art09.gif "Aboutgdip02_art09")  
  
## <a name="physical-and-mathematical-splines"></a>Physische und mathematische Splines  
 Eine physische Spline ist ein dünner Teil des Holzes oder eines anderen flexiblen Materials. Vor der Einführung mathematischer Splines verwendeten Designer physische Splines zum Zeichnen von Kurven. Ein Designer würde den Spline in einem Papier Abschnitt platzieren und ihn an eine bestimmte Gruppe von Punkten verankern. Der Designer kann dann eine Kurve erstellen, indem er die Spline mit einem Stift oder einem Stift zeichnet. Eine bestimmte Gruppe von Punkten kann abhängig von den Eigenschaften der physischen Spline eine Vielzahl von Kurven ergeben. Beispielsweise würde ein Spline mit einem hohen Widerstand zum wechseln eine andere Kurve als eine extrem flexible Spline ergeben.  
  
 Die Formeln für mathematische Splines basieren auf den Eigenschaften von flexiblen Stäbchen, sodass die Kurven, die von mathematischen Splines erzeugt werden, mit den Kurven vergleichbar sind, die von physischen Splines erzeugt wurden. Ebenso wie physische Splines mit unterschiedlichen Verspannungen durch einen bestimmten Satz von Punkten unterschiedliche Kurven bewirken, werden mathematische Splines mit unterschiedlichen Werten für den Tension-Parameter unterschiedliche Kurven durch einen bestimmten Satz von Punkten ergeben. Die folgende Abbildung zeigt vier kardinale Splines, die denselben Satz von Punkten passieren. Die Spannung wird für jede Spline angezeigt. Eine Spannung von 0 entspricht der unendlichen physischen Spannung und erzwingt, dass die Kurve die kürzeste Richtung (gerade Linien) zwischen Punkten übernimmt. Eine Spannung von 1 entspricht keiner physischen Spannung, sodass der Spline den Weg der geringsten Gesamt Kurve annehmen kann. Wenn Spannungswerte größer als 1 sind, verhält sich die Kurve wie eine komprimierte Spring-Kurve, die über einen längeren Pfad verfügt.  
  
 ![Kardinale Splines](./media/aboutgdip02-art10.gif "Aboutgdip02_art10")  
  
 Die vier Splines in der vorangehenden Abbildung teilen die gleiche Tangenten Linie am Ausgangspunkt. Der Tangens ist die Linie, die vom Startpunkt bis zum nächsten Punkt entlang der Kurve gezeichnet wird. Ebenso ist der gemeinsame Tangens am Endpunkt die Linie, die vom Endpunkt zum vorherigen Punkt der Kurve gezeichnet wird.  
  
 Um einen kardinalspline zu zeichnen, benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse, ein <xref:System.Drawing.Pen> und ein Array von- <xref:System.Drawing.Point> Objekten, die die Instanz der- <xref:System.Drawing.Graphics> Klasse die-Methode bereitstellt <xref:System.Drawing.Graphics.DrawCurve%2A> , die die Spline zeichnet, und das <xref:System.Drawing.Pen> speichert Attribute der Spline, wie z. b. Linienstärke und Farbe. Das Array von- <xref:System.Drawing.Point> Objekten speichert die Punkte, die die Kurve übergibt. Im folgenden Codebeispiel wird gezeigt, wie ein kardinaler Spline gezeichnet wird, der die Punkte in durchläuft `myPointArray` . Der dritte Parameter ist die Spannung.  
  
 [!code-csharp[LinesCurvesAndShapes#31](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#31)]
 [!code-vb[LinesCurvesAndShapes#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#31)]  
  
## <a name="see-also"></a>Siehe auch

- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Erstellen und Zeichnen von Kurven](constructing-and-drawing-curves.md)
