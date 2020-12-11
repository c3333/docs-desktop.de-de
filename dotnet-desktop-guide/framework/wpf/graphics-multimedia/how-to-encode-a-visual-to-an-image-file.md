---
title: 'Gewusst wie: Codieren eines Visual-Objekts in einer Bilddatei'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image files [WPF], encoding from visuals
- encoding image formats [WPF]
- visuals [WPF], encoding to an image file
ms.assetid: 2036385b-ea47-4d54-8027-5797f52c8149
ms.openlocfilehash: 193b6a14e404d32bb49d6e0ef3cbd513166bcce2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978194"
---
# <a name="how-to-encode-a-visual-to-an-image-file"></a><span data-ttu-id="8dcf0-102">Gewusst wie: Codieren eines Visual-Objekts in einer Bilddatei</span><span class="sxs-lookup"><span data-stu-id="8dcf0-102">How to: Encode a Visual to an Image File</span></span>
<span data-ttu-id="8dcf0-103">In diesem Beispiel wird veranschaulicht, wie ein <xref:System.Windows.Media.Visual> -Objekt mithilfe von und in in eine Bilddatei codiert wird <xref:System.Windows.Media.Imaging.RenderTargetBitmap> <xref:System.Windows.Media.Imaging.PngBitmapEncoder> .</span><span class="sxs-lookup"><span data-stu-id="8dcf0-103">This example demonstrates how to encode a <xref:System.Windows.Media.Visual> object into an image file using a <xref:System.Windows.Media.Imaging.RenderTargetBitmap> and a <xref:System.Windows.Media.Imaging.PngBitmapEncoder>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8dcf0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8dcf0-104">Example</span></span>  
 <span data-ttu-id="8dcf0-105">Die <xref:System.Windows.Media.DrawingVisual> wird mit einem erstellt <xref:System.Windows.Media.Imaging.BitmapImage> <xref:System.Windows.Media.FormattedText> , das in einem gerendert wird <xref:System.Windows.Media.Imaging.RenderTargetBitmap> .</span><span class="sxs-lookup"><span data-stu-id="8dcf0-105">The <xref:System.Windows.Media.DrawingVisual> is created using a <xref:System.Windows.Media.Imaging.BitmapImage> and <xref:System.Windows.Media.FormattedText> which is rendered to a <xref:System.Windows.Media.Imaging.RenderTargetBitmap>.</span></span> <span data-ttu-id="8dcf0-106">Die gerenderte Bitmap wird dann verwendet, um einen zu erstellen, der <xref:System.Windows.Media.Imaging.BitmapFrame> dem hinzugefügt wird <xref:System.Windows.Media.Imaging.PngBitmapEncoder> , um eine neue Portable Network Graphics (PNG)-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-106">The rendered bitmap is then used to create a <xref:System.Windows.Media.Imaging.BitmapFrame> which is added to the <xref:System.Windows.Media.Imaging.PngBitmapEncoder> to create a new Portable Network Graphics (PNG) file.</span></span>  
  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample_Encode.cs#rtbencodeinline1)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample_Encode.vb#rtbencodeinline1)]  
  
 <span data-ttu-id="8dcf0-107"><xref:System.Windows.Media.Imaging.PngBitmapEncoder>In diesem Beispiel wurde ein verwendet, aber eines der abgeleiteten <xref:System.Windows.Media.Imaging.BitmapEncoder> Objekte hätte zum Erstellen der Bilddatei verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-107">A <xref:System.Windows.Media.Imaging.PngBitmapEncoder> was used in this example but any of the derived <xref:System.Windows.Media.Imaging.BitmapEncoder> objects could have been used to create the image file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8dcf0-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dcf0-108">See also</span></span>

- <xref:System.Windows.Media.DrawingContext>
- [<span data-ttu-id="8dcf0-109">Übersicht über die Bildverarbeitung</span><span class="sxs-lookup"><span data-stu-id="8dcf0-109">Imaging Overview</span></span>](imaging-overview.md)
- [<span data-ttu-id="8dcf0-110">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="8dcf0-110">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="8dcf0-111">Verwenden von DrawingVisual-Objekten</span><span class="sxs-lookup"><span data-stu-id="8dcf0-111">Using DrawingVisual Objects</span></span>](using-drawingvisual-objects.md)
