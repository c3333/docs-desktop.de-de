---
title: 'Gewusst wie: Codieren und Decodieren eines GIF-Bilds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- encoding GIF images [WPF]
- encoding image formats [WPF]
- decoding GIF images [WPF]
- decoding image formats [WPF]
- GIF decoding [WPF]
- GIF encoding [WPF]
ms.assetid: 9cdd9ec7-71eb-444b-b9e3-991958461163
ms.openlocfilehash: ec509a03d95e5f72af0b1f362e253799b07edc1f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977568"
---
# <a name="how-to-encode-and-decode-a-gif-image"></a><span data-ttu-id="6cdf7-102">Gewusst wie: Codieren und Decodieren eines GIF-Bilds</span><span class="sxs-lookup"><span data-stu-id="6cdf7-102">How to: Encode and Decode a GIF Image</span></span>
<span data-ttu-id="6cdf7-103">In den folgenden Beispielen wird veranschaulicht, wie Sie ein Graphics Interchange Format-Image (GIF) mithilfe der spezifischen <xref:System.Windows.Media.Imaging.GifBitmapDecoder> -und-Objekte decodieren und Codieren <xref:System.Windows.Media.Imaging.GifBitmapEncoder> .</span><span class="sxs-lookup"><span data-stu-id="6cdf7-103">The following examples show how to decode and encode a Graphics Interchange Format (GIF) image using the specific <xref:System.Windows.Media.Imaging.GifBitmapDecoder> and <xref:System.Windows.Media.Imaging.GifBitmapEncoder> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6cdf7-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6cdf7-104">Example</span></span>  
 <span data-ttu-id="6cdf7-105">In diesem Beispiel wird veranschaulicht, wie ein GIF-Bild mit einem aus einem decodiert wird <xref:System.Windows.Media.Imaging.GifBitmapDecoder> <xref:System.IO.FileStream> .</span><span class="sxs-lookup"><span data-stu-id="6cdf7-105">This example demonstrates how to decode a GIF image using a <xref:System.Windows.Media.Imaging.GifBitmapDecoder> from a <xref:System.IO.FileStream>.</span></span>  
  
 [!code-cpp[GifBitmapDecoderEncoder#1](~/samples/snippets/cpp/VS_Snippets_Wpf/GifBitmapDecoderEncoder/CPP/GifEncoderDecoder.cpp#1)]
 [!code-csharp[GifBitmapDecoderEncoder#1](~/samples/snippets/csharp/VS_Snippets_Wpf/GifBitmapDecoderEncoder/CSharp/GifEncoderDecoder.cs#1)]
 [!code-vb[GifBitmapDecoderEncoder#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GifBitmapDecoderEncoder/VB/GifEncoderDecoder.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="6cdf7-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6cdf7-106">Example</span></span>  
 <span data-ttu-id="6cdf7-107">In diesem Beispiel wird veranschaulicht, wie <xref:System.Windows.Media.Imaging.BitmapSource> Sie ein in ein GIF-Bild mit einem codieren <xref:System.Windows.Media.Imaging.GifBitmapEncoder> .</span><span class="sxs-lookup"><span data-stu-id="6cdf7-107">This example demonstrates how to encode a <xref:System.Windows.Media.Imaging.BitmapSource> into a GIF image using a <xref:System.Windows.Media.Imaging.GifBitmapEncoder>.</span></span>  
  
 [!code-cpp[GifBitmapDecoderEncoder#4](~/samples/snippets/cpp/VS_Snippets_Wpf/GifBitmapDecoderEncoder/CPP/GifEncoderDecoder.cpp#4)]
 [!code-csharp[GifBitmapDecoderEncoder#4](~/samples/snippets/csharp/VS_Snippets_Wpf/GifBitmapDecoderEncoder/CSharp/GifEncoderDecoder.cs#4)]
 [!code-vb[GifBitmapDecoderEncoder#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GifBitmapDecoderEncoder/VB/GifEncoderDecoder.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="6cdf7-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cdf7-108">See also</span></span>

- [<span data-ttu-id="6cdf7-109">Übersicht über die Bildverarbeitung</span><span class="sxs-lookup"><span data-stu-id="6cdf7-109">Imaging Overview</span></span>](imaging-overview.md)
