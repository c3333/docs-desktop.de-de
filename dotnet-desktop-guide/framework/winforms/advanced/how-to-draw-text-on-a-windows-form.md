---
title: 'Vorgehensweise: Zeichnen von Text in einem Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- forms [Windows Forms], drawing text
- text [Windows Forms], drawing
ms.assetid: 5d2447a9-21a1-4adc-b954-5516f2bb9b2c
ms.openlocfilehash: dc99a863765cd617c2ab4a636286f42f5e8daf79
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975926"
---
# <a name="how-to-draw-text-on-a-windows-form"></a>Vorgehensweise: Zeichnen von Text in einem Windows Form
Im folgenden Codebeispiel wird gezeigt, wie die- <xref:System.Drawing.Graphics.DrawString%2A> Methode von verwendet wird <xref:System.Drawing.Graphics> , um Text auf einem Formular zu zeichnen. Alternativ können Sie <xref:System.Windows.Forms.TextRenderer> zum Zeichnen von Text in einem Formular verwenden. Weitere Informationen finden Sie unter Gewusst [wie: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md).  
  
## <a name="example"></a>Beispiel  
 [!code-cpp[System.Drawing.ConceptualHowTos#7](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#7)]
 [!code-csharp[System.Drawing.ConceptualHowTos#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#7)]
 [!code-vb[System.Drawing.ConceptualHowTos#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#7)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Die-Methode kann nicht <xref:System.Drawing.Graphics.DrawString%2A> im- <xref:System.Windows.Forms.Form.Load> Ereignishandler aufgerufen werden. Der gezeichnete Inhalt wird nicht neu gezeichnet, wenn die Größe des Formulars geändert oder durch ein anderes Formular verdeckt wird. Damit Ihre Inhalte automatisch neu gezeichnet werden, sollten Sie die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode überschreiben.  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Die folgenden Bedingungen können einen Ausnahmefehler verursachen:  
  
- Die Schriftart "Arial" ist nicht installiert.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics.DrawString%2A>
- <xref:System.Windows.Forms.TextRenderer.DrawText%2A>
- <xref:System.Drawing.StringFormat.FormatFlags%2A>
- <xref:System.Drawing.StringFormatFlags>
- <xref:System.Windows.Forms.TextFormatFlags>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [Erste Schritte mit Grafikprogrammierung](getting-started-with-graphics-programming.md)
- [Vorgehensweise: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md)
