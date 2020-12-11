---
title: 'Vorgehensweise: Auflisten installierter Decoder'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image decoders [Windows Forms], listing
ms.assetid: 11417191-8c95-40ca-8024-779e61706fb6
ms.openlocfilehash: 961862d6212b7e76812fc222d3a99f08528d9a16
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975904"
---
# <a name="how-to-list-installed-decoders"></a>Vorgehensweise: Auflisten installierter Decoder
Möglicherweise möchten Sie die auf einem Computer verfügbaren Abbild-Decoder auflisten, um zu bestimmen, ob Ihre Anwendung ein bestimmtes Bild Dateiformat lesen kann. Die- <xref:System.Drawing.Imaging.ImageCodecInfo> Klasse stellt die <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> statischen-Methoden bereit, damit Sie bestimmen können, welche Bilddecoder verfügbar sind. <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> Gibt ein Array von- <xref:System.Drawing.Imaging.ImageCodecInfo> Objekten zurück.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird die Liste der installierten Decoder und deren Eigenschaftswerte ausgegeben.  
  
 [!code-csharp[UsingImageEncodersDecoders#2](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#2)]
 [!code-vb[UsingImageEncodersDecoders#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#2)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Eine Windows Forms-Anwendung  
  
- Ein <xref:System.Windows.Forms.PaintEventArgs> , bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Auflisten installierter Encoder](how-to-list-installed-encoders.md)
- [Verwenden von Bildencodern und -decodern in Managed GDI+](using-image-encoders-and-decoders-in-managed-gdi.md)
