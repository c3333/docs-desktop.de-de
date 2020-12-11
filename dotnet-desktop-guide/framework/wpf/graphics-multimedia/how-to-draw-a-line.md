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
# <a name="how-to-draw-a-line"></a><span data-ttu-id="ac60a-102">Gewusst wie: Zeichnen einer Linie</span><span class="sxs-lookup"><span data-stu-id="ac60a-102">How to: Draw a Line</span></span>
<span data-ttu-id="ac60a-103">In diesem Beispiel wird gezeigt, wie Sie Linien mithilfe des- <xref:System.Windows.Shapes.Line> Elements zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ac60a-103">This example shows you how to draw lines by using the <xref:System.Windows.Shapes.Line> element.</span></span>  
  
 <span data-ttu-id="ac60a-104">Erstellen Sie ein-Element, um eine Linie zu zeichnen <xref:System.Windows.Shapes.Line> .</span><span class="sxs-lookup"><span data-stu-id="ac60a-104">To draw a line, create a <xref:System.Windows.Shapes.Line> element.</span></span> <span data-ttu-id="ac60a-105">Verwenden <xref:System.Windows.Shapes.Line.X1%2A> Sie die <xref:System.Windows.Shapes.Line.Y1%2A> Eigenschaften und, um den Startpunkt festzulegen, und verwenden Sie dessen-Eigenschaft und-Eigenschaft <xref:System.Windows.Shapes.Line.X2%2A> <xref:System.Windows.Shapes.Line.Y2%2A> , um den Endpunkt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ac60a-105">Use its <xref:System.Windows.Shapes.Line.X1%2A> and <xref:System.Windows.Shapes.Line.Y1%2A> properties to set its start point; and use its <xref:System.Windows.Shapes.Line.X2%2A> and <xref:System.Windows.Shapes.Line.Y2%2A> properties to set its end point.</span></span> <span data-ttu-id="ac60a-106">Legen Sie schließlich den Wert und fest, <xref:System.Windows.Shapes.Shape.Stroke%2A> <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> da eine Zeile ohne einen Strich unsichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="ac60a-106">Finally, set its <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> because a line without a stroke is invisible.</span></span>  
  
 <span data-ttu-id="ac60a-107">Das Festlegen des- <xref:System.Windows.Shapes.Shape.Fill%2A> Elements für eine Linie hat keine Auswirkung, da eine Linie kein innere hat.</span><span class="sxs-lookup"><span data-stu-id="ac60a-107">Setting the <xref:System.Windows.Shapes.Shape.Fill%2A> element for a line has no effect, because a line has no interior.</span></span>  
  
 <span data-ttu-id="ac60a-108">Im folgenden Beispiel werden drei Zeilen innerhalb eines- <xref:System.Windows.Controls.Canvas> Elements gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ac60a-108">The following example draws three lines inside a <xref:System.Windows.Controls.Canvas> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ac60a-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ac60a-109">Example</span></span>  
 [!code-xaml[drawingwithshapeelements#LineExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/lineexample.xaml#lineexample1)]  
  
 <span data-ttu-id="ac60a-110">Dieses Beispiel ist Teil einer größeren Stichprobe. Das komplette Beispiel finden Sie unter [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements).</span><span class="sxs-lookup"><span data-stu-id="ac60a-110">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac60a-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac60a-111">See also</span></span>

- <xref:System.Windows.Shapes.Line>
- [<span data-ttu-id="ac60a-112">Beispiel für Shape-Elemente</span><span class="sxs-lookup"><span data-stu-id="ac60a-112">Shape Elements Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements)
