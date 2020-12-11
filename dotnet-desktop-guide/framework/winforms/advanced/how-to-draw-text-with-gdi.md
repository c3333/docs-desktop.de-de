---
title: 'Vorgehensweise: Zeichnen von Text mit GDI'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI [Windows Forms], drawing text [Windows Forms]
- text [Windows Forms], drawing with TextRenderer
- drawing [Windows Forms], text
- Windows Forms, drawing text with GDI
ms.assetid: 2a19fe5d-2ace-451c-94db-01cb1118ef7b
ms.openlocfilehash: 3ed2b5c94e4a38a5873a34e61287c4038cab5cbb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975924"
---
# <a name="how-to-draw-text-with-gdi"></a>Vorgehensweise: Zeichnen von Text mit GDI
Mit der- <xref:System.Windows.Forms.TextRenderer.DrawText%2A> Methode in der- <xref:System.Windows.Forms.TextRenderer> Klasse können Sie auf die GDI-Funktionalität zum Zeichnen von Text in einem Formular oder Steuerelement zugreifen. Das GDI-Text Rendering bietet in der Regel eine bessere Leistung und eine präzisere Text Messung als GDI+.  
  
> [!NOTE]
> Die <xref:System.Windows.Forms.TextRenderer.DrawText%2A> Methoden der- <xref:System.Windows.Forms.TextRenderer> Klasse werden zum Drucken nicht unterstützt. Wenn Sie drucken, verwenden Sie immer die <xref:System.Drawing.Graphics.DrawString%2A> Methoden der- <xref:System.Drawing.Graphics> Klasse.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie Sie mithilfe der-Methode Text in mehreren Zeilen innerhalb eines Rechtecks zeichnen <xref:System.Windows.Forms.TextRenderer.DrawText%2A> .  
  
 [!code-csharp[System.Windows.Forms.TextRendererExamples#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TextRendererExamples/CS/Form1.cs#7)]
 [!code-vb[System.Windows.Forms.TextRendererExamples#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TextRendererExamples/VB/Form1.vb#7)]  
  
 Zum Rendering von Text mit der- <xref:System.Windows.Forms.TextRenderer> Klasse benötigen Sie <xref:System.Drawing.IDeviceContext> , wie z. b. <xref:System.Drawing.Graphics> und <xref:System.Drawing.Font> , einen Speicherort zum Zeichnen des Texts und die Farbe, in der der Text gezeichnet werden soll. Optional können Sie die Textformatierung mithilfe der- <xref:System.Windows.Forms.TextFormatFlags> Enumeration angeben.  
  
 Weitere Informationen zum Abrufen eines <xref:System.Drawing.Graphics> finden Sie unter Gewusst [wie: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md). Weitere Informationen zum Erstellen einer <xref:System.Drawing.Font> finden Sie unter Gewusst [wie: Erstellen von Schriftart Familien und Schriftarten](how-to-construct-font-families-and-fonts.md).  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorangehende Codebeispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.TextRenderer>
- <xref:System.Drawing.Font>
- <xref:System.Drawing.Color>
- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
