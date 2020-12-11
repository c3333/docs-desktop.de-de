---
title: 'Vorgehensweise: Ermitteln der von einem Encoder unterstützten Parameter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- encoder parameters [Windows Forms], determining supported
ms.assetid: f47ae459-e3ce-4d41-a140-2f6c6aea3f44
ms.openlocfilehash: 3e5345180e0ff3321b9ef0b885b836d3e9456f28
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972359"
---
# <a name="how-to-determine-the-parameters-supported-by-an-encoder"></a>Vorgehensweise: Ermitteln der von einem Encoder unterstützten Parameter
Sie können Bildparameter anpassen, z. b. Qualität und Komprimierungs Ebene, aber Sie müssen wissen, welche Parameter von einem bestimmten Bild Encoder unterstützt werden. Die- <xref:System.Drawing.Image> Klasse stellt die- <xref:System.Drawing.Image.GetEncoderParameterList%2A> Methode bereit, sodass Sie bestimmen können, welche Bildparameter für einen bestimmten Encoder unterstützt werden. Sie geben den Encoder mit einer GUID an. Die- <xref:System.Drawing.Image.GetEncoderParameterList%2A> Methode gibt ein Array von- <xref:System.Drawing.Imaging.EncoderParameter> Objekten zurück.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispielcode werden die unterstützten Parameter für den JPEG-Encoder ausgegeben. Verwenden Sie die Liste der Parameter Kategorien und zugeordneten GUIDs in der <xref:System.Drawing.Imaging.Encoder> Klassen Übersicht, um die Kategorie für jeden Parameter zu bestimmen.  
  
 [!code-csharp[UsingImageEncodersDecoders#3](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#3)]
 [!code-vb[UsingImageEncodersDecoders#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#3)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Eine Windows Forms-Anwendung  
  
- Ein <xref:System.Windows.Forms.PaintEventArgs> , bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Auflisten installierter Encoder](how-to-list-installed-encoders.md)
- [Bitmaptypen](types-of-bitmaps.md)
- [Verwenden von Bildencodern und -decodern in Managed GDI+](using-image-encoders-and-decoders-in-managed-gdi.md)
