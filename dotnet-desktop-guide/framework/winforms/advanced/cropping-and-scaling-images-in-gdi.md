---
title: Zuschneiden und Skalieren von Bildern in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI+, scaling images
- GDI+, cropping images
- images [Windows Forms], cropping
- compressing data [Windows Forms], images
- images [Windows Forms], expansion
- images [Windows Forms], scaling
- rectangles [Windows Forms], source
- rectangles [Windows Forms], destination
- images [Windows Forms], compression
ms.assetid: ad5daf26-005f-45bc-a2af-e0e97777a21a
ms.openlocfilehash: c3cdb06e99770808461f9266fb5f07df9074149b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975039"
---
# <a name="cropping-and-scaling-images-in-gdi"></a>Zuschneiden und Skalieren von Bildern in GDI+
Sie können die <xref:System.Drawing.Graphics.DrawImage%2A> -Methode der- <xref:System.Drawing.Graphics> Klasse verwenden, um Vektorbilder und Rasterbilder zu zeichnen und zu positionieren. <xref:System.Drawing.Graphics.DrawImage%2A> ist eine überladene Methode, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen.  
  
## <a name="drawimage-variations"></a>DrawImage-Variationen  
 Eine Variation der <xref:System.Drawing.Graphics.DrawImage%2A> -Methode empfängt eine <xref:System.Drawing.Bitmap> und eine <xref:System.Drawing.Rectangle> . Das Rechteck gibt das Ziel für den Zeichnungs Vorgang an. Das heißt, es gibt das Rechteck an, in dem das Bild gezeichnet werden soll. Wenn sich die Größe des Ziel Rechtecks von der Größe des ursprünglichen Bilds unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird. Im folgenden Codebeispiel wird gezeigt, wie Sie das gleiche Bild dreimal zeichnen: einmal ohne Skalierung, einmal mit einer Erweiterung und einmal mit einer Komprimierung:  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#31)]  
  
 Die folgende Abbildung zeigt die drei Abbildungen.  
  
 ![Skalieren](./media/aboutgdip03-art06.gif "AboutGdip03_Art06")  
  
 Einige Variationen der <xref:System.Drawing.Graphics.DrawImage%2A> Methode verfügen über einen Quell Rechteck Parameter sowie einen Parameter für einen Ziel Rechtecks. Der Source-Rechteck-Parameter gibt den Teil des zu zeichnenden ursprünglichen Bilds an. Das Ziel Rechteck gibt das Rechteck an, in dem dieser Teil des Bilds gezeichnet werden soll. Wenn sich die Größe des Ziel Rechtecks von der Größe des Quell Rechtecks unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird.  
  
 Im folgenden Codebeispiel wird gezeigt, wie ein <xref:System.Drawing.Bitmap> aus dem Datei Runner.jpg erstellt wird. Das gesamte Bild wird ohne Skalierung bei (0,0) gezeichnet. Anschließend wird ein kleiner Teil des Bilds zweimal gezeichnet: einmal mit einer Komprimierung und einmal mit einer Erweiterung.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#32)]  
  
 Die folgende Abbildung zeigt das nicht skalierte Bild und die komprimierten und erweiterten Bild Teile.  
  
 ![Zuschneiden und Skalieren](./media/aboutgdip03-art07.gif "AboutGdip03_Art07")  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
