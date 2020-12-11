---
title: 'Gewusst wie: Zeichnen eines einzelnen B-&#233;Zier-Spline'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines [Windows Forms], drawing
- drawing [Windows Forms], Bezier splines
ms.assetid: f4f3fe30-f0a6-4743-ac91-11310cebea9f
ms.openlocfilehash: ebb53e7df979a553ed4a44deba34345c9ecac772
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975941"
---
# <a name="how-to-draw-a-single-b233zier-spline"></a>Gewusst wie: Zeichnen eines einzelnen B-&#233;Zier-Spline
Eine Bézier-Spline wird von vier Punkten definiert: einem Startpunkt, zwei Kontrollpunkten und einem Endpunkt.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Bézier-Spline mit dem Startpunkt (10, 100) und dem Endpunkt (200, 100) gezeichnet. Die Kontrollpunkte lauten (100, 10) und (150, 150).  
  
 In der folgenden Abbildung wird der resultierende Bézier-Spline zusammen mit dem Startpunkt, den Kontrollpunkten und dem Endpunkt dargestellt. Die Abbildung zeigt auch die zusammen Geviert-Hülle des Splines, bei der es sich um ein Polygon handelt, das durch Verbinden der vier Punkte mit geraden Linien gebildet wird.  
  
 ![Abbildung einer Bezier-Spline.](./media/how-to-draw-a-single-bezier-spline/bezier-spline-illustration.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics.DrawBezier%2A>
- [Bézier-Splines in GDI+](bezier-splines-in-gdi.md)
- [Vorgehensweise: Zeichnen einer Folge von Bézier-Splines](how-to-draw-a-sequence-of-bezier-splines.md)
