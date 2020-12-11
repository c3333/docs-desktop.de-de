---
title: 'Vorgehensweise: Verwenden eines zwischengespeicherten Elements als Pinsel'
ms.date: 03/30/2017
helpviewer_keywords:
- BitmapCache [WPF], using
- cached element [WPF], use as a brush
- BitmapCacheBrush [WPF], using
- CacheMode [WPF], using
ms.assetid: d36e944a-866e-4baf-98c4-fd6a75f6fdd0
ms.openlocfilehash: 78df242c7f00b69e36ea4ab6751f51509d9e2220
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977868"
---
# <a name="how-to-use-a-cached-element-as-a-brush"></a><span data-ttu-id="b0a2a-102">Vorgehensweise: Verwenden eines zwischengespeicherten Elements als Pinsel</span><span class="sxs-lookup"><span data-stu-id="b0a2a-102">How to: Use a Cached Element as a Brush</span></span>
<span data-ttu-id="b0a2a-103">Verwenden Sie die- <xref:System.Windows.Media.BitmapCacheBrush> Klasse zur effizienten Wiederverwendung eines zwischengespeicherten Elements.</span><span class="sxs-lookup"><span data-stu-id="b0a2a-103">Use the <xref:System.Windows.Media.BitmapCacheBrush> class to reuse a cached element efficiently.</span></span> <span data-ttu-id="b0a2a-104">Um ein Element zwischenzuspeichern, erstellen Sie eine neue Instanz der <xref:System.Windows.Media.BitmapCache> -Klasse und weisen Sie der-Eigenschaft des-Elements zu <xref:System.Windows.UIElement.CacheMode%2A> .</span><span class="sxs-lookup"><span data-stu-id="b0a2a-104">To cache an element, create a new instance of the <xref:System.Windows.Media.BitmapCache> class and assign it to the element's <xref:System.Windows.UIElement.CacheMode%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b0a2a-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0a2a-105">Example</span></span>  
 <span data-ttu-id="b0a2a-106">Im folgenden Codebeispiel wird gezeigt, wie ein zwischengespeichertes Element wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0a2a-106">The following code example shows how to reuse a cached element.</span></span> <span data-ttu-id="b0a2a-107">Das zwischengespeicherte Element ist ein <xref:System.Windows.Controls.Image> Steuerelement, das ein großes Bild anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b0a2a-107">The cached element is an <xref:System.Windows.Controls.Image> control that displays a large image.</span></span> <span data-ttu-id="b0a2a-108">Das- <xref:System.Windows.Controls.Image> Steuerelement wird mithilfe der-Klasse als Bitmap zwischengespeichert <xref:System.Windows.Media.BitmapCache> , und der Cache wird wieder verwendet, indem es einem zugewiesen wird <xref:System.Windows.Media.BitmapCacheBrush> .</span><span class="sxs-lookup"><span data-stu-id="b0a2a-108">The <xref:System.Windows.Controls.Image> control is cached as a bitmap by using the <xref:System.Windows.Media.BitmapCache> class, and the cache is reused by assigning it to a <xref:System.Windows.Media.BitmapCacheBrush>.</span></span> <span data-ttu-id="b0a2a-109">Der Pinsel wird dem Hintergrund von 20-fünf-Schaltflächen zugewiesen, um eine effiziente Wiederverwendung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b0a2a-109">The brush is assigned to the background of twenty-five buttons to show efficient reuse.</span></span>  
  
 [!code-xaml[System.Windows.Media.BitmapCacheBrush#_BitmapCacheBrushXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcachebrush/cs/window1.xaml#_bitmapcachebrushxaml)]  
  
## <a name="see-also"></a><span data-ttu-id="b0a2a-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a2a-110">See also</span></span>

- <xref:System.Windows.Media.BitmapCache>
- <xref:System.Windows.Media.BitmapCacheBrush>
- <xref:System.Windows.UIElement.CacheMode%2A>
- [<span data-ttu-id="b0a2a-111">Vorgehensweise: Verbessern der Renderingleistung durch Zwischenspeichern eines Elements</span><span class="sxs-lookup"><span data-stu-id="b0a2a-111">How to: Improve Rendering Performance by Caching an Element</span></span>](how-to-improve-rendering-performance-by-caching-an-element.md)
