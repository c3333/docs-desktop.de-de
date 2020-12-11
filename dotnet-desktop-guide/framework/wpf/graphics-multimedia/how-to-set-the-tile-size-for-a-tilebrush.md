---
title: 'Gewusst wie: Festlegen der Flächengröße für ein TileBrush-Objekt'
ms.date: 03/30/2017
helpviewer_keywords:
- TileBrush [WPF], size of tile properties
- Viewport property of TileBrush [WPF]
ms.assetid: 04f41090-1b46-4e36-832f-d27d28708b8c
ms.openlocfilehash: af7bab59a292549b29dad9b6a7417f22b1b84e48
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975476"
---
# <a name="how-to-set-the-tile-size-for-a-tilebrush"></a>Gewusst wie: Festlegen der Flächengröße für ein TileBrush-Objekt

In diesem Beispiel wird gezeigt, wie die Kachel Größe für ein festgelegt wird <xref:System.Windows.Media.TileBrush> . Standardmäßig erzeugt eine <xref:System.Windows.Media.TileBrush> eine einzelne Kachel, die den zu Zeichnungs Bereich vollständig ausfüllt. Sie können dieses Verhalten überschreiben, indem Sie die <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaften und festlegen <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> .

Die- <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft gibt die Kachel Größe für einen an <xref:System.Windows.Media.TileBrush> . Standardmäßig ist der Wert der- <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft relativ zur Größe des gezeichneten Bereichs. <xref:System.Windows.Media.TileBrush.Viewport%2A>Legen Sie die-Eigenschaft auf fest, damit die-Eigenschaft eine absolute Kachel Größe angibt <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> <xref:System.Windows.Media.BrushMappingMode.Absolute> .

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird verwendet, <xref:System.Windows.Media.ImageBrush> <xref:System.Windows.Media.TileBrush> um ein Rechteck mit Kacheln zu zeichnen. Im Beispiel wird jede Kachel auf 50 Prozent um 50 Prozent des Ausgabe Bereichs (das Rechteck) festgelegt. Als Ergebnis wird das Rechteck mit vier Projektionen des Bilds gezeichnet.

Die folgende Abbildung zeigt die Ausgabe, die im Beispiel erzeugt wird:

![Ein Rechteck mit vier Kirschen, die das Ticken mit einem Bild Pinsel demonstrieren.](./media/how-to-set-the-tile-size-for-a-tilebrush/rectangle-tile-image-brush.png)

[!code-csharp[UsingImageBrush_snip#RelativeTileSizeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#relativetilesizeexample)]

Im nächsten Beispiel wird ein erstellt <xref:System.Windows.Media.ImageBrush> , dessen <xref:System.Windows.Media.TileBrush.Viewport%2A> auf `0,0,25,25` und dessen auf festgelegt <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> <xref:System.Windows.Media.BrushMappingMode.Absolute> und zum Zeichnen eines weiteren Rechtecks verwendet. Als Ergebnis erzeugt der Pinsel Flächen mit einer Breite und Höhe von 25 Pixeln.

Die folgende Abbildung zeigt die Ausgabe, die im Beispiel erzeugt wird:

![Ein Rechteck mit 48-Kirschen, das einen gekachelten TileBrush mit einem Viewport demonstriert.](./media/how-to-set-the-tile-size-for-a-tilebrush/25-x-25-viewport-tilebrush.png)

[!code-csharp[UsingImageBrush_snip#AbsoluteTileSizeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#absolutetilesizeexample)]

Die vorangehenden Beispiele sind Teil eines umfangreicheren Beispiels. Das komplette Beispiel finden Sie unter [ImageBrush Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ImageBrush).

Obwohl in diesem Beispiel die <xref:System.Windows.Media.ImageBrush> -Klasse verwendet wird, Verhalten sich die <xref:System.Windows.Media.TileBrush.Viewport%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> identisch für die anderen- <xref:System.Windows.Media.TileBrush> Objekte, d. h <xref:System.Windows.Media.DrawingBrush> . für und <xref:System.Windows.Media.VisualBrush> . Weitere Informationen zu <xref:System.Windows.Media.ImageBrush> und anderen <xref:System.Windows.Media.TileBrush> Objekten finden Sie unterzeichnen [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.TileBrush>
- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
- [Erstellen von unterschiedlichen Kachelmustern mit einem TileBrush](how-to-create-different-tile-patterns-with-a-tilebrush.md)
