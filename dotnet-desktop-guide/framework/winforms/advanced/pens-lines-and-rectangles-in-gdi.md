---
title: Stifte, Linien und Rechtecke in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines
- GDI+, lines
- drawing [Windows Forms], rectangles
- rectangles
- drawing [Windows Forms], lines
- GDI+, pens
- examples [Windows Forms], drawing lines and shapes
- examples [Windows Forms], pens
- GDI+, rectangles
- examples [Windows Forms], GDI+
- lines [Windows Forms], dashed
ms.assetid: 30b25aae-e3eb-4479-bdb8-187cf651fc84
ms.openlocfilehash: 06d2351ffa7d7f009d7b049f4689df7038b4d202
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976071"
---
# <a name="pens-lines-and-rectangles-in-gdi"></a>Stifte, Linien und Rechtecke in GDI+
Zum Zeichnen von Linien mit GDI+ müssen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt erstellen. Das <xref:System.Drawing.Graphics> -Objekt stellt die Methoden bereit, die die Zeichnung tatsächlich ausführen, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute, wie z. b. Linien Farbe, Breite und Stil.  
  
## <a name="drawing-a-line"></a>Zeichnen einer Linie  
 Um eine Linie zu zeichnen, müssen Sie die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode des- <xref:System.Drawing.Graphics> Objekts aufrufen. Das- <xref:System.Drawing.Pen> Objekt wird als eines der Argumente an die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode übermittelt. Im folgenden Beispiel wird eine Linie vom Punkt (4, 2) bis zum Punkt (12, 6) gezeichnet:  
  
 [!code-csharp[LinesCurvesAndShapes#41](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#41)]
 [!code-vb[LinesCurvesAndShapes#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#41)]  
  
 <xref:System.Drawing.Graphics.DrawLine%2A> ist eine überladene Methode der- <xref:System.Drawing.Graphics> Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen. Beispielsweise können Sie zwei <xref:System.Drawing.Point> -Objekte erstellen und die- <xref:System.Drawing.Point> Objekte als Argumente an die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode übergeben:  
  
 [!code-csharp[LinesCurvesAndShapes#42](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#42)]
 [!code-vb[LinesCurvesAndShapes#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#42)]  
  
## <a name="constructing-a-pen"></a>Erstellen eines Stifts  
 Sie können bestimmte Attribute angeben, wenn Sie ein- <xref:System.Drawing.Pen> Objekt erstellen. Beispielsweise `Pen` können Sie mit einem Konstruktor Farbe und Breite angeben. Im folgenden Beispiel wird eine blaue Linie der Breite 2 von (0,0) bis (60, 30) gezeichnet:  
  
 [!code-csharp[LinesCurvesAndShapes#43](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#43)]
 [!code-vb[LinesCurvesAndShapes#43](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#43)]  
  
## <a name="dashed-lines-and-line-caps"></a>Gestrichelte Linien und Linien Kappen  
 Das- <xref:System.Drawing.Pen> Objekt macht auch Eigenschaften verfügbar, wie z <xref:System.Drawing.Pen.DashStyle%2A> . b., mit denen Sie Features der Zeile angeben können. Im folgenden Beispiel wird eine gestrichelte Linie von (100, 50) nach (300, 80) gezeichnet:  
  
 [!code-csharp[LinesCurvesAndShapes#44](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#44)]
 [!code-vb[LinesCurvesAndShapes#44](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#44)]  
  
 Sie können die Eigenschaften des- <xref:System.Drawing.Pen> Objekts verwenden, um viele weitere Attribute der Zeile festzulegen. Die <xref:System.Drawing.Pen.StartCap%2A> <xref:System.Drawing.Pen.EndCap%2A> Eigenschaften und geben die Darstellung der Zeilenenden an. die enden können flach, quadratisch, gerundet, dreieckig oder eine benutzerdefinierte Form sein. Mithilfe der- <xref:System.Drawing.Pen.LineJoin%2A> Eigenschaft können Sie angeben, ob verbundene Linien gezippt (mit spitzen Ecken verknüpft), geglättet, gerundet oder abgeschnitten werden. In der folgenden Abbildung werden Zeilen mit verschiedenen Obergrenzen und joinstilen dargestellt.  
  
 ![Linien](./media/aboutgdip02-art04.gif "Aboutgdip02_art04")  
  
## <a name="drawing-a-rectangle"></a>Zeichnen eines Rechtecks  
 Zeichnungs Rechtecke mit GDI+ ähneln Zeichnungslinien. Zum Zeichnen eines Rechtecks benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt. Das <xref:System.Drawing.Graphics> -Objekt stellt eine <xref:System.Drawing.Graphics.DrawRectangle%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Attribute, wie z. b. Linienstärke und Farbe. Das- <xref:System.Drawing.Pen> Objekt wird als eines der Argumente an die- <xref:System.Drawing.Graphics.DrawRectangle%2A> Methode übermittelt. Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (100, 50), einer Breite von 80 und einer Höhe von 40 gezeichnet:  
  
 [!code-csharp[LinesCurvesAndShapes#45](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#45)]
 [!code-vb[LinesCurvesAndShapes#45](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#45)]  
  
 <xref:System.Drawing.Graphics.DrawRectangle%2A> ist eine überladene Methode der- <xref:System.Drawing.Graphics> Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen. Beispielsweise können Sie ein <xref:System.Drawing.Rectangle> -Objekt erstellen und das- <xref:System.Drawing.Rectangle> Objekt als Argument an die- <xref:System.Drawing.Graphics.DrawRectangle%2A> Methode übergeben:  
  
 [!code-csharp[LinesCurvesAndShapes#46](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#46)]
 [!code-vb[LinesCurvesAndShapes#46](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#46)]  
  
 Ein- <xref:System.Drawing.Rectangle> Objekt verfügt über Methoden und Eigenschaften zum Bearbeiten und Sammeln von Informationen über das Rechteck. Die <xref:System.Drawing.Rectangle.Inflate%2A> -Methode und die- <xref:System.Drawing.Rectangle.Offset%2A> Methode ändern z. b. die Größe und Position des Rechtecks. Die <xref:System.Drawing.Rectangle.IntersectsWith%2A> -Methode gibt Aufschluss darüber, ob das Rechteck ein anderes angegebenes Rechteck überschneidet und <xref:System.Drawing.Rectangle.Contains%2A> ob sich ein angegebener Punkt innerhalb des Rechtecks befindet.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Rectangle?displayProperty=nameWithType>
- [Vorgehensweise: Erstellen eines Stifts](how-to-create-a-pen.md)
- [Vorgehensweise: Zeichnen einer Linie in Windows Forms](how-to-draw-a-line-on-a-windows-form.md)
- [Vorgehensweise: Zeichnen der Kontur einer Form](how-to-draw-an-outlined-shape.md)
