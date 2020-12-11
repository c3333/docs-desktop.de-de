---
title: 'Vorgehensweise: Laden und Anzeigen von Metadateien'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- examples [Windows Forms], metafiles
- metafiles [Windows Forms], displaying
ms.assetid: 60af1714-f148-4d85-a739-0557965ffa73
ms.openlocfilehash: 6c17e0b2d023ccf80b0d32301b7ee6765edcae9f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975902"
---
# <a name="how-to-load-and-display-metafiles"></a>Vorgehensweise: Laden und Anzeigen von Metadateien
Die- <xref:System.Drawing.Imaging.Metafile> Klasse, die von der- <xref:System.Drawing.Image> Klasse erbt, stellt Methoden zum Aufzeichnen, anzeigen und untersuchen von Vektorbildern bereit.  
  
## <a name="example"></a>Beispiel  
 Zum Anzeigen eines Vektor Bilds (Metadatei) auf dem Bildschirm benötigen Sie ein <xref:System.Drawing.Imaging.Metafile> -Objekt und ein- <xref:System.Drawing.Graphics> Objekt. Übergeben Sie den Namen einer Datei (oder eines Datenstroms) an einen <xref:System.Drawing.Imaging.Metafile> Konstruktor. Nachdem Sie ein-Objekt erstellt haben <xref:System.Drawing.Imaging.Metafile> , übergeben Sie dieses <xref:System.Drawing.Imaging.Metafile> Objekt an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts.  
  
 Im Beispiel wird ein <xref:System.Drawing.Imaging.Metafile> -Objekt aus einer EMF-Datei (Enhanced Metafile) erstellt, und anschließend wird das Bild mit der linken oberen Ecke bei (60, 10) gezeichnet.  
  
 In der folgenden Abbildung ist die an der angegebenen Position gezeichnete Metadatendatei dargestellt.  
  
 ![Screenshot der Bildposition](./media/how-to-load-and-display-metafiles/metafile-drawn-specified-location.png "imageposition2")  
  
 [!code-csharp[System.Drawing.WorkingWithImages#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.WorkingWithImages#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
