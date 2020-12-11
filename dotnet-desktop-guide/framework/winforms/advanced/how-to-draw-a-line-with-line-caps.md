---
title: 'Vorgehensweise: Zeichnen einer Linie mit Linienenden'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
- drawing lines [Windows Forms], line caps
ms.assetid: eb68c3e1-c400-4886-8a04-76978a429cb6
ms.openlocfilehash: 34abfc86e980a24ebb835cfd88d2522f8372c68d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975946"
---
# <a name="how-to-draw-a-line-with-line-caps"></a>Vorgehensweise: Zeichnen einer Linie mit Linienenden
Sie können den Anfang oder das Ende einer Linie in einer von mehreren Formen zeichnen, die als Linien Caps bezeichnet werden. GDI+ unterstützt mehrere Linien Kappen, z. b. Round, Square, Diamond und Arrowhead.  
  
## <a name="example"></a>Beispiel  
 Sie können für den Anfang einer Linie (Start-Obergrenze), das Ende einer Linie (Ende) oder die Bindestriche einer gestrichelten Linie (Bindestrich) Zeilenenden angeben.  
  
 Im folgenden Beispiel wird eine Linie mit einem Pfeilspitzen an einem Ende und einem Rundenende am anderen Ende gezeichnet. Die Abbildung zeigt die resultierende Zeile:  
  
 ![Abbildung, die eine Linie mit einem Rundenende anzeigt.](./media/how-to-draw-a-line-with-line-caps/line-cap-arrowhead-example.gif)  
  
 [!code-csharp[System.Drawing.UsingAPen#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.UsingAPen#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
  
- Erstellen Sie ein Windows Form, und behandeln Sie das-Ereignis des Formulars <xref:System.Windows.Forms.Control.Paint> . Fügen Sie den Beispielcode in den Ereignishandler ein, der <xref:System.Windows.Forms.Control.Paint> als übergeben wird `e` <xref:System.Windows.Forms.PaintEventArgs> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Drawing2D.LineCap?displayProperty=nameWithType>
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
