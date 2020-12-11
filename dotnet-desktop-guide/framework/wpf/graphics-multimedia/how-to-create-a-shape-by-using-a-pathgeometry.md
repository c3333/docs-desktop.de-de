---
title: 'Gewusst wie: Erstellen einer Form mithilfe von PathGeometry'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], creating with PathGeometry class
- graphics [WPF], shapes
ms.assetid: 49a4a8b7-e738-45be-8dac-b54a6d8f5b21
ms.openlocfilehash: bdf3c937bfff1780a72e8743bc86a3c3dad2558d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977515"
---
# <a name="how-to-create-a-shape-by-using-a-pathgeometry"></a>Gewusst wie: Erstellen einer Form mithilfe von PathGeometry
In diesem Beispiel wird gezeigt, wie eine Form mithilfe der-Klasse erstellt wird <xref:System.Windows.Media.PathGeometry> . <xref:System.Windows.Media.PathGeometry> Objekte bestehen aus einem oder mehreren- <xref:System.Windows.Media.PathFigure> Objekten, die jeweils <xref:System.Windows.Media.PathFigure> eine andere "Abbildung" oder Form darstellen. Jede <xref:System.Windows.Media.PathFigure> besteht aus einem oder mehreren- <xref:System.Windows.Media.PathSegment> Objekten, die jeweils einen verbundenen Teil der Abbildung oder Form darstellen. Zu den Segment Typen zählen <xref:System.Windows.Media.LineSegment> , <xref:System.Windows.Media.ArcSegment> und <xref:System.Windows.Media.BezierSegment> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine <xref:System.Windows.Media.PathGeometry> zum Erstellen eines Dreiecks verwendet. Die  <xref:System.Windows.Media.PathGeometry> wird mit einem- <xref:System.Windows.Shapes.Path> Element angezeigt.  
  
 [!code-xaml[GeometrySample#49](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#49)]  
  
 Die folgende Abbildung zeigt die im vorherigen Beispiel erstellte Form.  
  
 ![Eine PathGeometry](./media/wcpsdk-graphicsmm-pathgeometry-triangle.gif "wcpsdk_graphicsmm_pathgeometry_triangle")  
Ein mit PathGeometry erstelltes Dreieck  
  
 Im vorherigen Beispiel wurde gezeigt, wie eine relativ einfache Form, ein Dreieck, erstellt wird. Ein <xref:System.Windows.Media.PathGeometry> kann auch verwendet werden, um komplexere Formen zu erstellen, einschließlich Bögen und Kurven. Beispiele finden Sie unter [Erstellen eines elliptischen Bogens](how-to-create-an-elliptical-arc.md), [Erstellen einer kubischen Bezier-Kurve](how-to-create-a-cubic-bezier-curve.md)und [Erstellen einer quadratischen Bezier-Kurve](how-to-create-a-quadratic-bezier-curve.md).  
  
 Dieses Beispiel ist Teil eines größeren Beispiels. Das vollständige Beispiel finden Sie unter [Beispiel für Geometrien](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Geometry).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.GeometryDrawing>
- [Übersicht über die Geometrie](geometry-overview.md)
- [Beispiel für Geometry](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Geometry)
