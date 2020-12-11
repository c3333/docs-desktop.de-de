---
title: 'Vorgehensweise: Verbessern der Renderingleistung durch Zwischenspeichern eines Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- rendering performance [WPF], caching an element
- BitmapCache [WPF], improving rendering performance
- CacheMode [WPF], improving rendering performance
- performance [WPF], caching an element
- UIElement [WPF], caching
ms.assetid: 4739c1fc-60ba-4c46-aba6-f6c1a2688f19
ms.openlocfilehash: 118e8b0cca52c44788c9d5b291d710f765e7af2a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976776"
---
# <a name="how-to-improve-rendering-performance-by-caching-an-element"></a>Vorgehensweise: Verbessern der Renderingleistung durch Zwischenspeichern eines Elements
Verwenden Sie die- <xref:System.Windows.Media.BitmapCache> Klasse zum Verbessern der Renderingleistung eines komplexen <xref:System.Windows.UIElement> Um ein Element zwischenzuspeichern, erstellen Sie eine neue Instanz der <xref:System.Windows.Media.BitmapCache> -Klasse und weisen Sie der-Eigenschaft des-Elements zu <xref:System.Windows.UIElement.CacheMode%2A> . Sie können einen <xref:System.Windows.Media.BitmapCache> effizient in einem wieder verwenden <xref:System.Windows.Media.BitmapCacheBrush> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie ein komplexes Element erstellt und als Bitmap zwischengespeichert wird. Dadurch wird die Leistung verbessert, wenn das Element animiert wird. Das-Element ist ein Zeichenbereich, der Shape-Geometrien mit vielen Vertices enthält. Eine <xref:System.Windows.Media.BitmapCache> mit Standardwerten wird der <xref:System.Windows.UIElement.CacheMode%2A> der Canvas zugewiesen, und eine Animation zeigt die glatte Skalierung der zwischengespeicherten Bitmap an.  
  
 [!code-xaml[System.Windows.Media.BitmapCache#_BitmapCacheXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcache/cs/window1.xaml#_bitmapcachexaml)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.BitmapCache>
- <xref:System.Windows.Media.BitmapCacheBrush>
- <xref:System.Windows.UIElement.CacheMode%2A>
- [Vorgehensweise: Verwenden eines zwischengespeicherten Elements als Pinsel](how-to-use-a-cached-element-as-a-brush.md)
