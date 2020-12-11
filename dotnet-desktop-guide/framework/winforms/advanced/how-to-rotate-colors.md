---
title: 'Vorgehensweise: Drehen von Farben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], rotating
- examples [Windows Forms], rotating colors
ms.assetid: e2e4c300-159c-4f4a-9b56-103b0f7cbc05
ms.openlocfilehash: 8d2717dd7b819e963126072279b361fda02188bc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976137"
---
# <a name="how-to-rotate-colors"></a>Vorgehensweise: Drehen von Farben
Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren. Wir können das Visualisieren der Rotation vereinfachen, indem wir akzeptieren, dass eine der Farbkomponenten korrigiert wird. Angenommen, die Alpha Komponente muss bei 1 (vollständig nicht transparent) korrigiert bleiben. Anschließend können wir einen dreidimensionalen Farbraum mit roten, grünen und blauen Achsen visualisieren, wie in der folgenden Abbildung dargestellt.  
  
 ![Abbildung, die die Drehung mit roten, grünen und blauen Achsen anzeigt.](./media/how-to-rotate-colors/rotation-red-green-blue-axes.gif)  
  
 Eine Farbe kann als Punkt im 3D-Raum betrachtet werden. Der Punkt (1, 0, 0) im Raum stellt z. b. die Farbe rot dar, und der Punkt (0, 1, 0) im Raum stellt die Farbe grün dar.  
  
 In der folgenden Abbildung wird gezeigt, was es bedeutet, die Farbe (1, 0, 0) durch einen Winkel von 60 Grad in der Red-Green Ebene zu drehen. Die Drehung in einer Ebene parallel zur Red-Green Ebene kann als Drehung der blauen Achse betrachtet werden.  
  
 ![Abbildung, die die Drehung der blauen Achse anzeigt.](./media/how-to-rotate-colors/rotation-about-blue-axis.gif)  
  
 In der folgenden Abbildung wird gezeigt, wie eine Farbmatrix initialisiert wird, um Drehungen zu jeder der drei Koordinatenachsen (rot, grün, blau) auszuführen:  
  
 ![Initialisieren Sie eine Farbmatrix, um Drehungen zu drei Achsen auszuführen.](./media/how-to-rotate-colors/rotation-about-three-axes.gif)  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Bild, das alle eine Farbe (1, 0, 0,6) ist, und eine 60-Grad-Drehung der blauen Achse angewendet. Der Winkel der Drehung wird in einer Ebene durchlaufen, die parallel zur roten grünen Ebene ist.  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das Farb gedrehte Bild auf der rechten Seite an:  
  
 ![Abbildung, die das ursprüngliche Bild und das Farb gedrehte Bild anzeigt.](./media/how-to-rotate-colors/original-color-rotated-images.png)  
  
 Die folgende Abbildung zeigt eine Visualisierung der Farb Drehung, die im folgenden Code ausgeführt wird:
  
 ![Abbildung, die die Visualisierung der Farb Drehung anzeigt.](./media/how-to-rotate-colors/visualization-color-rotation.gif)  
  
 [!code-csharp[System.Drawing.RotateColors#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RotateColors/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.RotateColors#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RotateColors/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist. Ersetzen `RotationInput.bmp` Sie dies durch einen Bilddateinamen und Pfad, der auf Ihrem System gültig ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Neueinfärben von Bildern](recoloring-images.md)
