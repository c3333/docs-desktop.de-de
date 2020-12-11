---
title: 'Vorgehensweise: Zuschneiden und Skalieren von Bildern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], cropping
- images [Windows Forms], scaling
ms.assetid: 053e3360-bca0-4b25-9afa-0e77a6f17b03
ms.openlocfilehash: 4257431881565f9160f45795111d374cc680dedd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972361"
---
# <a name="how-to-crop-and-scale-images"></a>Vorgehensweise: Zuschneiden und Skalieren von Bildern
Die <xref:System.Drawing.Graphics> -Klasse stellt mehrere <xref:System.Drawing.Graphics.DrawImage%2A> Methoden bereit, von denen einige über Quell-und Ziel Rechteck Parameter verfügen, die Sie zum Zuschneiden und Skalieren von Bildern verwenden können.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datenträger Datei Apple.gif erstellt. Der Code zeichnet das gesamte Apple-Image in seiner ursprünglichen Größe. Der Code ruft dann die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts auf, um einen Teil des Apple-Bilds in einem Ziel Rechteck zu zeichnen, das größer ist als das ursprüngliche Apple-Image.  
  
 Die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode bestimmt, welcher Teil des Apple gezeichnet werden soll, indem das Quell Rechteck betrachtet wird, das durch das dritte, vierte, fünfte und sechste Argument angegeben wird. In diesem Fall wird Apple auf 75 Prozent seiner Breite und 75 Prozent seiner Höhe zugeschnitten.  
  
 <xref:System.Drawing.Graphics.DrawImage%2A>Mit der-Methode wird bestimmt, wo das gekippte Apple gezeichnet werden soll und wie groß das angeschnittenen Apple ist, indem das Ziel Rechteck, das durch das zweite Argument angegeben wird, durchsucht wird. In diesem Fall ist das Ziel Rechteck um 30 Prozent breiter und 30 Prozent höher als das ursprüngliche Bild.  
  
 Die folgende Abbildung zeigt das ursprüngliche Apple und das skalierte, ausgeschnittene Apple.  
  
 ![Screenshot eines ursprünglichen Bilds und des abgeschnittenen Bilds.](./media/how-to-crop-and-scale-images/original-image-cropped-image.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.WorkingWithImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist. Stellen Sie sicher, `Apple.gif` dass Sie durch einen Bilddateinamen und-Pfad ersetzen, die auf Ihrem System gültig sind.  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
