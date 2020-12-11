---
title: 'Vorgehensweise: Festlegen von Stiftbreite und -ausrichtung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pens [Windows Forms], setting width
- pens [Windows Forms], setting alignment
ms.assetid: a202af36-4d31-4401-a126-b232f51db581
ms.openlocfilehash: 1f1ea6e8ef0b94aa46a4bf8177d59e59297d6e3f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976128"
---
# <a name="how-to-set-pen-width-and-alignment"></a>Vorgehensweise: Festlegen von Stiftbreite und -ausrichtung
Wenn Sie ein-Element erstellen <xref:System.Drawing.Pen> , können Sie die Stift Breite als eines der Argumente für den Konstruktor angeben. Sie können auch die Stift Breite mit der- <xref:System.Drawing.Pen.Width%2A> Eigenschaft der- <xref:System.Drawing.Pen> Klasse ändern.  
  
 Eine theoretische Linie hat eine Breite von 0. Wenn Sie eine Linie zeichnen, die 1 Pixel breit ist, werden die Pixel auf der theoretischen Linie zentriert. Wenn Sie eine Linie zeichnen, die mehr als ein Pixel breit ist, werden die Pixel entweder in der theoretischen Linie zentriert oder bis zu einer Seite der theoretischen Linie angezeigt. Sie können die Eigenschaft Pen Alignment eines festlegen <xref:System.Drawing.Pen> , um zu bestimmen, wie die mit diesem Stift gezeichneten Pixel in Bezug auf die theoretischen Linien positioniert werden.  
  
 Die Werte <xref:System.Drawing.Drawing2D.PenAlignment.Center> , <xref:System.Drawing.Drawing2D.PenAlignment.Outset> und <xref:System.Drawing.Drawing2D.PenAlignment.Inset> , die in den folgenden Codebeispielen angezeigt werden, sind Member der- <xref:System.Drawing.Drawing2D.PenAlignment> Enumeration.  
  
 Im folgenden Codebeispiel wird eine Linie zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.  
  
### <a name="to-vary-the-width-of-a-pen"></a>So verändern Sie die Breite eines Stifts  
  
- Legen Sie den Wert der- <xref:System.Drawing.Pen.Alignment%2A> Eigenschaft auf <xref:System.Drawing.Drawing2D.PenAlignment.Center> (die Standardeinstellung) fest, um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel auf der theoretischen Linie zentriert werden. Die folgende Abbildung zeigt die resultierende Zeile.  
  
     ![Eine schwarze dünne Linie mit grüner Hervorhebung.](./media/how-to-set-pen-width-and-alignment/green-pixels-centered-line.gif)  
  
     Im folgenden Codebeispiel wird ein Rechteck zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.  
  
     [!code-csharp[System.Drawing.UsingAPen#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#41)]
     [!code-vb[System.Drawing.UsingAPen#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#41)]  
  
### <a name="to-change-the-alignment-of-a-pen"></a>So ändern Sie die Ausrichtung eines Stifts  
  
- Legen Sie den Wert der-Eigenschaft auf fest, <xref:System.Drawing.Pen.Alignment%2A> <xref:System.Drawing.Drawing2D.PenAlignment.Center> um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel auf der Grenze des Rechtecks zentriert werden.  
  
     Die folgende Abbildung zeigt das resultierende Rechteck:
  
     ![Ein Rechteck, das mit schwarzen, schmalen Linien mit grüner Hervorhebung gezeichnet wird.](./media/how-to-set-pen-width-and-alignment/green-pixels-centered-rectangle.gif)  
  
     [!code-csharp[System.Drawing.UsingAPen#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#42)]
     [!code-vb[System.Drawing.UsingAPen#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#42)]  
  
### <a name="to-create-an-inset-pen"></a>So erstellen Sie einen einfügen-Stift  
  
- Ändern Sie die Ausrichtung des grünen Stifts, indem Sie die dritte Anweisung im vorangehenden Codebeispiel wie folgt ändern:  
  
     [!code-csharp[System.Drawing.UsingAPen#43](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#43)]
     [!code-vb[System.Drawing.UsingAPen#43](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#43)]  
  
     Nun werden die Pixel in der Breite grünen Linie im Inneren des Rechtecks angezeigt, wie in der folgenden Abbildung dargestellt:
  
     ![Ein Rechteck, das mit schwarzen Linien mit der Breite grünen Linie in gezeichnet wird.](./media/how-to-set-pen-width-and-alignment/green-pixels-inside-rectangle.gif)  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
