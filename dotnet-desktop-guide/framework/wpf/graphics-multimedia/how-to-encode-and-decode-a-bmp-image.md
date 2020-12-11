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
# <a name="how-to-encode-and-decode-a-bmp-image"></a><span data-ttu-id="acd35-102">Gewusst wie: Codieren und Decodieren eines BMP-Bilds</span><span class="sxs-lookup"><span data-stu-id="acd35-102">How to: Encode and Decode a BMP Image</span></span>
<span data-ttu-id="acd35-103">In den folgenden Beispielen wird gezeigt, wie Sie ein Bitmap-Bild (BMP) mithilfe der spezifischen <xref:System.Windows.Media.Imaging.BmpBitmapDecoder> -und-Objekte decodieren und Codieren <xref:System.Windows.Media.Imaging.BmpBitmapEncoder> .</span><span class="sxs-lookup"><span data-stu-id="acd35-103">The following examples show how to decode and encode a bitmap (BMP) image using the specific <xref:System.Windows.Media.Imaging.BmpBitmapDecoder> and <xref:System.Windows.Media.Imaging.BmpBitmapEncoder> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="acd35-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="acd35-104">Example</span></span>  
 <span data-ttu-id="acd35-105">In diesem Beispiel wird veranschaulicht, wie ein BMP-Bild mit einem aus einem decodiert wird <xref:System.Windows.Media.Imaging.BmpBitmapDecoder> <xref:System.Uri> .</span><span class="sxs-lookup"><span data-stu-id="acd35-105">This example demonstrates how to decode a BMP image using a <xref:System.Windows.Media.Imaging.BmpBitmapDecoder> from a <xref:System.Uri>.</span></span>  
  
 [!code-cpp[BmpBitmapDecoderEncoder#5](~/samples/snippets/cpp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CPP/anotherfile.cpp#5)]
 [!code-csharp[BmpBitmapDecoderEncoder#5](~/samples/snippets/csharp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CSharp/BitmapFrame.cs#5)]
 [!code-vb[BmpBitmapDecoderEncoder#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/VB/BitmapFrame.vb#5)]  
  
## <a name="example"></a><span data-ttu-id="acd35-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="acd35-106">Example</span></span>  
 <span data-ttu-id="acd35-107">In diesem Beispiel wird veranschaulicht, wie ein <xref:System.Windows.Media.Imaging.BitmapSource> mithilfe eines in ein BMP-Bild codiert wird <xref:System.Windows.Media.Imaging.BmpBitmapEncoder> .</span><span class="sxs-lookup"><span data-stu-id="acd35-107">This example demonstrates how to encode a <xref:System.Windows.Media.Imaging.BitmapSource> into a BMP image using a <xref:System.Windows.Media.Imaging.BmpBitmapEncoder>.</span></span>  
  
 [!code-cpp[BmpBitmapDecoderEncoder#4](~/samples/snippets/cpp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CPP/anotherfile.cpp#4)]
 [!code-csharp[BmpBitmapDecoderEncoder#4](~/samples/snippets/csharp/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/CSharp/BitmapFrame.cs#4)]
 [!code-vb[BmpBitmapDecoderEncoder#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BmpBitmapDecoderEncoder/VB/BitmapFrame.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="acd35-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acd35-108">See also</span></span>

- [<span data-ttu-id="acd35-109">Übersicht über die Bildverarbeitung</span><span class="sxs-lookup"><span data-stu-id="acd35-109">Imaging Overview</span></span>](imaging-overview.md)
