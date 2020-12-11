---
title: 'Vorgehensweise: Zeichnen von kardinalen Splines'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cardinal splines [Windows Forms], drawing
- drawing [Windows Forms], cardinal splines
- graphics [Windows Forms], cardinal splines
ms.assetid: a4a41e80-4461-4b47-b6bd-2c5e68881994
ms.openlocfilehash: 12e938567d529b33ead93e081d380a650a803f23
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975931"
---
# <a name="how-to-draw-cardinal-splines"></a>Vorgehensweise: Zeichnen von kardinalen Splines
Eine kardinale Splinekurve ist eine Kurve, die durch einen bestimmten Satz von Punkten reibungslos verläuft. Um einen kardinalspline zu zeichnen, erstellen Sie ein <xref:System.Drawing.Graphics> -Objekt, und übergeben Sie die Adresse eines Arrays von Punkten an die- <xref:System.Drawing.Graphics.DrawCurve%2A> Methode.  
  
### <a name="drawing-a-bell-shaped-cardinal-spline"></a>Zeichnen eines Bell-Shaped kardinalspline  
  
- Im folgenden Beispiel wird ein glockenförmiger kardinaler Spline gezeichnet, der fünf festgelegte Punkte durchläuft. In der folgenden Abbildung werden die Kurve und fünf Punkte dargestellt.  
  
     ![Diagramm, das einen glockenförmigen kardinalspline anzeigt.](./media/how-to-draw-cardinal-splines/bell-shaped-cardinal-spline.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#21)]  
  
### <a name="drawing-a-closed-cardinal-spline"></a>Zeichnen einer geschlossenen kardinalspline  
  
- Verwenden Sie die- <xref:System.Drawing.Graphics.DrawClosedCurve%2A> Methode der- <xref:System.Drawing.Graphics> Klasse, um einen geschlossenen kardinalspline zu zeichnen. In einer geschlossenen kardinalsplinekurve wird die Kurve bis zum letzten Punkt im Array fortgesetzt und stellt eine Verbindung mit dem ersten Punkt im Array her. Im folgenden Beispiel wird eine geschlossene kardinale Spline gezeichnet, die sechs festgelegte Punkte durchläuft. Die folgende Abbildung zeigt den geschlossenen Spline zusammen mit den sechs Punkten:  
  
 ![Diagramm, das einen geschlossenen kardinalspline anzeigt.](./media/how-to-draw-cardinal-splines/closed-cardinal-spine.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#22)]  
  
### <a name="changing-the-bend-of-a-cardinal-spline"></a>Ändern der Kurve eines kardinalen Spline  
  
- Ändern Sie die Art und Weise, in der sich ein kardinaler Spline mit einem Spannungs Argument an die <xref:System.Drawing.Graphics.DrawCurve%2A> Methode beugt. Im folgenden Beispiel werden drei kardinale Splines gezeichnet, die denselben Satz von Punkten durchlaufen. Die folgende Abbildung zeigt die drei Splines zusammen mit Ihren Spannungswerten. Beachten Sie, dass die Punkte durch gerade Linien verbunden sind, wenn die Spannung den Wert 0 hat.  
  
 ![Diagramm, das drei kardinale Splines anzeigt.](./media/how-to-draw-cardinal-splines/three-cardinal-splines.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#23)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#23)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Die vorhergehenden Beispiele sind für die Verwendung mit Windows Forms konzipiert und erfordern <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Erstellen und Zeichnen von Kurven](constructing-and-drawing-curves.md)
