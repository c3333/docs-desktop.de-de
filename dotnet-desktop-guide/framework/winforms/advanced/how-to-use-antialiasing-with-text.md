---
title: 'Vorgehensweise: Verwenden der Bildkantenglättung mit Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- strings [Windows Forms], smoothing drawn
- antialiasing [Windows Forms], using with text
- text [Windows Forms], smoothing
- text [Windows Forms], antialiasing
- strings [Windows Forms], antialiasing when drawing
ms.assetid: 48fc34f3-f236-4b01-a0cb-f0752e6d22ae
ms.openlocfilehash: 632ed329173d134495a424b34ca7c71e402607bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976105"
---
# <a name="how-to-use-antialiasing-with-text"></a>Vorgehensweise: Verwenden der Bildkantenglättung mit Text
*Antialiasing* bezieht sich auf die Glättung von verzweigten Kanten von gezeichneten Grafiken und Text, um deren Darstellung oder Lesbarkeit zu verbessern. Mit den verwalteten GDI+-Klassen können Sie einen hochwertigen Text mit Antialiasing und niedrigerer Qualität rendert. In der Regel benötigt das Rendern höherer Qualität mehr Verarbeitungszeit als das Rendering mit niedrigerer Qualität. Um den Text Qualitätsgrad festzulegen, legen <xref:System.Drawing.Graphics.TextRenderingHint%2A> Sie die-Eigenschaft eines <xref:System.Drawing.Graphics> auf eines der Elemente der- <xref:System.Drawing.Text.TextRenderingHint> Enumeration fest.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird Text mit zwei verschiedenen Qualitätseinstellungen gezeichnet.  
  
 [!code-csharp[System.Drawing.FontsAndText#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.FontsAndText#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#21)]  

 Die folgende Abbildung zeigt die Ausgabe des Beispielcodes:  
  
 ![Screenshot, der Text mit zwei verschiedenen Qualitätseinstellungen anzeigt.](./media/how-to-use-antialiasing-with-text/antialiasing-text-quality-settings.png)  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorangehende Codebeispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , dass ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
