---
title: 'Vorgehensweise: Zeichnen einer vorhandenen Bitmap auf dem Bildschirm'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [Windows Forms], displaying in Windows Forms
- bitmaps [Windows Forms], loading in Windows Forms applications
- images [Windows Forms], displaying on Windows Forms
ms.assetid: 5bc558d7-b326-4050-a834-b8600da0de95
ms.openlocfilehash: 90511adf9caffe7952e270d6fe32dd85162a29d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975936"
---
# <a name="how-to-draw-an-existing-bitmap-to-the-screen"></a>Vorgehensweise: Zeichnen einer vorhandenen Bitmap auf dem Bildschirm
Sie können ein vorhandenes Bild problemlos auf dem Bildschirm zeichnen. Zunächst müssen Sie ein- <xref:System.Drawing.Bitmap> Objekt erstellen, indem Sie den Bitmap-Konstruktor verwenden, der einen Dateinamen annimmt <xref:System.Drawing.Bitmap.%23ctor%28System.String%29> . Dieser Konstruktor akzeptiert Bilder mit verschiedenen Dateiformaten, einschließlich BMP, GIF, JPEG, PNG und TIFF. Nachdem Sie das-Objekt erstellt haben <xref:System.Drawing.Bitmap> , übergeben Sie dieses <xref:System.Drawing.Bitmap> Objekt an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts.  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel <xref:System.Drawing.Bitmap> wird ein-Objekt aus einer JPEG-Datei erstellt, und anschließend wird die Bitmap mit der linken oberen Ecke bei (60, 10) gezeichnet.  
  
 In der folgenden Abbildung wird die Bitmap gezeigt, die an der angegebenen Position gezeichnet wurde:  
  
 ![Screenshot, der ein Bild an einer bestimmten Position anzeigt.](./media/how-to-draw-an-existing-bitmap-to-the-screen/bitmap-specified-position.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.WorkingWithImages#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
