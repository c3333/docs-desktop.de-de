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
# <a name="how-to-paint-an-area-with-a-video"></a>Gewusst wie: Zeichnen eines Bereichs mit einem Video
Dieses Beispiel zeigt, wie Sie einen Bereich mit Medien zeichnen. Eine Möglichkeit, einen Bereich mit Medien zu zeichnen, besteht darin, einen mit einem zu verwenden <xref:System.Windows.Controls.MediaElement> <xref:System.Windows.Media.VisualBrush> . Verwenden <xref:System.Windows.Controls.MediaElement> Sie, um das Medium zu laden und wiederzugeben, und verwenden Sie es dann zum Festlegen der- <xref:System.Windows.Media.VisualBrush.Visual%2A> Eigenschaft von <xref:System.Windows.Media.VisualBrush> . Anschließend können Sie mit dem <xref:System.Windows.Media.VisualBrush> einen Bereich mit den geladenen Medien zeichnen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein <xref:System.Windows.Controls.MediaElement> und ein verwendet <xref:System.Windows.Media.VisualBrush> , um die <xref:System.Windows.Controls.TextBlock.Foreground%2A> eines-Steuer Elements <xref:System.Windows.Controls.TextBlock> mit Video zu zeichnen. In diesem Beispiel wird die- <xref:System.Windows.Controls.MediaElement.IsMuted%2A> Eigenschaft des auf festgelegt <xref:System.Windows.Controls.MediaElement> `true` , sodass kein Sound erzeugt wird.  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundinline)]  
  
## <a name="example"></a>Beispiel  
 Da <xref:System.Windows.Media.VisualBrush> von der-Klasse erbt <xref:System.Windows.Media.TileBrush> , stellt es mehrere Tick Modi bereit. Durch Festlegen der <xref:System.Windows.Media.TileBrush.TileMode%2A> -Eigenschaft eines <xref:System.Windows.Media.VisualBrush> auf <xref:System.Windows.Media.TileMode.Tile> und durch Festlegen der- <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft auf einen Wert, der kleiner als der zu Zeichnungs enden Bereich ist, können Sie ein Kachel Muster erstellen.  
  
 Das folgende Beispiel ist mit dem vorherigen Beispiel identisch, mit dem Unterschied, dass <xref:System.Windows.Media.VisualBrush> ein Muster aus dem Video generiert.  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundtiledinline)]  
  
 Informationen zum Hinzufügen einer Inhalts Datei (z. b. einer Mediendatei) zu Ihrer Anwendung finden Sie unter [WPF-Anwendungs Ressource, Inhalts-und Datendateien](../app-development/wpf-application-resource-content-and-data-files.md). Wenn Sie eine Mediendatei hinzufügen, müssen Sie Sie als Inhalts Datei und nicht als Ressourcen Datei hinzufügen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.VisualBrush>
- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
- [Übersicht über TileBrush](tilebrush-overview.md)
- [Übersicht über Multimedia](multimedia-overview.md)
