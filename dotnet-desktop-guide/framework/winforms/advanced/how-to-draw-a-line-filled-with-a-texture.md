---
title: 'Vorgehensweise: Zeichnen einer mit einer Textur ausgefüllten Linie'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], texture
- drawing lines [Windows Forms], texture
ms.assetid: dc9118cc-f3c2-42e5-8173-f46d41d18fd5
ms.openlocfilehash: c0f90c298f48aeb96893bb09241faddc08d8a49d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975954"
---
# <a name="how-to-draw-a-line-filled-with-a-texture"></a>Vorgehensweise: Zeichnen einer mit einer Textur ausgefüllten Linie
Anstatt eine Linie mit einer voll Tonfarbe zu zeichnen, können Sie eine Linie mit einer Textur zeichnen. Um Linien und Kurven mit einer Textur zu zeichnen, erstellen Sie ein <xref:System.Drawing.TextureBrush> -Objekt, und übergeben <xref:System.Drawing.TextureBrush> Sie das Objekt an einen <xref:System.Drawing.Pen.%23ctor%2A> Konstruktor. Die Bitmap, die dem Textur Pinsel zugeordnet ist, wird verwendet, um die Ebene (unsichtbar) zu Kacheln, und wenn der Stift eine Linie oder Kurve zeichnet, wird der Strich des Stifts bestimmte Pixel der Kachel Textur nicht abdecken.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Bitmap> Objekt aus der-Datei erstellt `Texture1.jpg` . Diese Bitmap wird zum Erstellen eines <xref:System.Drawing.TextureBrush> -Objekts verwendet, und das- <xref:System.Drawing.TextureBrush> Objekt wird verwendet, um ein-Objekt zu erstellen <xref:System.Drawing.Pen> . Der-Befehl <xref:System.Drawing.Graphics.DrawImage%2A> zeichnet die Bitmap mit der linken oberen Ecke bei (0,0). Der-Befehl <xref:System.Drawing.Graphics.DrawEllipse%2A> verwendet das- <xref:System.Drawing.Pen> Objekt, um eine strukturierte Ellipse zu zeichnen.  
  
 Die folgende Abbildung zeigt die Bitmap und die strukturierte Ellipse:  
  
 ![Screenshot, der die Bitmap und die strukturierte Ellipse anzeigt](./media/how-to-draw-a-line-filled-with-a-texture/bitmap-textured-ellipse.png)  
  
 [!code-csharp[System.Drawing.UsingAPen#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.UsingAPen#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Erstellen Sie ein Windows Form, und behandeln Sie das-Ereignis des Formulars <xref:System.Windows.Forms.Control.Paint> . Fügen Sie den vorangehenden Code in den- <xref:System.Windows.Forms.Control.Paint> Ereignishandler ein. Ersetzen `Texture.jpg` Sie dies durch ein gültiges Bild auf Ihrem System.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
