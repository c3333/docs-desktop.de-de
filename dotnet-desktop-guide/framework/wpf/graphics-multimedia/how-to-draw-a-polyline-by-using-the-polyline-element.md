---
title: 'Gewusst wie: Zeichnen einer Polylinie mithilfe des Polylinien-Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- connected lines [WPF]
- polylines [WPF], drawing
- graphics [WPF], polylines
- lines [WPF], connected (see polylines)
- drawing [WPF], polylines
ms.assetid: 65db8935-d047-4295-87c4-b427ff3ad293
ms.openlocfilehash: 4871d357d81ec80b63e69e6af133ae10b4e08b15
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978195"
---
# <a name="how-to-draw-a-polyline-by-using-the-polyline-element"></a>Gewusst wie: Zeichnen einer Polylinie mithilfe des Polylinien-Elements
In diesem Beispiel wird gezeigt, wie Sie mithilfe des-Elements eine Polylinie zeichnen, bei der es sich um eine Reihe verbundener Linien handelt <xref:System.Windows.Shapes.Polyline> .  
  
 Um eine Polylinie zu zeichnen, erstellen Sie ein <xref:System.Windows.Shapes.Polyline> -Element, und verwenden <xref:System.Windows.Shapes.Polyline.Points%2A> Sie die-Eigenschaft, um die Form Scheitel Punkte anzugeben. Verwenden Sie abschließend die <xref:System.Windows.Shapes.Shape.Stroke%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> , um die polyliniengliederung zu beschreiben, da eine Linie ohne Strich unsichtbar ist.  
  
> [!NOTE]
> Da das- <xref:System.Windows.Shapes.Polyline> Element keine geschlossene Form ist, hat die- <xref:System.Windows.Shapes.Shape.Fill%2A> Eigenschaft keine Auswirkung, auch wenn Sie die Form Gliederung absichtlich schließen. Um eine geschlossene Form mit einem zu erstellen <xref:System.Windows.Shapes.Shape.Fill%2A> , verwenden Sie ein- <xref:System.Windows.Shapes.Polygon> Element.  
  
 Im folgenden Beispiel werden zwei- <xref:System.Windows.Shapes.Polyline> Elemente in einem-Element gezeichnet <xref:System.Windows.Controls.Canvas> .  
  
## <a name="example"></a>Beispiel  
 In [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] ist die gültige Syntax für Punkte eine durch Leerzeichen getrennte Liste mit durch Trennzeichen getrennten x-und y-Koordinatenpaaren.  
  
 [!code-xaml[drawingwithshapeelements#PolylineExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/polylineexample.xaml#polylineexample1)]  
  
 Obwohl in diesem Beispiel ein- <xref:System.Windows.Controls.Canvas> Element verwendet wird, das die Polylinien enthält, können Sie polylinienelemente (und alle anderen Shape-Elemente) mit beliebigen <xref:System.Windows.Controls.Panel> oder verwenden <xref:System.Windows.Controls.Control> , die nicht Text Inhalt unterstützen.  
  
 Dieses Beispiel ist Teil einer größeren Stichprobe. Das komplette Beispiel finden Sie unter [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Shapes.Polyline>
- <xref:System.Windows.Shapes.Polygon>
- <xref:System.Windows.Shapes.Shape>
- [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements)
- [Übersicht über Formen und die grundlegenden Funktionen zum Zeichnen in WPF](shapes-and-basic-drawing-in-wpf-overview.md)
