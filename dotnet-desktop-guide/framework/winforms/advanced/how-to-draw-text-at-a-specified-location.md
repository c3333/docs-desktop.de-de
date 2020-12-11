---
title: 'Vorgehensweise: Zeichnen von Text an einer angegebenen Position'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing at specified locations [Windows Forms]
- drawing text
- drawing text [Windows Forms], specified locations [Windows Forms]
- Windows Forms, drawing text at a specified location
ms.assetid: 60816423-1c38-465e-980d-2c2b64d74086
ms.openlocfilehash: 0c36b00e4f6f71f0ecf8042853bb8e99e57854da
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975927"
---
# <a name="how-to-draw-text-at-a-specified-location"></a>Vorgehensweise: Zeichnen von Text an einer angegebenen Position
Wenn Sie eine benutzerdefinierte Zeichnung ausführen, können Sie Text in einer einzelnen horizontalen Linie beginnend an einem angegebenen Punkt zeichnen. Sie können Text auf diese Weise zeichnen, indem Sie die <xref:System.Drawing.Graphics.DrawString%2A> überladene-Methode der- <xref:System.Drawing.Graphics> Klasse verwenden, die einen-oder-Parameter annimmt <xref:System.Drawing.Point> <xref:System.Drawing.PointF> . Die <xref:System.Drawing.Graphics.DrawString%2A> -Methode erfordert auch <xref:System.Drawing.Brush> und. <xref:System.Drawing.Font>  
  
 Sie können auch die <xref:System.Windows.Forms.TextRenderer.DrawText%2A> überladene-Methode der verwenden <xref:System.Windows.Forms.TextRenderer> , die einen annimmt <xref:System.Drawing.Point> . <xref:System.Windows.Forms.TextRenderer.DrawText%2A> erfordert auch <xref:System.Drawing.Color> und <xref:System.Drawing.Font> .  
  
 Die folgende Abbildung zeigt die Ausgabe von Text, der an einem angegebenen Punkt gezeichnet wird, wenn Sie die <xref:System.Drawing.Graphics.DrawString%2A> überladene-Methode verwenden.  
  
 ![Screenshot, der die Ausgabe von Text an einem angegebenen Punkt anzeigt.](./media/how-to-draw-text-at-a-specified-location/font-text-specified-point.png)  
  
### <a name="to-draw-a-line-of-text-with-gdi"></a>So zeichnen Sie eine Textzeile mit GDI+  
  
1. Verwenden Sie die- <xref:System.Drawing.Graphics.DrawString%2A> Methode, und übergeben Sie den gewünschten Text <xref:System.Drawing.Point> oder <xref:System.Drawing.PointF> , <xref:System.Drawing.Font> und <xref:System.Drawing.Brush> .  
  
     [!code-csharp[System.Drawing.AlignDrawnText#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#30)]
     [!code-vb[System.Drawing.AlignDrawnText#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#30)]  
  
### <a name="to-draw-a-line-of-text-with-gdi"></a>So zeichnen Sie eine Textzeile mit GDI  
  
1. Verwenden Sie die- <xref:System.Windows.Forms.TextRenderer.DrawText%2A> Methode, und übergeben Sie den gewünschten Text,, <xref:System.Drawing.Point> <xref:System.Drawing.Font> und <xref:System.Drawing.Color> .  
  
     [!code-csharp[System.Drawing.AlignDrawnText#40](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#40)]
     [!code-vb[System.Drawing.AlignDrawnText#40](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#40)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 In den vorherigen Beispielen ist Folgendes erforderlich:  
  
- <xref:System.Windows.Forms.PaintEventArgs>  `e`, bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md)
- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
- [Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten](how-to-construct-font-families-and-fonts.md)
- [Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck](how-to-draw-wrapped-text-in-a-rectangle.md)
