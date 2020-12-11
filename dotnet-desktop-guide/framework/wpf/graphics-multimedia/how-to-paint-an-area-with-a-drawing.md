---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einer Zeichnung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], painting with drawings
- painting [WPF], with drawings
- drawings [WPF], painting with
ms.assetid: c10dc4b1-09b1-41e8-ad14-456b5fb377df
ms.openlocfilehash: 6b204ae631912181333e2559ebadcdc37e7693b7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978185"
---
# <a name="how-to-paint-an-area-with-a-drawing"></a>Gewusst wie: Zeichnen eines Bereichs mit einer Zeichnung
Dieses Beispiel zeigt, wie Sie einen Bereich mit einer Zeichnung zeichnen. Um einen Bereich mit einer Zeichnung zu zeichnen, verwenden Sie ein <xref:System.Windows.Media.DrawingBrush> -Objekt und ein-Objekt oder mehrere- <xref:System.Windows.Media.Drawing> Objekte.   Im folgenden Beispiel wird ein- <xref:System.Windows.Media.DrawingBrush> Objekt verwendet, um ein-Objekt mit einer Zeichnung zweier Ellipsen zu zeichnen.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[drawingbrush_snip#DrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_snip/CS/DrawingBrushExample.xaml#drawingbrushexamplewholepage)]  
  
 [!code-csharp[drawingbrush_procedural_snip#DrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_procedural_snip/CSharp/DrawingBrushExample.cs#drawingbrushexamplewholepage)]
 [!code-vb[drawingbrush_procedural_snip#DrawingBrushExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/drawingbrush_procedural_snip/VisualBasic/DrawingBrushExample.vb#drawingbrushexamplewholepage)]  
  
 Die folgende Abbildung zeigt die Ausgabe des Beispiels.  
  
 ![Ausgabe von einem DrawingBrush](./media/graphicsmm-drawingbrush-simple.png "graphicsmm_drawingbrush_simple")  
  
 (Der Mittelpunkt der Form ist weiß aus     [den Untersteuern der Füllung einer zusammengesetzten Form](how-to-control-the-fill-of-a-composite-shape.md)beschriebenen Gründen.)  
  
 Durch Festlegen <xref:System.Windows.Media.DrawingBrush> der Eigenschaften und des-Objekts <xref:System.Windows.Media.TileBrush.Viewport%2A> <xref:System.Windows.Media.TileBrush.TileMode%2A> können Sie ein sich wiederholendes Muster erstellen. Im folgenden Beispiel wird ein Objekt mit einem aus einer Zeichnung von zwei Ellipsen erstellten Muster gezeichnet.  
  
 [!code-xaml[drawingbrush_snip#TiledDrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_snip/CS/TiledDrawingBrushExample.xaml#tileddrawingbrushexamplewholepage)]  
  
 [!code-csharp[drawingbrush_procedural_snip#TiledDrawingBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/drawingbrush_procedural_snip/CSharp/TiledDrawingBrushExample.cs#tileddrawingbrushexamplewholepage)]
 [!code-vb[drawingbrush_procedural_snip#TiledDrawingBrushExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/drawingbrush_procedural_snip/VisualBasic/TiledDrawingBrushExample.vb#tileddrawingbrushexamplewholepage)]  
  
 Die folgende Abbildung zeigt die Kachel <xref:System.Windows.Media.DrawingBrush> Ausgabe.  
  
 ![Gekachelte Ausgabe von einem DrawingBrush](./media/graphicsmm-drawingbrush-tiled.png "graphicsmm_drawingbrush_tiled")  
  
 Weitere Informationen zum Zeichnen von Pinsel finden Sie unterzeichnen [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen. Weitere Informationen zu <xref:System.Windows.Media.Drawing> Objekten finden Sie unter [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md).
