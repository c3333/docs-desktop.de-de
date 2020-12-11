---
title: 'Gewusst wie: Erstellen von unterschiedlichen Kachelmustern mit einem TileBrush'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TileBrush [WPF], creating tile patterns
- tile patterns [WPF], creating
- creating [WPF], tile patterns with TileBrush
ms.assetid: 5aa46632-3527-4668-9d8d-0375c8af28aa
ms.openlocfilehash: c1051b234961eee9ae740af2abac3d64c523656c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976933"
---
# <a name="how-to-create-different-tile-patterns-with-a-tilebrush"></a>Gewusst wie: Erstellen von unterschiedlichen Kachelmustern mit einem TileBrush
In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft eines verwendet wird <xref:System.Windows.Media.TileBrush> , um ein Muster zu erstellen.  
  
 Mithilfe der- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft können Sie angeben, wie der Inhalt einer <xref:System.Windows.Media.TileBrush> wiederholt wird, d. h., Sie können einen Ausgabebereich ausfüllen. Zum Erstellen eines Musters legen Sie den <xref:System.Windows.Media.TileBrush.TileMode%2A> auf <xref:System.Windows.Media.TileMode.Tile> , <xref:System.Windows.Media.TileMode.FlipX> , oder fest <xref:System.Windows.Media.TileMode.FlipY> <xref:System.Windows.Media.TileMode.FlipXY> . Sie müssen auch die <xref:System.Windows.Media.TileBrush.Viewport%2A> der- <xref:System.Windows.Media.TileBrush> Klasse so festlegen, dass Sie kleiner ist als der Bereich, den Sie zeichnen. andernfalls wird nur eine einzelne Kachel erstellt, unabhängig von der Einstellung, die <xref:System.Windows.Media.TileBrush.TileMode%2A> Sie verwenden.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden fünf- <xref:System.Windows.Media.DrawingBrush> Objekte erstellt, die jeweils eine andere <xref:System.Windows.Media.TileBrush.TileMode%2A> Einstellung erhält und zum Zeichnen von fünf Rechtecke verwendet werden. Obwohl in diesem Beispiel die- <xref:System.Windows.Media.DrawingBrush> Klasse verwendet <xref:System.Windows.Media.TileBrush.TileMode%2A> wird, um das Verhalten zu veranschaulichen, funktioniert die- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft identisch für alle- <xref:System.Windows.Media.TileBrush> Objekte, d. h <xref:System.Windows.Media.ImageBrush> . für, <xref:System.Windows.Media.VisualBrush> und <xref:System.Windows.Media.DrawingBrush> .  
  
 In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.  
  
 ![TileBrush-Kachelbeispiel-Ausgabe](./media/graphicsmm-drawingbrushtilemodeexample.png "graphicsmm_DrawingBrushTileModeExample")  
Mit der TileMode-Eigenschaft erstellte Kachel Muster  
  
 [!code-csharp[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/TileModeExample.cs#graphicsmmdrawingbrushtilemodeexample)]
 [!code-vb[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/tilemodeexample.vb#graphicsmmdrawingbrushtilemodeexample)]
 [!code-xaml[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/TileModeExample.xaml#graphicsmmdrawingbrushtilemodeexample)]  
  
## <a name="see-also"></a>Siehe auch

- [Festlegen der Kachelgröße für einen TileBrush](how-to-set-the-tile-size-for-a-tilebrush.md)
- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
