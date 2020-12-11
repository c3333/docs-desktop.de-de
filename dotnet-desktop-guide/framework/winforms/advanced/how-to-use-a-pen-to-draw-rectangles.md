---
title: 'Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Rechtecken'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- rectangles [Windows Forms], drawing
- pens [Windows Forms], drawing rectangles
ms.assetid: 54a7fa14-3ad8-4d64-b424-2a12005b250c
ms.openlocfilehash: cd5d965f8b92d15cdeb3049330d9b3cc0de893b2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975855"
---
# <a name="how-to-use-a-pen-to-draw-rectangles"></a>Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Rechtecken
Um Rechtecke zu zeichnen, benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt. Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawRectangle%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Funktionen der Zeile, z. b. Farbe und Breite.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (10, 10) gezeichnet. Das Rechteck hat eine Breite von 100 und eine Höhe von 50. Das zweite Argument, das an den <xref:System.Drawing.Pen.%23ctor%2A> Konstruktor übergeben wird, gibt an, dass die Stift Breite 5 Pixel beträgt.  
  
 Wenn das Rechteck gezeichnet wird, wird der Stift auf die Begrenzung des Rechtecks zentriert. Da die Stift Breite 5 beträgt, werden die Seiten des Rechtecks 5 Pixel breit gezeichnet, sodass 1 Pixel an der Grenze selbst gezeichnet wird, 2 Pixel im inneren gezeichnet werden und 2 Pixel auf der Außenseite gezeichnet werden. Weitere Informationen zur Ausrichtung von Pen finden Sie unter Gewusst [wie: Festlegen der Stift Breite und-Ausrichtung](how-to-set-pen-width-and-alignment.md).  
  
 Die folgende Abbildung zeigt das resultierende Rechteck. Die gepunkteten Linien zeigen an, wo das Rechteck gezeichnet worden wäre, wenn die Stift Breite ein Pixel gewesen wäre. Die erweiterte Ansicht der oberen linken Ecke des Rechtecks zeigt, dass die dicken schwarzen Linien auf diese gepunkteten Linien zentriert sind.  
  
 ![Screenshot, der das gezeichnete Rechteck mit schwarzen und gepunkteten Linien anzeigt](./media/how-to-use-a-pen-to-draw-rectangles/drawn-rectangle-black-lines-dotted-lines.gif)  
  
 [!code-csharp[System.Drawing.UsingAPen#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.UsingAPen#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
