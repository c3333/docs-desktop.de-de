---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einem Video'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- painting with a video [WPF]
- video [WPF], painting with
- brushes [WPF], painting with a video
ms.assetid: 04dd6600-4a6e-4b43-a93e-21cce7dfbcb8
ms.openlocfilehash: be09d1310847cd7214ea795a704c25d994f07b7a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977853"
---
# <a name="how-to-paint-an-area-with-a-video"></a><span data-ttu-id="d832a-102">Gewusst wie: Zeichnen eines Bereichs mit einem Video</span><span class="sxs-lookup"><span data-stu-id="d832a-102">How to: Paint an Area with a Video</span></span>
<span data-ttu-id="d832a-103">Dieses Beispiel zeigt, wie Sie einen Bereich mit Medien zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d832a-103">This example shows how to paint an area with media.</span></span> <span data-ttu-id="d832a-104">Eine Möglichkeit, einen Bereich mit Medien zu zeichnen, besteht darin, einen mit einem zu verwenden <xref:System.Windows.Controls.MediaElement> <xref:System.Windows.Media.VisualBrush> .</span><span class="sxs-lookup"><span data-stu-id="d832a-104">One way to paint an area with media is to use a <xref:System.Windows.Controls.MediaElement> together with a <xref:System.Windows.Media.VisualBrush>.</span></span> <span data-ttu-id="d832a-105">Verwenden <xref:System.Windows.Controls.MediaElement> Sie, um das Medium zu laden und wiederzugeben, und verwenden Sie es dann zum Festlegen der- <xref:System.Windows.Media.VisualBrush.Visual%2A> Eigenschaft von <xref:System.Windows.Media.VisualBrush> .</span><span class="sxs-lookup"><span data-stu-id="d832a-105">Use the <xref:System.Windows.Controls.MediaElement> to load and play the media, and then use it to set the <xref:System.Windows.Media.VisualBrush.Visual%2A> property of the <xref:System.Windows.Media.VisualBrush>.</span></span> <span data-ttu-id="d832a-106">Anschließend können Sie mit dem <xref:System.Windows.Media.VisualBrush> einen Bereich mit den geladenen Medien zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d832a-106">You can then use the <xref:System.Windows.Media.VisualBrush> to paint an area with the loaded media.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d832a-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d832a-107">Example</span></span>  
 <span data-ttu-id="d832a-108">Im folgenden Beispiel wird ein <xref:System.Windows.Controls.MediaElement> und ein verwendet <xref:System.Windows.Media.VisualBrush> , um die <xref:System.Windows.Controls.TextBlock.Foreground%2A> eines-Steuer Elements <xref:System.Windows.Controls.TextBlock> mit Video zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d832a-108">The following example uses a <xref:System.Windows.Controls.MediaElement> and a <xref:System.Windows.Media.VisualBrush> to paint the <xref:System.Windows.Controls.TextBlock.Foreground%2A> of a <xref:System.Windows.Controls.TextBlock> control with video.</span></span> <span data-ttu-id="d832a-109">In diesem Beispiel wird die- <xref:System.Windows.Controls.MediaElement.IsMuted%2A> Eigenschaft des auf festgelegt <xref:System.Windows.Controls.MediaElement> `true` , sodass kein Sound erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="d832a-109">This example sets the <xref:System.Windows.Controls.MediaElement.IsMuted%2A> property of the <xref:System.Windows.Controls.MediaElement> to `true` so that it produces no sound.</span></span>  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundinline)]  
  
## <a name="example"></a><span data-ttu-id="d832a-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d832a-110">Example</span></span>  
 <span data-ttu-id="d832a-111">Da <xref:System.Windows.Media.VisualBrush> von der-Klasse erbt <xref:System.Windows.Media.TileBrush> , stellt es mehrere Tick Modi bereit.</span><span class="sxs-lookup"><span data-stu-id="d832a-111">Because <xref:System.Windows.Media.VisualBrush> inherits from the <xref:System.Windows.Media.TileBrush> class, it provides several tiling modes.</span></span> <span data-ttu-id="d832a-112">Durch Festlegen der <xref:System.Windows.Media.TileBrush.TileMode%2A> -Eigenschaft eines <xref:System.Windows.Media.VisualBrush> auf <xref:System.Windows.Media.TileMode.Tile> und durch Festlegen der- <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft auf einen Wert, der kleiner als der zu Zeichnungs enden Bereich ist, können Sie ein Kachel Muster erstellen.</span><span class="sxs-lookup"><span data-stu-id="d832a-112">By setting the <xref:System.Windows.Media.TileBrush.TileMode%2A> property of a <xref:System.Windows.Media.VisualBrush> to <xref:System.Windows.Media.TileMode.Tile> and by setting its <xref:System.Windows.Media.TileBrush.Viewport%2A> property to a value smaller than the area that you are painting, you can create a tiled pattern.</span></span>  
  
 <span data-ttu-id="d832a-113">Das folgende Beispiel ist mit dem vorherigen Beispiel identisch, mit dem Unterschied, dass <xref:System.Windows.Media.VisualBrush> ein Muster aus dem Video generiert.</span><span class="sxs-lookup"><span data-stu-id="d832a-113">The following example is identical to the previous example, except that the <xref:System.Windows.Media.VisualBrush> generates a pattern from the video.</span></span>  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundtiledinline)]  
  
 <span data-ttu-id="d832a-114">Informationen zum Hinzufügen einer Inhalts Datei (z. b. einer Mediendatei) zu Ihrer Anwendung finden Sie unter [WPF-Anwendungs Ressource, Inhalts-und Datendateien](../app-development/wpf-application-resource-content-and-data-files.md).</span><span class="sxs-lookup"><span data-stu-id="d832a-114">For information about how to add a content file, such as a media file, to your application, see [WPF Application Resource, Content, and Data Files](../app-development/wpf-application-resource-content-and-data-files.md).</span></span> <span data-ttu-id="d832a-115">Wenn Sie eine Mediendatei hinzufügen, müssen Sie Sie als Inhalts Datei und nicht als Ressourcen Datei hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d832a-115">When you add a media file, you must add it as a content file, not as a resource file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d832a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d832a-116">See also</span></span>

- <xref:System.Windows.Media.VisualBrush>
- [<span data-ttu-id="d832a-117">Zeichnen mit Bildern, Zeichnungen und visuellen Elementen</span><span class="sxs-lookup"><span data-stu-id="d832a-117">Painting with Images, Drawings, and Visuals</span></span>](painting-with-images-drawings-and-visuals.md)
- [<span data-ttu-id="d832a-118">Übersicht über TileBrush</span><span class="sxs-lookup"><span data-stu-id="d832a-118">TileBrush Overview</span></span>](tilebrush-overview.md)
- [<span data-ttu-id="d832a-119">Übersicht über Multimedia</span><span class="sxs-lookup"><span data-stu-id="d832a-119">Multimedia Overview</span></span>](multimedia-overview.md)
