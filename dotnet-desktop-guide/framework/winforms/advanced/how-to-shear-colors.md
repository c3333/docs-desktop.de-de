---
title: 'Vorgehensweise: Scheren von Farben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], transforming with color matrices
- colors [Windows Forms], shearing
ms.assetid: 0a424171-5b8b-45c4-afef-e9720a6c3e22
ms.openlocfilehash: 825e5a90ebb0d9df3b894ce7bd353e917b676939
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975876"
---
# <a name="how-to-shear-colors"></a>Vorgehensweise: Scheren von Farben
Durch das Scheren wird eine Farbkomponente um einen in einer anderen Farbkomponente proportionalen Betrag vergrößert oder verringert. Nehmen Sie z. b. die Transformation, bei der die rote Komponente um einen halben Wert der blauen Komponente erweitert wird. Bei einer solchen Transformation würde die Farbe (0,2, 0,5, 1) zu (0,7, 0,5, 1) werden. Die neue rote Komponente ist 0,2 + (1/2) (1) = 0,7.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars4.bmp erstellt. Anschließend wendet der Code die im vorherigen Absatz beschriebene Scheren Transformation auf jedes Pixel im Bild an.  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das auf der rechten Seite gelauftene Bild:
  
 ![Zwei Quadrate mit farbiger farbiger Seite und Darstellung des ursprünglichen Bilds und des gerenderten Bilds.](./media/how-to-shear-colors/original-image-sheared-image.png)  
  
 In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der Transformation für das Scheren-Diagramm aufgelistet.  
  
|Original|Zert|  
|--------------|-------------|  
|(0, 0, 1, 1)|(0.5, 0, 1, 1)|  
|(0.5, 1, 0.5, 1)|(0.75, 1, 0.5, 1)|  
|(1, 1, 0, 1)|(1, 1, 0, 1)|  
|(0.4, 0.4, 0.4, 1)|(0.6, 0.4, 0.4, 1)|  
  
 [!code-csharp[System.Drawing.Misc3#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Misc3/CS/Form1.cs#9)]
 [!code-vb[System.Drawing.Misc3#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Misc3/VB/Form1.vb#9)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist. Ersetzen `ColorBars.bmp` Sie dies durch einen Bildnamen und einen Pfad, der auf Ihrem System gültig ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Neueinfärben von Bildern](recoloring-images.md)
