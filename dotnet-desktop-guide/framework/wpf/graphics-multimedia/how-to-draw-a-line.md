---
title: 'Gewusst wie: Zeichnen einer Linie'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], lines
- graphics [WPF], lines
- lines [WPF], drawing
ms.assetid: 0513ee01-6b27-4bb3-85f3-3a3e6710d80e
ms.openlocfilehash: a803c1be01086ca8911ef4cc33bd67697239e2c0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972262"
---
# <a name="how-to-draw-a-line"></a>Gewusst wie: Zeichnen einer Linie
In diesem Beispiel wird gezeigt, wie Sie Linien mithilfe des- <xref:System.Windows.Shapes.Line> Elements zeichnen.  
  
 Erstellen Sie ein-Element, um eine Linie zu zeichnen <xref:System.Windows.Shapes.Line> . Verwenden <xref:System.Windows.Shapes.Line.X1%2A> Sie die <xref:System.Windows.Shapes.Line.Y1%2A> Eigenschaften und, um den Startpunkt festzulegen, und verwenden Sie dessen-Eigenschaft und-Eigenschaft <xref:System.Windows.Shapes.Line.X2%2A> <xref:System.Windows.Shapes.Line.Y2%2A> , um den Endpunkt festzulegen. Legen Sie schließlich den Wert und fest, <xref:System.Windows.Shapes.Shape.Stroke%2A> <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> da eine Zeile ohne einen Strich unsichtbar ist.  
  
 Das Festlegen des- <xref:System.Windows.Shapes.Shape.Fill%2A> Elements für eine Linie hat keine Auswirkung, da eine Linie kein innere hat.  
  
 Im folgenden Beispiel werden drei Zeilen innerhalb eines- <xref:System.Windows.Controls.Canvas> Elements gezeichnet.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[drawingwithshapeelements#LineExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/lineexample.xaml#lineexample1)]  
  
 Dieses Beispiel ist Teil einer größeren Stichprobe. Das komplette Beispiel finden Sie unter [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Shapes.Line>
- [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements)
