---
title: 'Gewusst wie: Zeichnen eines Rechtecks'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], rectangles
- graphics [WPF], rectangles
- rectangles [WPF], drawing
ms.assetid: beeb57ef-fab5-4446-a38a-1588f97b4c2f
ms.openlocfilehash: 95191e9d90bc2ac32902399125d9a51192e897bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972423"
---
# <a name="how-to-draw-a-rectangle"></a>Gewusst wie: Zeichnen eines Rechtecks
In diesem Beispiel wird gezeigt, wie ein Rechteck mithilfe des-Elements gezeichnet wird <xref:System.Windows.Shapes.Rectangle> .  
  
 Um ein Rechteck zu zeichnen, erstellen Sie ein <xref:System.Windows.Shapes.Rectangle> -Element, und geben Sie dessen <xref:System.Windows.FrameworkElement.Width%2A> und an <xref:System.Windows.FrameworkElement.Height%2A> . Um den inneren Bereich des Rechtecks zu zeichnen, legen Sie dessen fest <xref:System.Windows.Shapes.Shape.Fill%2A> . Um dem Rechteck eine Kontur zuzuweisen, verwenden Sie dessen <xref:System.Windows.Shapes.Shape.Stroke%2A> -Eigenschaft und-Eigenschaft <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> .  
  
 Geben Sie die optionalen-Eigenschaft und die-Eigenschaft an, um das Rechteck mit abgerundeten Ecken anzugeben <xref:System.Windows.Shapes.Rectangle.RadiusX%2A> <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> <xref:System.Windows.Shapes.Rectangle.RadiusX%2A>Mit der-Eigenschaft und der-Eigenschaft <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> wird die x-Achse und die y-Achse der Ellipse festgelegt, die zum Abrunden der Ecken des Rechtecks verwendet wird.  
  
 Im folgenden Beispiel werden zwei- <xref:System.Windows.Shapes.Rectangle> Elemente in einem gezeichnet <xref:System.Windows.Controls.Canvas> . Das erste Rechteck verfügt über ein <xref:System.Windows.Media.Brushes.Blue%2A> Inneres. Das zweite Rechteck verfügt über eine <xref:System.Windows.Media.Brushes.Blue%2A> innere, eine <xref:System.Windows.Media.Brushes.Black%2A> Kontur und gerundete Ecken.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[drawingwithshapeelements#Rectangle1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/rectangleexample.xaml#rectangle1)]  
  
 Obwohl in diesem Beispiel ein <xref:System.Windows.Controls.Canvas> -Element verwendet wird, das die Rechtecke enthält, können Sie Rechteck Elemente (und alle anderen Shape-Elemente) mit beliebigen <xref:System.Windows.Controls.Panel> oder verwenden <xref:System.Windows.Controls.Control> , die nicht Textinhalte unterstützen. In der Tat sind Rechtecke besonders nützlich für das Bereitstellen von Hintergründen für Teile von <xref:System.Windows.Controls.Grid> Panels. Ein Beispiel finden Sie in der [Übersicht über die Tabelle](../advanced/table-overview.md).  
  
 Dieses Beispiel ist Teil einer größeren Stichprobe. Das komplette Beispiel finden Sie unter [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Shapes.Rectangle>
- [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements)
- [Übersicht über Formen und die grundlegenden Funktionen zum Zeichnen in WPF](shapes-and-basic-drawing-in-wpf-overview.md)
- [Tabellen Übersicht](../advanced/table-overview.md)
