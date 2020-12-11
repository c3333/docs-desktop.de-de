---
title: 'Gewusst wie: Skalieren eines Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], elements
- graphics [WPF], scaling elements
ms.assetid: 18158d94-bbe7-4f6a-814e-84d27fa748bf
ms.openlocfilehash: 34d954f68747be9eedc0ef71634e0c18b411d260
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977312"
---
# <a name="how-to-scale-an-element"></a>Gewusst wie: Skalieren eines Elements
Dieses Beispiel zeigt, wie ein- <xref:System.Windows.Media.ScaleTransform> Element zum Skalieren eines Elements verwendet wird.  
  
 Verwenden <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> , um die Größe des Elements mit dem angegebenen Faktor zu ändern. Beispielsweise wird <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> das-Element mit dem Wert 1,5 auf 150 Prozent seiner ursprünglichen Breite gestreckt. <xref:System.Windows.Media.ScaleTransform.ScaleY%2A>Der Wert 0,5 verkleinert die Höhe eines Elements um 50 Prozent.  
  
 Verwenden <xref:System.Windows.Media.ScaleTransform.CenterX%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.ScaleTransform.CenterY%2A> , um den Punkt anzugeben, der die Mitte des Skalierungs Vorgangs ist. Standardmäßig wird eine <xref:System.Windows.Media.ScaleTransform> am Punkt (0,0) zentriert, der der oberen linken Ecke des Rechtecks entspricht. Dies hat den Effekt, dass das Element verschoben wird, und auch, dass es größer erscheint, denn wenn Sie ein anwenden <xref:System.Windows.Media.Transform> , ändern Sie den Koordinaten Bereich, in dem sich das Objekt befindet.  
  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.ScaleTransform> , um die Größe von 50 x 50 zu verdoppeln <xref:System.Windows.Shapes.Rectangle> . Der <xref:System.Windows.Media.ScaleTransform> hat den Wert 0 (Standard) für <xref:System.Windows.Media.ScaleTransform.CenterX%2A> und <xref:System.Windows.Media.ScaleTransform.CenterY%2A> .  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[transformsSample#21](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#21)]  
  
 In der Regel legen Sie <xref:System.Windows.Media.ScaleTransform.CenterX%2A> und <xref:System.Windows.Media.ScaleTransform.CenterY%2A> auf den Mittelpunkt des Objekts fest, das skaliert wird: ( <xref:System.Windows.FrameworkElement.Width%2A> /2, <xref:System.Windows.FrameworkElement.Height%2A> /2).  
  
 Das folgende Beispiel zeigt eine andere <xref:System.Windows.Shapes.Rectangle> , die die Größe verdoppelt, jedoch den <xref:System.Windows.Media.ScaleTransform> Wert 25 für <xref:System.Windows.Media.ScaleTransform.CenterX%2A> und <xref:System.Windows.Media.ScaleTransform.CenterY%2A> , was der Mitte des Rechtecks entspricht.  
  
 [!code-xaml[transformsSample#22](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#22)]  
  
 Die folgende Abbildung zeigt den Unterschied zwischen den beiden <xref:System.Windows.Media.ScaleTransform> Vorgängen. Die gepunktete Linie stellt die Größe und die Position des Rechtecks vor der Skalierung dar.  
  
 ![2-fach-Skalierung mit unterschiedlichen Mittelpunkten](./media/wcpsdk-graphicsmm-scalecenter.gif "wcpsdk_graphicsmm_scalecenter")  
Zwei ScaleTransform-Vorgänge mit identischen ScaleX- und ScaleY-Werten aber unterschiedlichen Mittelpunkten  
  
 Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Transform>
- <xref:System.Windows.Media.ScaleTransform>
- [Übersicht über Transformationen](transforms-overview.md)
- [Artikel zu Vorgehensweisen](transformations-how-to-topics.md)
