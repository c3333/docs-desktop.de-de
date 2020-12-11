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
# <a name="how-to-use-a-cached-element-as-a-brush"></a>Vorgehensweise: Verwenden eines zwischengespeicherten Elements als Pinsel
Verwenden Sie die- <xref:System.Windows.Media.BitmapCacheBrush> Klasse zur effizienten Wiederverwendung eines zwischengespeicherten Elements. Um ein Element zwischenzuspeichern, erstellen Sie eine neue Instanz der <xref:System.Windows.Media.BitmapCache> -Klasse und weisen Sie der-Eigenschaft des-Elements zu <xref:System.Windows.UIElement.CacheMode%2A> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird gezeigt, wie ein zwischengespeichertes Element wieder verwendet wird. Das zwischengespeicherte Element ist ein <xref:System.Windows.Controls.Image> Steuerelement, das ein großes Bild anzeigt. Das- <xref:System.Windows.Controls.Image> Steuerelement wird mithilfe der-Klasse als Bitmap zwischengespeichert <xref:System.Windows.Media.BitmapCache> , und der Cache wird wieder verwendet, indem es einem zugewiesen wird <xref:System.Windows.Media.BitmapCacheBrush> . Der Pinsel wird dem Hintergrund von 20-fünf-Schaltflächen zugewiesen, um eine effiziente Wiederverwendung anzuzeigen.  
  
 [!code-xaml[System.Windows.Media.BitmapCacheBrush#_BitmapCacheBrushXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcachebrush/cs/window1.xaml#_bitmapcachebrushxaml)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.BitmapCache>
- <xref:System.Windows.Media.BitmapCacheBrush>
- <xref:System.Windows.UIElement.CacheMode%2A>
- [Vorgehensweise: Verbessern der Renderingleistung durch Zwischenspeichern eines Elements](how-to-improve-rendering-performance-by-caching-an-element.md)
