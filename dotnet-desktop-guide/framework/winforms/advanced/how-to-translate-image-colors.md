---
title: 'Vorgehensweise: Verschieben von Bildfarben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [Windows Forms], changing colors
- images [Windows Forms], changing colors
- image colors [Windows Forms]
ms.assetid: 2106fb9a-4d60-4dcf-9220-9f189a6c4d19
ms.openlocfilehash: fb9ec30c06740214b8dc6b65d32eba4e2920c89b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976111"
---
# <a name="how-to-translate-image-colors"></a>Vorgehensweise: Verschieben von Bildfarben
Eine Übersetzung Fügt einer oder mehreren der vier Farbkomponenten einen Wert hinzu. Die Farbmatrix Einträge, die Übersetzungen darstellen, werden in der folgenden Tabelle angegeben.  
  
|Zu über setzende Komponente|Matrix Eintrag|  
|--------------------------------|------------------|  
|Red|[4][0]|  
|Grün|[4][1]|  
|Blau|[4][2]|  
|Alpha|[4][3]|  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars.bmp erstellt. Anschließend fügt der Code der roten Komponente jedes Pixels im Bild 0,75 hinzu. Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite an:  
  
 ![Screenshot des ursprünglichen und transformierten Bilds.](./media/how-to-translate-image-colors/original-image-translate-colors.png)  
  
 In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der roten Übersetzung aufgelistet. Beachten Sie, dass die rote Komponente in der zweiten Zeile nicht geändert wird, da der Höchstwert für eine Farbkomponente 1 ist. (Auf ähnliche Weise ist der minimale Wert für eine Farbkomponente 0.)  
  
|Original|Übersetzt|  
|--------------|----------------|  
|Schwarz (0,0 (0, 0, 1)|(0.75, 0, 0, 1)|  
|Rot (1, 0, 0, 1)|(1, 0, 0, 1)|  
|Grün (0, 1, 0, 1)|(0.75, 1, 0, 1)|  
|Blau (0,0 (0, 1, 1)|(0.75, 0, 1, 1)|  
  
 [!code-csharp[System.Drawing.RecoloringImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.RecoloringImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist. Ersetzen `ColorBars.bmp` Sie dies durch einen Bilddateinamen und-Pfad, die auf Ihrem System gültig sind.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Neueinfärben von Bildern](recoloring-images.md)
