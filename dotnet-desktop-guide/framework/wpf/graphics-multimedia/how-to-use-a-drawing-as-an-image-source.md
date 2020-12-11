---
title: 'Gewusst wie: Verwenden einer Zeichnung als Bildquelle'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], drawings [WPF], as image sources
- image sources [WPF], drawings
- drawings [WPF], as image sources
ms.assetid: dcf71c7b-9e86-4b8e-8e39-0d0ce0389ef4
ms.openlocfilehash: d4b91a6495e1c54400d5fbfe43b6311d908565a7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975464"
---
# <a name="how-to-use-a-drawing-as-an-image-source"></a>Gewusst wie: Verwenden einer Zeichnung als Bildquelle
Dieses Beispiel zeigt, wie Sie einen <xref:System.Windows.Media.Drawing> als <xref:System.Windows.Controls.Image.Source%2A> für ein- <xref:System.Windows.Controls.Image> Steuerelement verwenden. <xref:System.Windows.Media.Drawing>Wenn Sie ein mit einem-Steuerelement anzeigen möchten <xref:System.Windows.Controls.Image> , verwenden <xref:System.Windows.Media.DrawingImage> Sie als die des <xref:System.Windows.Controls.Image> -Steuer Elements, <xref:System.Windows.Controls.Image.Source%2A> und legen <xref:System.Windows.Media.DrawingImage> Sie die-Eigenschaft des-Objekts <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> auf die anzuzeigende Zeichnung fest  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.DrawingImage> und ein-Steuerelement verwendet <xref:System.Windows.Controls.Image> , um einen anzuzeigen <xref:System.Windows.Media.GeometryDrawing> . Dieses Beispiel erzeugt die folgende Ausgabe:  
  
 ![Eine GeometryDrawing von zwei Ellipsen](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")  
Ein DrawingImage  
  
 [!code-csharp[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingImageExample.cs#drawingimageexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingImageExample.xaml#drawingimageexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Freezable.Freeze%2A>
- [Zeichnen eines Bilds mit einer ImageDrawing](how-to-draw-an-image-using-imagedrawing.md)
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
- [Übersicht über Freezable-Objekte](../advanced/freezable-objects-overview.md)
- [PresentationOptions:Freeze-Attribut](../advanced/presentationoptions-freeze-attribute.md)
