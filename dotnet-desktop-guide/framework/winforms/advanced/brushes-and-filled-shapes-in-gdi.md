---
title: Pinsel und gefüllte Formen in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [Windows Forms], GDI+
- filled shapes [Windows Forms], GDI+
- shapes [Windows Forms], GDI+
- GDI+, brushes
- GDI+, filled shapes
- gradient brushes
- brushes [Windows Forms], gradient
ms.assetid: e863e2a7-0294-4130-99b6-f1ea3201e7cd
ms.openlocfilehash: 45ef0b5920e43300e047d363149ea10a7833477b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972407"
---
# <a name="brushes-and-filled-shapes-in-gdi"></a>Pinsel und gefüllte Formen in GDI+
Eine geschlossene Form, z. b. ein Rechteck oder eine Ellipse, besteht aus einem Umriss und einem inneren. Der Umriss wird mit einem Stift gezeichnet, und das Innere ist mit einem Pinsel gefüllt. GDI+ bietet verschiedene Pinsel Klassen zum Auffüllen des Inneren von geschlossenen Formen: <xref:System.Drawing.SolidBrush> , <xref:System.Drawing.Drawing2D.HatchBrush> , <xref:System.Drawing.TextureBrush> , <xref:System.Drawing.Drawing2D.LinearGradientBrush> und <xref:System.Drawing.Drawing2D.PathGradientBrush> . Alle diese Klassen erben von der- <xref:System.Drawing.Brush> Klasse. Die folgende Abbildung zeigt ein Rechteck, das mit einem Pinsel gefüllt ist, und eine Ellipse mit einem Schraffurpinsel.  
  
 ![Gefüllte Formen](./media/aboutgdip02-art17.gif "Aboutgdip02_art17")  
  
## <a name="solid-brushes"></a>Vollpinsel  
 Um eine geschlossene Form auszufüllen, benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse und eine-Klasse <xref:System.Drawing.Brush> . Die Instanz der <xref:System.Drawing.Graphics> -Klasse stellt Methoden bereit, wie z. b. <xref:System.Drawing.Graphics.FillRectangle%2A> und <xref:System.Drawing.Graphics.FillEllipse%2A> , und <xref:System.Drawing.Brush> speichert Attribute der Füllung, z. b. Farbe und Muster. <xref:System.Drawing.Brush>Wird als eines der Argumente an die Fill-Methode übermittelt. Im folgenden Codebeispiel wird gezeigt, wie eine Ellipse mit einer voll Tonfarbe gefüllt wird.  
  
 [!code-csharp[LinesCurvesAndShapes#121](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#121)]
 [!code-vb[LinesCurvesAndShapes#121](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#121)]  
  
> [!NOTE]
> Im vorherigen Beispiel ist der Pinsel vom Typ, der <xref:System.Drawing.SolidBrush> von erbt <xref:System.Drawing.Brush> .  
  
## <a name="hatch-brushes"></a>Pinsel Schraffur  
 Wenn Sie eine Form mit einem Schraffurpinsel ausfüllen, geben Sie eine Vordergrundfarbe, eine Hintergrundfarbe und eine Schraffurart an. Die Vordergrundfarbe ist die Farbe der Schraffur.  
  
 [!code-csharp[LinesCurvesAndShapes#122](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#122)]
 [!code-vb[LinesCurvesAndShapes#122](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#122)]  
  
 GDI+ bietet mehr als 50 Schraffurstile. die drei in der folgenden Abbildung gezeigten Stile sind <xref:System.Drawing.Drawing2D.HatchStyle.Horizontal> , <xref:System.Drawing.Drawing2D.HatchStyle.ForwardDiagonal> und <xref:System.Drawing.Drawing2D.HatchStyle.Cross> .  
  
 ![Gefüllte Formen](./media/aboutgdip02-art18.gif "Aboutgdip02_art18")  
  
## <a name="texture-brushes"></a>Textur Pinsel  
 Mit einem Textur Pinsel können Sie eine Form mit einem Muster ausfüllen, das in einer Bitmap gespeichert ist. Angenommen, das folgende Bild ist in einer Datenträger Datei mit dem Namen gespeichert `MyTexture.bmp` .  
  
 ![Ausgefüllte Form](./media/aboutgdip02-art19.gif "Aboutgdip02_Art19")  
  
 Im folgenden Codebeispiel wird gezeigt, wie eine Ellipse ausgefüllt wird, indem das in gespeicherte Bild wiederholt wird `MyTexture.bmp` .  
  
 [!code-csharp[LinesCurvesAndShapes#123](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#123)]
 [!code-vb[LinesCurvesAndShapes#123](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#123)]  
  
 Die folgende Abbildung zeigt die gefüllte Ellipse.  
  
 ![Ausgefüllte Form](./media/aboutgdip02-art20.gif "AboutGdip02_Art20")  
  
## <a name="gradient-brushes"></a>Farbverlaufs Pinsel  
 GDI+ bietet zwei Arten von Farbverlaufs Pinsel: Linear und Path. Mit einem linearen Farbverlaufs Pinsel können Sie eine Form mit einer Farbe ausfüllen, die sich allmählich ändert, wenn Sie die Form horizontal, vertikal oder diagonal verschieben. Im folgenden Codebeispiel wird veranschaulicht, wie eine Ellipse mit einem horizontalen Farbverlaufs Pinsel ausgefüllt wird, der sich von blau in grün ändert, während Sie vom linken Rand der Ellipse zum rechten Rand wechseln.  
  
 [!code-csharp[LinesCurvesAndShapes#124](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#124)]
 [!code-vb[LinesCurvesAndShapes#124](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#124)]  
  
 Die folgende Abbildung zeigt die gefüllte Ellipse.  
  
 ![Ausgefüllte Form](./media/aboutgdip02-art21.gif "AboutGdip02_Art21")  
  
 Ein Pinsel mit dem Pfad Farbverlauf kann so konfiguriert werden, dass die Farbe geändert wird, wenn Sie von der Mitte einer Form zum Rand wechseln.  
  
 ![Ausgefüllte Form](./media/aboutgdip02-art22.gif "AboutGdip02_Art22")  
  
 Pfad Farbverlaufs Pinsel sind recht flexibel. Der Farbverlaufs Pinsel, der zum Ausfüllen des Dreiecks in der folgenden Abbildung verwendet wird, ändert sich allmählich von rot in der Mitte zu jeder der drei verschiedenen Farben in den Scheitel Punkten.  
  
 ![Ausgefüllte Form](./media/aboutgdip02-art23.gif "AboutGdip02_Art23")  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.SolidBrush?displayProperty=nameWithType>
- <xref:System.Drawing.Drawing2D.HatchBrush?displayProperty=nameWithType>
- <xref:System.Drawing.TextureBrush?displayProperty=nameWithType>
- <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Vorgehensweise: Zeichnen eines ausgefüllten Rechtecks in Windows Forms](how-to-draw-a-filled-rectangle-on-a-windows-form.md)
- [Vorgehensweise: Zeichnen einer ausgefüllten Ellipse in Windows Forms](how-to-draw-a-filled-ellipse-on-a-windows-form.md)
