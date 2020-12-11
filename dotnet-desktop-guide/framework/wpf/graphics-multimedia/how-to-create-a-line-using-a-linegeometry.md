---
title: 'Gewusst wie: Erstellen einer Linie mit einer LineGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], lines
ms.assetid: 41231b22-1f74-4c26-a8e7-a55b29f8f6bd
ms.openlocfilehash: f8c334a54f78aec7af91064a447fd18f23dcfbdc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977408"
---
# <a name="how-to-create-a-line-using-a-linegeometry"></a>Gewusst wie: Erstellen einer Linie mit einer LineGeometry
In diesem Beispiel wird gezeigt, wie die-Klasse verwendet wird <xref:System.Windows.Media.LineGeometry> , um eine Zeile zu beschreiben. Eine <xref:System.Windows.Media.LineGeometry> wird durch die Start-und Endpunkte definiert.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt und dargestellt wird <xref:System.Windows.Media.LineGeometry> .  Ein- <xref:System.Windows.Shapes.Path> Element wird verwendet, um die Zeile zu Rendering.  Da eine Linie keinen Bereich aufweist, <xref:System.Windows.Shapes.Path> wird das Objekt <xref:System.Windows.Shapes.Shape.Fill%2A> nicht angegeben. stattdessen werden die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Shapes.Shape.Stroke%2A> <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> verwendet.  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmlinegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmlinegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmlinegeometryexample)]  
  
 ![LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")  
Eine LineGeometry, gezeichnet von (10,20) bis (100,130)  
  
 Andere einfache Geometry-Klassen sind <xref:System.Windows.Media.LineGeometry> und <xref:System.Windows.Media.EllipseGeometry> . Diese Geometrien und komplexere können auch mithilfe von oder erstellt werden <xref:System.Windows.Media.PathGeometry> <xref:System.Windows.Media.StreamGeometry> . Weitere Informationen finden Sie in der [Übersicht über die Geometrie](geometry-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Geometrie](geometry-overview.md)
- [Erstellen einer zusammengesetzten Form](how-to-create-a-composite-shape.md)
- [Erstellen einer Form mithilfe einer PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md)
