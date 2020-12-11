---
title: 'Vorgehensweise: Auflisten installierter Encoder'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image encoders [Windows Forms], listing
ms.assetid: 49e8e4e9-7a67-42d9-86bf-08821cdc282e
ms.openlocfilehash: 2634dd96b3aa5edcecde092919eb328b7f3dadc3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976155"
---
# <a name="how-to-list-installed-encoders"></a>Vorgehensweise: Auflisten installierter Encoder
Möglicherweise möchten Sie die auf einem Computer verfügbaren Bild Encoder auflisten, um zu bestimmen, ob Ihre Anwendung in einem bestimmten Bild Dateiformat gespeichert werden kann. Die- <xref:System.Drawing.Imaging.ImageCodecInfo> Klasse stellt die <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> statischen-Methoden bereit, damit Sie bestimmen können, welche Bild Encoder verfügbar sind. <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> Gibt ein Array von- <xref:System.Drawing.Imaging.ImageCodecInfo> Objekten zurück.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird die Liste der installierten Encoder und deren Eigenschaftswerte ausgegeben.  
  
 [!code-csharp[UsingImageEncodersDecoders#1](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#1)]
 [!code-vb[UsingImageEncodersDecoders#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Eine Windows Forms-Anwendung  
  
- Ein <xref:System.Windows.Forms.PaintEventArgs> , bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Auflisten installierter Decoder](how-to-list-installed-decoders.md)
- [Verwenden von Bildencodern und -decodern in Managed GDI+](using-image-encoders-and-decoders-in-managed-gdi.md)
