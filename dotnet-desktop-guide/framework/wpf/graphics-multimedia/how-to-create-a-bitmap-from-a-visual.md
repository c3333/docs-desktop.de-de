---
title: 'Gewusst wie: Erstellen einer Bitmap mit einem visuellen Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [WPF], rendering from visuals
- visuals [WPF], rendering to bitmaps
ms.assetid: 103fc7f5-7306-4026-9d61-2005e79959f3
ms.openlocfilehash: a622d99f7c477f8654526ed399f1eb37288682fe
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977619"
---
# <a name="how-to-create-a-bitmap-from-a-visual"></a><span data-ttu-id="0f73e-102">Gewusst wie: Erstellen einer Bitmap mit einem visuellen Element</span><span class="sxs-lookup"><span data-stu-id="0f73e-102">How to: Create a Bitmap from a Visual</span></span>
<span data-ttu-id="0f73e-103">Dieses Beispiel zeigt, wie Sie eine Bitmap aus einem erstellen können <xref:System.Windows.Media.Visual> .</span><span class="sxs-lookup"><span data-stu-id="0f73e-103">This example shows how you can create a bitmap from a <xref:System.Windows.Media.Visual>.</span></span> <span data-ttu-id="0f73e-104">Eine <xref:System.Windows.Media.DrawingVisual> wird mit gerendert <xref:System.Windows.Media.FormattedText> .</span><span class="sxs-lookup"><span data-stu-id="0f73e-104">A <xref:System.Windows.Media.DrawingVisual> is rendered with <xref:System.Windows.Media.FormattedText>.</span></span> <span data-ttu-id="0f73e-105">Das <xref:System.Windows.Media.Visual> wird dann in der gerendert, das <xref:System.Windows.Media.Imaging.RenderTargetBitmap> eine Bitmap des angegebenen Texts erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f73e-105">The <xref:System.Windows.Media.Visual> is then rendered to the <xref:System.Windows.Media.Imaging.RenderTargetBitmap> creating a bitmap of the given text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0f73e-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0f73e-106">Example</span></span>  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample.cs#creatertbimage)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample.vb#creatertbimage)]  
  
## <a name="see-also"></a><span data-ttu-id="0f73e-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f73e-107">See also</span></span>

- <xref:System.Windows.Media.DrawingContext>
- [<span data-ttu-id="0f73e-108">Übersicht über die Bildverarbeitung</span><span class="sxs-lookup"><span data-stu-id="0f73e-108">Imaging Overview</span></span>](imaging-overview.md)
- [<span data-ttu-id="0f73e-109">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="0f73e-109">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="0f73e-110">Verwenden von DrawingVisual-Objekten</span><span class="sxs-lookup"><span data-stu-id="0f73e-110">Using DrawingVisual Objects</span></span>](using-drawingvisual-objects.md)
