---
title: Zeichnen, Positionieren und Klonen von Bildern in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- raster images [Windows Forms]
- images [Windows Forms], positioning
- drawing [Windows Forms], images
- drawing [Windows Forms], raster images
- images [Windows Forms], cloning
- images [Windows Forms], drawing
- GDI+, drawing images
- GDI+, cloning images
- GDI+, positioning images
ms.assetid: 09f0c07a-19c0-43b4-90a2-862a10545ce8
ms.openlocfilehash: b5f98e7bdef9ff8ed0a4cd0e040cb92a31f30503
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975290"
---
# <a name="drawing-positioning-and-cloning-images-in-gdi"></a>Zeichnen, Positionieren und Klonen von Bildern in GDI+
Sie können die <xref:System.Drawing.Bitmap> -Klasse verwenden, um Rasterbilder zu laden und anzuzeigen, und Sie können die <xref:System.Drawing.Imaging.Metafile> -Klasse verwenden, um Vektorbilder zu laden und anzuzeigen. Die <xref:System.Drawing.Bitmap> -und- <xref:System.Drawing.Imaging.Metafile> Klassen erben von der- <xref:System.Drawing.Image> Klasse. Zum Anzeigen eines Vektor Bilds benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse und eine-Klasse <xref:System.Drawing.Imaging.Metafile> . Zum Anzeigen eines Raster Bilds benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse und eine-Klasse <xref:System.Drawing.Bitmap> . Die Instanz der- <xref:System.Drawing.Graphics> Klasse stellt die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode bereit, die die-oder-Methode <xref:System.Drawing.Imaging.Metafile> <xref:System.Drawing.Bitmap> als Argument empfängt.  
  
## <a name="file-types-and-cloning"></a>Dateitypen und Klonen  
 Im folgenden Codebeispiel wird gezeigt, wie ein <xref:System.Drawing.Bitmap> aus dem Datei Climber.jpg erstellt und die Bitmap angezeigt wird. Der Zielpunkt für die obere linke Ecke des Bilds (10, 10) wird in den zweiten und dritten Parametern angegeben.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#11)]  
  
 In der folgenden Abbildung ist das Bild dargestellt.  
  
 ![Bildbeispiel](./media/aboutgdip03-art04.gif "AboutGdip03_Art04")  
  
 Sie können <xref:System.Drawing.Bitmap> Objekte aus einer Vielzahl von Grafikdatei Formaten erstellen: BMP, GIF, JPEG, EXIF, PNG, TIFF und Symbol.  
  
 Im folgenden Codebeispiel wird gezeigt, wie Sie <xref:System.Drawing.Bitmap> -Objekte aus einer Vielzahl von Dateitypen erstellen und dann die Bitmaps anzeigen.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#12)]  
  
 Die- <xref:System.Drawing.Bitmap> Klasse stellt eine-Methode bereit, mit der <xref:System.Drawing.Bitmap.Clone%2A> Sie eine Kopie einer vorhandenen erstellen können <xref:System.Drawing.Bitmap> . Die- <xref:System.Drawing.Bitmap.Clone%2A> Methode verfügt über einen Parameter des Quell Rechtecks, mit dem Sie den Teil der ursprünglichen Bitmap angeben können, den Sie kopieren möchten. Im folgenden Codebeispiel wird gezeigt, wie ein erstellt <xref:System.Drawing.Bitmap> wird, indem die obere Hälfte eines vorhandenen geklont wird <xref:System.Drawing.Bitmap> . Anschließend werden beide Bilder gezeichnet.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#13)]  
  
 Die folgende Abbildung zeigt die beiden Bilder.  
  
 ![Zuschneiden](./media/aboutgdip03-art05.gif "AboutGdip03_Art05")  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md)
- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
