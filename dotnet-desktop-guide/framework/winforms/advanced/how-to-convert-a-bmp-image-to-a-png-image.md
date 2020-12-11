---
title: 'Vorgehensweise: Konvertieren eines BMP-Bilds in ein PNG-Bild'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- BMP images [Windows Forms], converting to PNG
- image formats [Windows Forms], converting between
ms.assetid: 9d4a692d-73ac-4ce3-9e05-9ec321e8fbd6
ms.openlocfilehash: 59200941aa0f872a0bd99510bfaa8a8b878a9061
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975011"
---
# <a name="how-to-convert-a-bmp-image-to-a-png-image"></a>Vorgehensweise: Konvertieren eines BMP-Bilds in ein PNG-Bild
Sie möchten sicher oft eine Datei von einem Bilddateiformat in ein anderes konvertieren. Sie können diese Konvertierung einfach durchführen, indem Sie die <xref:System.Drawing.Image.Save%2A>-Methode der <xref:System.Drawing.Image>-Klasse aufrufen und das <xref:System.Drawing.Imaging.ImageFormat> für das gewünschte Bilddateiformat angeben.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein BMP-Bild eines Typs geladen und im PNG-Format gespeichert.  
  
 [!code-csharp[UsingImageEncodersDecoders#4](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#4)]
 [!code-vb[UsingImageEncodersDecoders#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Eine Windows Forms-Anwendung  
  
- Einen Verweis auf den `System.Drawing.Imaging`-Namespace  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Auflisten installierter Encoder](how-to-list-installed-encoders.md)
- [Verwenden von Bildencodern und -decodern in Managed GDI+](using-image-encoders-and-decoders-in-managed-gdi.md)
- [Bitmaptypen](types-of-bitmaps.md)
