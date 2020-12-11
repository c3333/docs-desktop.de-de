---
title: 'Vorgehensweise: Verwenden des Interpolationsmodus zum Steuern der Bildqualität während der Skalierung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- interpolation mode [Windows Forms], controlling image quality
- images [Windows Forms], scaling
- images [Windows Forms], controlling quality
ms.assetid: fde9bccf-8aa5-4b0d-ba4b-788740627b02
ms.openlocfilehash: ab0ff93b3ee26467c0de448efd31b698167f95c2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976101"
---
# <a name="how-to-use-interpolation-mode-to-control-image-quality-during-scaling"></a>Vorgehensweise: Verwenden des Interpolationsmodus zum Steuern der Bildqualität während der Skalierung
Der Interpolations Modus eines- <xref:System.Drawing.Graphics> Objekts wirkt sich auf die Art der Skalierung (Streckung und Verkleinerung) von GDI+ aus. Die- <xref:System.Drawing.Drawing2D.InterpolationMode> Enumeration definiert mehrere Interpolations Modi, von denen einige in der folgenden Liste aufgeführt sind:  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.NearestNeighbor>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.Bilinear>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.HighQualityBilinear>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.Bicubic>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.HighQualityBicubic>  
  
 Zum Strecken eines Bilds muss jedes Pixel im ursprünglichen Bild einer Gruppe von Pixeln im größeren Bild zugeordnet werden. Zum Verkleinern eines Bilds müssen Gruppen von Pixeln im ursprünglichen Bild einem einzelnen Pixel im kleineren Bild zugeordnet werden. Die Effektivität der Algorithmen, die diese Zuordnungen durchführen, bestimmt die Qualität eines skalierten Bilds. Algorithmen, die skalierbare Images höherer Qualität liefern, erfordern tendenziell mehr Verarbeitungszeit. In der vorangehenden Liste <xref:System.Drawing.Drawing2D.InterpolationMode.NearestNeighbor> ist der Modus der niedrigsten Qualität und <xref:System.Drawing.Drawing2D.InterpolationMode.HighQualityBicubic> der Modus mit der höchsten Qualität.  
  
 Um den Interpolations Modus festzulegen, weisen Sie einen der Member der- <xref:System.Drawing.Drawing2D.InterpolationMode> Enumeration der- <xref:System.Drawing.Graphics.InterpolationMode%2A> Eigenschaft eines-Objekts zu <xref:System.Drawing.Graphics> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Bild gezeichnet und dann mit drei verschiedenen Interpolations Modi verkleinert.  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild und die drei kleineren Bilder.  
  
 ![Screenshot, der ein Bild mit unterschiedlichen Interpolations Einstellungen anzeigt.](./media/how-to-use-interpolation-mode-to-control-image-quality-during-scaling/varied-interpolation-settings.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#81](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#81)]
 [!code-vb[System.Drawing.WorkingWithImages#81](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#81)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
