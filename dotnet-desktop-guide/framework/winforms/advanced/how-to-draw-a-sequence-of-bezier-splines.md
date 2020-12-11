---
title: 'Gewusst wie: Zeichnen einer Sequenz von B&#233;Zier-Splines'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- splines [Windows Forms], drawing Bezier
- Bezier splines [Windows Forms], drawing sequence of
ms.assetid: 37a0bedb-20c2-4cf0-91fa-a5509e826b30
ms.openlocfilehash: 976787f5830282a581d05a9c24d1f83dceca4b25
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975942"
---
# <a name="how-to-draw-a-sequence-of-b233zier-splines"></a>Gewusst wie: Zeichnen einer Sequenz von B&#233;Zier-Splines
Mit der- <xref:System.Drawing.Graphics.DrawBeziers%2A> Methode der-Klasse können Sie <xref:System.Drawing.Graphics> eine Sequenz verbundener Bézier-Splines zeichnen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Kurve gezeichnet, die aus zwei verbundenen Bézier-Splines besteht. Der Endpunkt der ersten Bézier-Spline ist der Startpunkt der zweiten Bézier-Spline.  
  
 In der folgenden Abbildung werden die verbundenen Splines zusammen mit den sieben Punkten angezeigt:  
  
 ![Grafik, in der die verbundenen Splines zusammen mit sieben Punkten angezeigt werden.](./media/how-to-draw-a-sequence-of-bezier-splines/bezier-spline-seven-points.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Bézier-Splines in GDI+](bezier-splines-in-gdi.md)
- [Erstellen und Zeichnen von Kurven](constructing-and-drawing-curves.md)
