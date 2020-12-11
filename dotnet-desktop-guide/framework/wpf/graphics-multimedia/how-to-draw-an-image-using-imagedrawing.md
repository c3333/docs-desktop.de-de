---
title: 'Gewusst wie: Zeichnen eines Bilds mit ImageDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], images
- graphics [WPF], drawing images
- images [WPF], drawing
ms.assetid: df28ab41-25fb-4ab3-b51d-7f695b24f55e
ms.openlocfilehash: f9459185bf81160b45222e7d6821e0f945ada381
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972260"
---
# <a name="how-to-draw-an-image-using-imagedrawing"></a>Gewusst wie: Zeichnen eines Bilds mit ImageDrawing
In diesem Beispiel wird gezeigt, wie ein Bild mit einem <xref:System.Windows.Media.ImageDrawing> gezeichnet wird. Ein <xref:System.Windows.Media.ImageDrawing> ermöglicht Ihnen das Anzeigen eines <xref:System.Windows.Media.ImageSource> mit <xref:System.Windows.Media.DrawingBrush> , <xref:System.Windows.Media.DrawingImage> oder <xref:System.Windows.Media.Visual> . Zum Zeichnen eines Bilds erstellen Sie eine <xref:System.Windows.Media.ImageDrawing> und legen deren <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> -und- <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> Eigenschaften fest. Die <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> -Eigenschaft gibt das zu zeichnende Bild an, und die- <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> Eigenschaft gibt die Position und die Größe jedes Bilds an.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine zusammengesetzte Zeichnung mit vier- <xref:System.Windows.Media.ImageDrawing> Objekten erstellt. Dieses Beispiel erzeugt die folgende Abbildung:  
  
 ![Mehrere DrawingImage-Objekte](./media/graphicsmm-imagedrawingexample.jpg "graphicsmm_ImageDrawingExample")  
Vier ImageDrawing-Objekte  
  
 [!code-csharp[DrawingMiscSnippets_snip#ImageDrawingExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/ImageDrawingExample.cs#imagedrawingexample)]
 [!code-xaml[DrawingMiscSnippets_snip#ImageDrawingExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/ImageDrawingExample.xaml#imagedrawingexample)]  
  
 Ein Beispiel, das eine einfache Möglichkeit zum Anzeigen eines Bilds ohne Verwendung von zeigt <xref:System.Windows.Media.ImageDrawing> , finden Sie unter [Verwenden des Image-Elements](../controls/how-to-use-the-image-element.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Freezable.Freeze%2A>
- <xref:System.Windows.Controls.Image>
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
- [Übersicht über Freezable-Objekte](../advanced/freezable-objects-overview.md)
- [PresentationOptions:Freeze-Attribut](../advanced/presentationoptions-freeze-attribute.md)
