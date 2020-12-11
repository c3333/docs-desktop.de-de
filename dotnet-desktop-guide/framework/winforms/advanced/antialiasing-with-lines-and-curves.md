---
title: Antialiasing bei Linien und Kurven
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- antialiasing
- antialiasing [Windows Forms], smoothing modes
- GDI+, antialiasing
ms.assetid: 810da1a4-c136-4abf-88df-68e49efdd8d4
ms.openlocfilehash: 871c5cb3cd9356f677633acb04fe82021a9787c5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974899"
---
# <a name="antialiasing-with-lines-and-curves"></a>Antialiasing bei Linien und Kurven
Wenn Sie GDI+ zum Zeichnen einer Linie verwenden, geben Sie den Ausgangspunkt und den Endpunkt der Zeile an, aber Sie müssen keine Informationen über die einzelnen Pixel in der Zeile angeben. GDI+ funktioniert in Verbindung mit der Anzeigetreiber Software, um zu bestimmen, welche Pixel eingeschaltet werden, um die Zeile auf einem bestimmten Anzeigegerät anzuzeigen.  
  
## <a name="aliasing"></a>Aliase  
 Angenommen, die gerade rote Linie wechselt vom Punkt (4, 2) bis zum Punkt (16, 10). Angenommen, das Koordinatensystem hat seinen Ursprung in der oberen linken Ecke, und die Maßeinheit ist das Pixel. Nehmen Sie auch an, dass die x-Achse nach rechts und die y-Achse nach unten zeigt. Die folgende Abbildung zeigt eine vergrößerte Ansicht der roten Linie, die auf einem mehrfarbigen Hintergrund gezeichnet wird.  
  
 ![Linie ohne Antialiasing](./media/aboutgdip02-art33.gif "AboutGdip02_Art33")  
  
 Die zum Rendering der Linie verwendeten roten Pixel sind nicht transparent. Es gibt keine teilweise transparenten Pixel in der Zeile. Diese Art von Zeilen Rendering gibt der Linie eine verzweigte Darstellung, und die Linie sieht in etwa wie eine Treppe aus. Diese Methode zum Darstellen einer Linie mit einer Treppe wird als Aliasing bezeichnet. die Treppe ist ein Alias für die theoretische Zeile.  
  
## <a name="antialiasing"></a>Antialiasing  
 Ein anspruchsvolleres Verfahren zum Rendern einer Linie besteht darin, teilweise transparente Pixel zusammen mit nicht transparenten Pixeln zu verwenden. Pixel sind auf rein rot oder auf eine Mischung aus roter und der Hintergrundfarbe festgelegt, je nachdem, wie nah Sie auf die Linie sind. Diese Art des Renderings wird als Antialiasing bezeichnet und führt zu einer Zeile, die das menschliche Auge als nahtloser ansieht. In der folgenden Abbildung wird gezeigt, wie bestimmte Pixel mit dem Hintergrund kombiniert werden, um eine Zeile mit einem-oder-Alias zu bilden.  
  
 ![Antialiasing bei einer Linie](./media/aboutgdip02-art34.gif "AboutGdip02_Art34")  
  
 Antialiasing, auch als Glättung bezeichnet, kann auch auf Kurven angewendet werden. Die folgende Abbildung zeigt eine vergrößerte Ansicht einer gegläten Ellipse.  
  
 ![Antialiasing bei Kurven](./media/aboutgdip02-art35.gif "AboutGdip02_Art35")  
  
 In der folgenden Abbildung wird die gleiche Ellipse in der tatsächlichen Größe angezeigt, einmal ohne Antialiasing und einmal mit Antialiasing.  
  
 ![Antialiasingbeispiel](./media/aboutgdip02-art36.gif "AboutGdip02_Art36")  
  
 Zum Zeichnen von Linien und Kurven, die Antialiasing verwenden, erstellen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse, und legen Sie die zugehörige- <xref:System.Drawing.Graphics.SmoothingMode%2A> Eigenschaft auf <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> oder fest <xref:System.Drawing.Drawing2D.SmoothingMode.HighQuality> . Anschließend wird eine der Zeichnungs Methoden der gleichen Klasse aufgerufen <xref:System.Drawing.Graphics> .  
  
 [!code-csharp[LinesCurvesAndShapes#81](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#81)]
 [!code-vb[LinesCurvesAndShapes#81](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#81)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.SmoothingMode?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Vorgehensweise: Verwenden der Bildkantenglättung mit Text](how-to-use-antialiasing-with-text.md)
