---
title: 'Vorgehensweise: Verknüpfen von Linien'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- miter line join style
- bevel line join style
- line join
- drawing [Windows Forms], joining lines
- GraphicsPath object
- round line join style
- lines [Windows Forms], joining
- graphics [Windows Forms], joining lines
ms.assetid: 9fc480c2-3c75-4fd1-8ab5-296a99e820e2
ms.openlocfilehash: 362ce0c701d6e5f640fecd143a60cf471045629c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976156"
---
# <a name="how-to-join-lines"></a>Vorgehensweise: Verknüpfen von Linien
Ein Zeilen Beitritt ist der gemeinsame Bereich, der durch zwei Zeilen gebildet wird, deren enden sich überlappen. GDI+ bietet drei zeilige joinstile: Miter, Abschrägung und Round. Der linienjoinstil ist eine Eigenschaft der- <xref:System.Drawing.Pen> Klasse. Wenn Sie einen linienjoinstil für ein- <xref:System.Drawing.Pen> Objekt angeben, wird dieser joinstil auf alle verbundenen Linien in jedem Objekt angewendet, das <xref:System.Drawing.Drawing2D.GraphicsPath> mit diesem Stift gezeichnet wird.  
  
 In der folgenden Abbildung sind die Ergebnisse des Beispiels für ein gepuffertes Zeilen Verknüpfungs Beispiel dargestellt.  
  
 ![Abbildung, in der joinlinien angezeigt werden.](./media/how-to-join-lines/joined-beveled-lines.gif)  
  
## <a name="example"></a>Beispiel  
 Sie können den linienjoinstil mithilfe der- <xref:System.Drawing.Pen.LineJoin%2A> Eigenschaft der- <xref:System.Drawing.Pen> Klasse angeben. Das Beispiel veranschaulicht einen gevelten Zeilen Beitritt zwischen einer horizontalen Linie und einer vertikalen Linie. Im folgenden Code ist der Wert, der <xref:System.Drawing.Drawing2D.LineJoin.Bevel> der- <xref:System.Drawing.Pen.LineJoin%2A> Eigenschaft zugewiesen ist, ein Member der- <xref:System.Drawing.Drawing2D.LineJoin> Enumeration. Die anderen Member der <xref:System.Drawing.Drawing2D.LineJoin> -Enumeration sind <xref:System.Drawing.Drawing2D.LineJoin.Miter> und <xref:System.Drawing.Drawing2D.LineJoin.Round> .  
  
 [!code-csharp[System.Drawing.UsingAPen#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingAPen#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
