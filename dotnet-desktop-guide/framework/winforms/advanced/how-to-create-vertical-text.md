---
title: 'Vorgehensweise: Erstellen von vertikalem Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing vertical
- Windows Forms, drawing vertical text
- strings [Windows Forms], drawing vertical
- vertical text [Windows Forms], drawing
ms.assetid: 50c69046-4188-47d9-b949-cc2610ffd337
ms.openlocfilehash: 86401342625f593945b801f7619ef9ca9681317c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972362"
---
# <a name="how-to-create-vertical-text"></a>Vorgehensweise: Erstellen von vertikalem Text
Sie können ein- <xref:System.Drawing.StringFormat> Objekt verwenden, um anzugeben, dass Text vertikal und nicht horizontal gezeichnet werden soll.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird der-Wert der- <xref:System.Drawing.StringFormatFlags.DirectionVertical> <xref:System.Drawing.StringFormat.FormatFlags%2A> Eigenschaft eines- <xref:System.Drawing.StringFormat> Objekts zugewiesen. Dieses <xref:System.Drawing.StringFormat> Objekt wird an die- <xref:System.Drawing.Graphics.DrawString%2A> Methode der- <xref:System.Drawing.Graphics> Klasse übermittelt. Der Wert <xref:System.Drawing.StringFormatFlags.DirectionVertical> ist ein Member der- <xref:System.Drawing.StringFormatFlags> Enumeration.  
  
 Die folgende Abbildung zeigt den vertikalen Text:
  
 ![Grafik, die vertikalen Schriftart Text zeigt.](./media/how-to-create-vertical-text/vertical-font-text-graphic.png)  
  
 [!code-csharp[System.Drawing.FontsAndText#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.FontsAndText#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
  
- Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md)
