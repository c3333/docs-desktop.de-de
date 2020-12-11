---
title: 'Gewusst wie: Erstellen einer GeometryDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], renderable
- renderable shapes [WPF]
- graphics [WPF], GeometryDrawing class
- classes [WPF], GeometryDrawing
ms.assetid: 11d3c096-91ba-4d41-9bba-aeac0db70f97
ms.openlocfilehash: f5cdcfdb68ad8030bcbd6c689f45a8baddd000e1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977607"
---
# <a name="how-to-create-a-geometrydrawing"></a>Gewusst wie: Erstellen einer GeometryDrawing
In diesem Beispiel wird gezeigt, wie ein erstellt und angezeigt wird <xref:System.Windows.Media.GeometryDrawing> . Mit einem <xref:System.Windows.Media.GeometryDrawing> können Sie eine Form mit einer Füllung und einem Umriss erstellen, indem Sie eine <xref:System.Windows.Media.Pen> und eine <xref:System.Windows.Media.Brush> mit einem verknüpfen <xref:System.Windows.Media.Geometry> . Der <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> beschreibt die Struktur der Form, <xref:System.Windows.Media.GeometryDrawing.Brush%2A> beschreibt die Füllung der Form und <xref:System.Windows.Media.GeometryDrawing.Pen%2A> beschreibt die Kontur der Form.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein-Typ verwendet <xref:System.Windows.Media.GeometryDrawing> , um eine Form zu erzeugen. Die Form wird durch ein <xref:System.Windows.Media.GeometryGroup> und zwei- <xref:System.Windows.Media.EllipseGeometry> Objekte beschrieben. Das Innere der Form wird mit einem <xref:System.Windows.Media.LinearGradientBrush> gezeichnet, und der Umriss wird mit einem gezeichnet <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen> . Die <xref:System.Windows.Media.GeometryDrawing> wird mit einem <xref:System.Windows.Media.ImageDrawing> -Element und einem- <xref:System.Windows.Controls.Image> Element angezeigt.  
  
 [!code-csharp[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/GeometryDrawingExample.cs#geometrydrawingexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/GeometryDrawingExample.xaml#geometrydrawingexamplewholepage)]  
  
 In der folgenden Abbildung wird das resultierende gezeigt <xref:System.Windows.Media.GeometryDrawing> .  
  
 ![Eine GeometryDrawing von zwei Ellipsen](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")  
  
 Um komplexere Zeichnungen zu erstellen, können Sie mehrere Zeichnungsobjekte in einer einzelnen zusammengesetzten Zeichnung mit einem kombinieren <xref:System.Windows.Media.DrawingGroup> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.DrawingGroup>
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
- [Übersicht über die Geometrie](geometry-overview.md)
- [Erstellen einer zusammengesetzten Zeichnung](how-to-create-a-composite-drawing.md)
