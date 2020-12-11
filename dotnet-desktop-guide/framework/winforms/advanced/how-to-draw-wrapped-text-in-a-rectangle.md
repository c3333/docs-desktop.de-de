---
title: 'Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, drawing text in a rectangle
- text [Windows Forms], drawing in a rectangle
- strings [Windows Forms], drawing in a rectangle
ms.assetid: e1fb432a-dc90-48b5-9b6b-acc14507133d
ms.openlocfilehash: ace79e45737a3ce26d8bdcd603e923c1e6040d4d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975915"
---
# <a name="how-to-draw-wrapped-text-in-a-rectangle"></a>Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck
Mit der <xref:System.Drawing.Graphics.DrawString%2A> überladenen-Methode der- <xref:System.Drawing.Graphics> Klasse, die einen-oder-Parameter annimmt, können Sie eingeschlossene Text in einem Rechteck zeichnen <xref:System.Drawing.Rectangle> <xref:System.Drawing.RectangleF> . Außerdem verwenden Sie eine <xref:System.Drawing.Brush> und eine <xref:System.Drawing.Font> .  
  
 Sie können auch eingeschlossene Text in einem Rechteck zeichnen, indem Sie die <xref:System.Windows.Forms.TextRenderer.DrawText%2A> überladene-Methode der verwenden <xref:System.Windows.Forms.TextRenderer> , die einen <xref:System.Drawing.Rectangle> -Parameter und einen- <xref:System.Windows.Forms.TextFormatFlags> Parameter annimmt. Außerdem verwenden Sie eine <xref:System.Drawing.Color> und eine <xref:System.Drawing.Font> .  
  
 Die folgende Abbildung zeigt die Ausgabe von Text, der im Rechteck gezeichnet wird, wenn Sie die- <xref:System.Drawing.Graphics.DrawString%2A> Methode verwenden:
  
 ![Screenshot, der die Ausgabe zeigt, wenn die DrawString-Methode verwendet wird.](./media/how-to-draw-wrapped-text-in-a-rectangle/drawstring-method-font-text.png)  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a>So zeichnen Sie umschließenen Text in einem Rechteck mit GDI+  
  
1. Verwenden <xref:System.Drawing.Graphics.DrawString%2A> Sie die überladene-Methode, und übergeben Sie den gewünschten Text, <xref:System.Drawing.Rectangle> oder <xref:System.Drawing.RectangleF> <xref:System.Drawing.Font> und <xref:System.Drawing.Brush> .  
  
     [!code-csharp[System.Drawing.AlignDrawnText#50](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#50)]
     [!code-vb[System.Drawing.AlignDrawnText#50](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#50)]  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a>So zeichnen Sie umschließenen Text in einem Rechteck mit GDI  
  
1. Verwenden Sie den- <xref:System.Windows.Forms.TextFormatFlags> Enumerationswert, um anzugeben, dass der Text mit der <xref:System.Windows.Forms.TextRenderer.DrawText%2A> überladenen Methode umschließt werden soll, und übergeben Sie den gewünschten Text, <xref:System.Drawing.Rectangle> <xref:System.Drawing.Font> und <xref:System.Drawing.Color> .  
  
     [!code-csharp[System.Drawing.AlignDrawnText#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#60)]
     [!code-vb[System.Drawing.AlignDrawnText#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#60)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 In den vorherigen Beispielen ist Folgendes erforderlich:  
  
- <xref:System.Windows.Forms.PaintEventArgs>`e`, bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md)
- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
- [Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten](how-to-construct-font-families-and-fonts.md)
- [Vorgehensweise: Zeichnen von Text an einer angegebenen Position](how-to-draw-text-at-a-specified-location.md)
