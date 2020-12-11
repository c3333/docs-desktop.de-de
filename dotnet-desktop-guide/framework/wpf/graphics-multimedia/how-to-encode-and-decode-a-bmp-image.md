---
title: 'Gewusst wie: Codieren und Decodieren eines BMP-Bilds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- encoding BMP images [WPF]
- BMP encoding [WPF]
- decoding BMP images [WPF]
- encoding image formats [WPF]
- BMP decoding [WPF]
- decoding image formats [WPF]
ms.assetid: feb5ef27-28ac-40ab-bfc2-e0456990d32c
ms.openlocfilehash: 7d3520a1b1913fe68fedb0ea9d76cc138ed661c4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977406"
---
# <a name="how-to-encode-and-decode-a-bmp-image"></a>Gewusst wie: Codieren und Decodieren eines BMP-Bilds
In den folgenden Beispielen wird gezeigt, wie Sie ein Bitmap-Bild (BMP) mithilfe der spezifischen <xref:System.Windows.Media.Imaging.BmpBitmapDecoder> -und-Objekte decodieren und Codieren <xref:System.Windows.Media.Imaging.BmpBitmapEncoder> .  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird veranschaulicht, wie ein BMP-Bild mit einem aus einem decodiert wird <xref:System.Windows.Media.Imaging.BmpBitmapDecoder> <xref:System.Uri> .  
  
 [!code-cpp[BmpBitmapDecoderEncoder#5](~/samples/snippets/cpp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CPP/anotherfile.cpp#5)]
 [!code-csharp[BmpBitmapDecoderEncoder#5](~/samples/snippets/csharp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CSharp/BitmapFrame.cs#5)]
 [!code-vb[BmpBitmapDecoderEncoder#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/VB/BitmapFrame.vb#5)]  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird veranschaulicht, wie ein <xref:System.Windows.Media.Imaging.BitmapSource> mithilfe eines in ein BMP-Bild codiert wird <xref:System.Windows.Media.Imaging.BmpBitmapEncoder> .  
  
 [!code-cpp[BmpBitmapDecoderEncoder#4](~/samples/snippets/cpp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CPP/anotherfile.cpp#4)]
 [!code-csharp[BmpBitmapDecoderEncoder#4](~/samples/snippets/csharp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CSharp/BitmapFrame.cs#4)]
 [!code-vb[BmpBitmapDecoderEncoder#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/VB/BitmapFrame.vb#4)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Bildverarbeitung](imaging-overview.md)
