---
title: 'Vorgehensweise: Erstellen von Miniaturbildern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- thumbnail images [Windows Forms], creating
- images [Windows Forms], creating thumbnails
ms.assetid: e956242a-1e5b-4217-a3cf-5f3fb45d00ba
ms.openlocfilehash: 786a92d99f5e7a0c27f502efa9a5fe617ac4d4d6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972367"
---
# <a name="how-to-create-thumbnail-images"></a>Vorgehensweise: Erstellen von Miniaturbildern
Bei einem Miniaturbild handelt es sich um eine kleine Version eines Bilds. Sie können ein Miniaturbild erstellen, indem Sie die- <xref:System.Drawing.Image.GetThumbnailImage%2A> Methode eines- <xref:System.Drawing.Image> Objekts aufrufen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus einer JPG-Datei erstellt. Das ursprüngliche Bild hat eine Breite von 640 Pixeln und eine Höhe von 479 Pixel. Der Code erstellt ein Miniaturbild mit einer Breite von 100 Pixeln und einer Höhe von 100 Pixeln.  
  
 Die folgende Abbildung zeigt das Miniaturbild:  
  
 ![Screenshot, der die Miniaturansicht der Ausgabe anzeigt.](./media/how-to-create-thumbnail-images/construct-thumbnail-image.png)  
  
> [!NOTE]
> In diesem Beispiel wird eine Rückruf Methode deklariert, aber nie verwendet. Dies unterstützt alle Versionen von GDI+.  
  
 [!code-csharp[System.Drawing.WorkingWithImages#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.WorkingWithImages#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist. Um das Beispiel auszuführen, führen Sie die folgenden Schritte aus:  
  
1. Erstellen Sie eine neue Windows Forms-Anwendung.  
  
2. Fügen Sie dem Formular den Beispielcode hinzu.  
  
3. Erstellen eines Handlers für das Ereignis des Formulars <xref:System.Windows.Forms.Control.Paint>  
  
4. Nennen Sie im <xref:System.Windows.Forms.Control.Paint> -Handler die `GetThumbnail` -Methode, und übergeben Sie `e` für <xref:System.Windows.Forms.PaintEventArgs> .  
  
5. Suchen Sie nach einer Bilddatei, für die Sie eine Miniaturansicht erstellen möchten.  
  
6. Geben Sie in der- `GetThumbnail` Methode den Pfad und den Dateinamen für das Image an.  
  
7. Drücken Sie F5, um das Beispiel auszuführen.  
  
     Im Formular wird ein Miniaturbild von 100 nach 100 angezeigt.  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
