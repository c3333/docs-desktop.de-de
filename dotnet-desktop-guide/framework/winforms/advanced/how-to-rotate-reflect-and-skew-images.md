---
title: 'Vorgehensweise: Drehen, Spiegeln und Neigen von Bildern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], reflecting
- images [Windows Forms], rotating
- images [Windows Forms], skewing
ms.assetid: a3bf97eb-63ed-425a-ba07-dcc65efb567c
ms.openlocfilehash: 80ac92d545d9be7a4a611038eaaadbbdbe2e8ecf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975884"
---
# <a name="how-to-rotate-reflect-and-skew-images"></a>Vorgehensweise: Drehen, Spiegeln und Neigen von Bildern
Sie können ein Bild drehen, reflektieren und verzerren, indem Sie Zielpunkte für die obere linke, obere Rechte und untere linke Ecke des ursprünglichen Bilds angeben. Die drei Zielpunkte bestimmen eine affine Transformation, die das ursprüngliche rechteckige Bild einem Parallelogram zuordnet.  
  
## <a name="example"></a>Beispiel  
 Angenommen, das ursprüngliche Bild ist ein Rechteck mit der oberen linken Ecke bei (0,0), der oberen rechten Ecke bei (100, 0) und der unteren linken Ecke bei (0, 50). Nehmen Sie nun an, dass Sie die drei Punkte den Zielpunkten wie folgt zuordnen.  
  
|Ursprünglicher Punkt|Zielpunkt|  
|--------------------|-----------------------|  
|Oben links (0,0)|(200, 20)|  
|Upper-Right (100, 0)|(110, 100)|  
|Unten links (0, 50)|(250, 30)|  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild und das dem Parallelogram zugeordnete Bild. Das ursprüngliche Bild wurde verzerrt, reflektiert, gedreht und übersetzt. Die x-Achse entlang des oberen Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (110, 100). Die y-Achse entlang des linken Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (250, 30).  
  
 ![Das ursprüngliche Bild und das dem Parallelogram zugeordnete Bild.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-illustration.gif)  
  
 Die folgende Abbildung zeigt eine ähnliche Transformation, die auf ein Foto Bild angewendet wurde:  
  
 ![Das Bild eines Kletterers und des Bilds, das dem Parallelogramm zugeordnet ist.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-photo.png)  
  
 Die folgende Abbildung zeigt eine ähnliche Transformation, die auf eine Metadatei angewendet wird:  
  
 ![Abbildung von Formen und Text, die dem Parallelogram zugeordnet sind.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-metafile.png)  
  
 Im folgenden Beispiel werden die in der ersten Abbildung gezeigten Bilder erzeugt.  
  
 [!code-csharp[System.Drawing.WorkingWithImages#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.WorkingWithImages#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist. Stellen Sie sicher, `Stripes.bmp` dass Sie durch den Pfad zu einem Bild ersetzen, das auf Ihrem System gültig ist.  
  
## <a name="see-also"></a>Siehe auch

- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
