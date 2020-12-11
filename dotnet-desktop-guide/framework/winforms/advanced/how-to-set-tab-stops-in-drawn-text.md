---
title: 'Vorgehensweise: Festlegen von Tabstopps in gezeichnetem Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing with tab stops
- tabs [Windows Forms], drawn text
ms.assetid: 64878f98-39ba-4303-b63f-0859ab682eeb
ms.openlocfilehash: 8821f6170b8ba588e3197ef54eab14c2719a6cc3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975881"
---
# <a name="how-to-set-tab-stops-in-drawn-text"></a>Vorgehensweise: Festlegen von Tabstopps in gezeichnetem Text
Sie können Tabstopps für Text festlegen, indem Sie die <xref:System.Drawing.StringFormat.SetTabStops%2A> -Methode eines <xref:System.Drawing.StringFormat> -Objekts aufrufen und dieses <xref:System.Drawing.StringFormat> Objekt anschließend an die- <xref:System.Drawing.Graphics.DrawString%2A> Methode der-Klasse übergeben <xref:System.Drawing.Graphics> .  
  
> [!NOTE]
> <xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType>Unterstützt das Hinzufügen von Tabstopps zum Zeichnen von Text nicht, obwohl Sie vorhandene Tabstopps mit dem-Flag erweitern können <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird der Tabstopp bei 150, 250 und 350 festgelegt. Anschließend wird im Code eine Liste mit Namen und testbewertungen im Registerkarten Format angezeigt.  
  
 Die folgende Abbildung zeigt den Text im Registerkarten Format:  
  
 ![Screenshot, der eine Liste mit Namen und Bewertungen im Registerkarten Format anzeigt.](./media/how-to-set-tab-stops-in-drawn-text/tab-list-names-test-scores.png)  
  
 Der folgende Code übergibt zwei Argumente an die- <xref:System.Drawing.StringFormat.SetTabStops%2A> Methode. Das zweite Argument ist ein Array, das Tabulator Offsets enthält. Das erste an übergebenen Argument ist 0 (null) <xref:System.Drawing.StringFormat.SetTabStops%2A> , womit angegeben wird, dass der erste Offset im Array von Position 0, dem linken Rand des umgebenden Rechtecks, gemessen wird.  
  
 [!code-csharp[System.Drawing.FontsAndText#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.FontsAndText#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
  
- Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
- [Vorgehensweise: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md)
