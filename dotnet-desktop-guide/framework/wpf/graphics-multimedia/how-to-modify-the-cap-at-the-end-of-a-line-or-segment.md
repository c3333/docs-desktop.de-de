---
title: 'Gewusst wie: Ändern des Endes einer Zeile oder eines Segments'
ms.date: 03/30/2017
helpviewer_keywords:
- Shape elements [WPF], ends
- Shape elements [WPF], caps
- graphics [WPF], Shape caps
ms.assetid: f4bf3416-b3d8-4568-b98e-3eda8f6dbf7a
ms.openlocfilehash: 5f755d7b4d1682755ea461121f91c0666d450ad1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978191"
---
# <a name="how-to-modify-the-cap-at-the-end-of-a-line-or-segment"></a>Gewusst wie: Ändern des Endes einer Zeile oder eines Segments
In diesem Beispiel wird gezeigt, wie die Form am Anfang oder Ende eines geöffneten Elements geändert wird <xref:System.Windows.Shapes.Shape> . Um die Obergrenze am Anfang eines geöffneten zu ändern, verwenden Sie die zugehörige- <xref:System.Windows.Shapes.Shape> <xref:System.Windows.Shapes.Shape.StrokeStartLineCap%2A> Eigenschaft. Um die Obergrenze am Ende eines geöffneten zu ändern, verwenden Sie die zugehörige- <xref:System.Windows.Shapes.Shape> <xref:System.Windows.Shapes.Shape.StrokeEndLineCap%2A> Eigenschaft. Informationen zum Anzeigen der verfügbaren Zeilenenden finden Sie unter der- <xref:System.Windows.Media.PenLineCap> Enumeration.  
  
> [!NOTE]
> Diese Eigenschaft wirkt sich nur auf eine geöffnete Form aus, z <xref:System.Windows.Shapes.Line> . b. ein, ein <xref:System.Windows.Shapes.Polyline> oder ein offenes <xref:System.Windows.Shapes.Path> Element.  
  
 Im folgenden Beispiel werden vier Elemente gezeichnet, und es wird <xref:System.Windows.Shapes.Polyline> jeweils ein anderer Satz von Formen an den Enden der einzelnen Elemente verwendet.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[drawingwithshapeelements#ShapeLineCaps1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/linecapsandjoinsexample.xaml#shapelinecaps1)]  
  
 Dieses Beispiel ist Teil einer größeren Stichprobe. Das komplette Beispiel finden Sie unter [Beispiel für Shape-Elemente](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ShapeElements).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Shapes.Polyline>
- <xref:System.Windows.Media.PenLineCap>
