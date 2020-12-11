---
title: 'Gewusst wie: Definieren eines Rechtecks mit RectangleGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rectangles
- rectangles [WPF], creating with RectangleGeometry class
ms.assetid: e40b8a8e-54b8-416b-a9f2-be6dca9fdf0b
ms.openlocfilehash: 146ca7017ee38ad5c1065e59662ac441e7bfbfe2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977407"
---
# <a name="how-to-define-a-rectangle-using-a-rectanglegeometry"></a>Gewusst wie: Definieren eines Rechtecks mit RectangleGeometry
In diesem Beispiel wird beschrieben, wie Sie die- <xref:System.Windows.Media.RectangleGeometry> Klasse verwenden, um ein Rechteck zu beschreiben.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt und dargestellt wird <xref:System.Windows.Media.RectangleGeometry> .  Die relative Position und die Abmessungen des Rechtecks werden durch eine- <xref:System.Windows.Rect> Struktur definiert. Die relative Position ist, `50,50` und die Höhe und die Breite `25` bilden beide ein Quadrat. Das Innere des Rechtecks wird mit einem Pinsel gezeichnet, <xref:System.Windows.Media.Brushes.LemonChiffon%2A> und der Umriss wird mit einem <xref:System.Windows.Media.Brushes.Black%2A> Strich mit einer Stärke von gezeichnet `1` .  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmrectanglegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmrectanglegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmrectanglegeometryexample)]  
  
 ![RectangleGeometry](./media/graphicsmm-rectangle.gif "graphicsmm_rectangle")  
RectangleGeometry  
  
 Obwohl in diesem Beispiel ein- <xref:System.Windows.Shapes.Path> Element zum Rendering von verwendet <xref:System.Windows.Media.RectangleGeometry> wurde, gibt es viele weitere Möglichkeiten,-Objekte zu verwenden <xref:System.Windows.Media.RectangleGeometry> . Beispielsweise kann ein <xref:System.Windows.Media.RectangleGeometry> verwendet werden, um den <xref:System.Windows.UIElement.Clip%2A> eines oder eines <xref:System.Windows.UIElement> von anzugeben <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> <xref:System.Windows.Media.GeometryDrawing> .  
  
 Andere einfache Geometry-Klassen sind <xref:System.Windows.Media.LineGeometry> und <xref:System.Windows.Media.EllipseGeometry> . Diese Geometrien und komplexere können auch mithilfe von oder erstellt werden <xref:System.Windows.Media.PathGeometry> <xref:System.Windows.Media.StreamGeometry> .  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Geometrie](geometry-overview.md)
- [Erstellen einer zusammengesetzten Form](how-to-create-a-composite-shape.md)
- [Erstellen einer Form mithilfe einer PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md)
