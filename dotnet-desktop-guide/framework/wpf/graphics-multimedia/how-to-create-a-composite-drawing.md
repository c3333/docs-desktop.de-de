---
title: 'Gewusst wie: Erstellen einer zusammengesetzten Zeichnung'
ms.date: 03/30/2017
helpviewer_keywords:
- drawings [WPF], composite
- composite drawings [WPF]
- graphics [WPF], composite drawings
ms.assetid: 066eb0ab-5f0e-439d-85c6-dca60af269fc
ms.openlocfilehash: 0af7fbca593627ebe8cd102a02617a27eac50aa5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978224"
---
# <a name="how-to-create-a-composite-drawing"></a>Gewusst wie: Erstellen einer zusammengesetzten Zeichnung
Dieses Beispiel zeigt, wie Sie mithilfe <xref:System.Windows.Media.DrawingGroup> von komplexe Zeichnungen erstellen, indem Sie mehrere <xref:System.Windows.Media.Drawing> Objekte zu einer einzelnen zusammengesetzten Zeichnung kombinieren.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.DrawingGroup> , um eine zusammengesetzte Zeichnung aus den <xref:System.Windows.Media.GeometryDrawing> -und-Objekten zu erstellen <xref:System.Windows.Media.ImageDrawing> . In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.  
  
 ![Eine DrawingGroup mit mehreren Zeichnungen](./media/graphicsmm-simple.jpg "graphicsmm_simple")  
Eine zusammengesetzte Zeichnung, die mit DrawingGroup erstellt wird  
  
 Beachten Sie den grauen Rahmen, in dem die Begrenzungen der Zeichnung angezeigt werden.  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMSimpleDrawingGroupExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupExample.cs#graphicsmmsimpledrawinggroupexample)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMSimpleDrawingGroupExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupExample.xaml#graphicsmmsimpledrawinggroupexample)]  
  
 Sie können eine verwenden, um eine, die-,-,- <xref:System.Windows.Media.DrawingGroup> <xref:System.Windows.Media.DrawingGroup.Transform%2A> oder- <xref:System.Windows.Media.DrawingGroup.Opacity%2A> Einstellung <xref:System.Windows.Media.DrawingGroup.OpacityMask%2A> <xref:System.Windows.Media.DrawingGroup.BitmapEffect%2A> <xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A> <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> auf die darin enthaltenen Zeichnungen anzuwenden. Da ein <xref:System.Windows.Media.DrawingGroup> auch ein ist <xref:System.Windows.Media.Drawing> , kann es andere- <xref:System.Windows.Media.DrawingGroup> Objekte enthalten.  
  
 Das folgende Beispiel ähnelt dem vorherigen Beispiel, mit dem Unterschied, dass es zusätzliche <xref:System.Windows.Media.DrawingGroup> -Objekte verwendet, um Bitmapeffekte und eine Deck Kraft Maske auf einige ihrer Zeichnungen anzuwenden. In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.  
  
 ![Eine DrawingGroup mit mehreren Zeichnungen](./media/graphicsmm-multiple.jpg "graphicsmm_multiple")  
Zusammengesetzte Zeichnung mit mehreren DrawingGroup-Objekten  
  
 Beachten Sie den grauen Rahmen, in dem die Begrenzungen der Zeichnung angezeigt werden.  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMMultipleDrawingGroupsExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupExample.cs#graphicsmmmultipledrawinggroupsexample)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMMultipleDrawingGroupsExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupExample.xaml#graphicsmmmultipledrawinggroupsexample)]  
  
 Weitere Informationen zu <xref:System.Windows.Media.Drawing> Objekten finden Sie unter [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.DrawingGroup.BitmapEffect%2A>
- <xref:System.Windows.Media.DrawingGroup.Transform%2A>
- <xref:System.Windows.Media.DrawingGroup.OpacityMask%2A>
- <xref:System.Windows.Media.DrawingGroup.Opacity%2A>
- <xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A>
- <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A>
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
