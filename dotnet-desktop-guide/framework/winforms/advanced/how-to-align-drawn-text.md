---
title: 'Vorgehensweise: Ausrichten von gezeichnetem Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], aligning
- Windows Forms, aligning drawn text
ms.assetid: 83c10a81-1a90-4b5c-98aa-2c6c4b280079
ms.openlocfilehash: 3a569284a1c4b43fa7264e0354934436f95b8dc3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972383"
---
# <a name="how-to-align-drawn-text"></a>Vorgehensweise: Ausrichten von gezeichnetem Text
Wenn Sie eine benutzerdefinierte Zeichnung durchführen, können Sie den gezeichneten Text häufig in einem Formular oder Steuerelement zentrieren. Sie können mit der-Methode oder der-Methode gezeichneter Text problemlos ausrichten, <xref:System.Drawing.Graphics.DrawString%2A> <xref:System.Windows.Forms.TextRenderer.DrawText%2A> indem Sie das richtige Formatierungs Objekt erstellen und die entsprechenden Formatflags festlegen.  
  
### <a name="to-draw-centered-text-with-gdi-drawstring"></a>So zeichnen Sie zentrierten Text mit GDI+ (DrawString)  
  
1. Verwenden <xref:System.Drawing.StringFormat> Sie eine mit der entsprechenden- <xref:System.Drawing.Graphics.DrawString%2A> Methode, um zentrierten Text anzugeben.  
  
     [!code-csharp[System.Drawing.AlignDrawnText#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#10)]
     [!code-vb[System.Drawing.AlignDrawnText#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#10)]  
  
### <a name="to-draw-centered-text-with-gdi-drawtext"></a>So zeichnen Sie zentrierten Text mit GDI (DrawText)  
  
1. Verwenden Sie die <xref:System.Windows.Forms.TextFormatFlags> -Enumeration zum umwickeln und vertikalen und horizontalen Zentrieren von Text mit der entsprechenden- <xref:System.Windows.Forms.TextRenderer.DrawText%2A> Methode.  
  
     [!code-csharp[System.Drawing.AlignDrawnText#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#20)]
     [!code-vb[System.Drawing.AlignDrawnText#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#20)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Die vorangehenden Codebeispiele sind für die Verwendung mit Windows Forms konzipiert und erfordern <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md)
- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
- [Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten](how-to-construct-font-families-and-fonts.md)
