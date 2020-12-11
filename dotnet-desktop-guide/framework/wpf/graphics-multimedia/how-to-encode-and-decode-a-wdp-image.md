---
title: 'Gewusst wie: Codieren und Decodieren eines WDP-Bilds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- WDP encoding [WPF]
- WDP decoding [WPF]
- encoding image formats [WPF]
- decoding WDP images [WPF]
- decoding image formats [WPF]
- encoding WDP images [WPF]
ms.assetid: 911777d1-516b-49db-a87b-b54e31b18532
ms.openlocfilehash: 8c5c312c7e58d48a865e493c38c3defd3f5f3d1d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977605"
---
# <a name="how-to-encode-and-decode-a-wdp-image"></a>Gewusst wie: Codieren und Decodieren eines WDP-Bilds
In den folgenden Beispielen wird gezeigt, wie Sie ein Microsoft Windows Media-Foto mithilfe der spezifischen <xref:System.Windows.Media.Imaging.WmpBitmapDecoder> -und-Objekte decodieren und Codieren <xref:System.Windows.Media.Imaging.WmpBitmapEncoder> .  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird veranschaulicht, wie ein Windows Media-Fotobild mithilfe eines aus einer decodiert wird <xref:System.Windows.Media.Imaging.WmpBitmapDecoder> <xref:System.Uri> .  
  
 [!code-cpp[WdpBitmapDecoderEncoder#1](~/samples/snippets/cpp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CPP/WDPEncoderDecoder.cpp#1)]
 [!code-csharp[WdpBitmapDecoderEncoder#1](~/samples/snippets/csharp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CSharp/WDPEncoderDecoder.cs#1)]
 [!code-vb[WdpBitmapDecoderEncoder#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/VB/WDPEncoderDecoder.vb#1)]  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird veranschaulicht, wie <xref:System.Windows.Media.Imaging.BitmapSource> Sie mit einem in ein Windows Media-Foto-Bild codieren <xref:System.Windows.Media.Imaging.WmpBitmapEncoder> .  
  
 [!code-cpp[WdpBitmapDecoderEncoder#4](~/samples/snippets/cpp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CPP/WDPEncoderDecoder.cpp#4)]
 [!code-csharp[WdpBitmapDecoderEncoder#4](~/samples/snippets/csharp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CSharp/WDPEncoderDecoder.cs#4)]
 [!code-vb[WdpBitmapDecoderEncoder#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/VB/WDPEncoderDecoder.vb#4)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Bildverarbeitung](imaging-overview.md)
