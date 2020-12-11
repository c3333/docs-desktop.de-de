---
title: 'Gewusst wie: Neigen eines Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- skewing elements [WPF]
- graphics [WPF], skewing elements
- classes [WPF], SkewTransform
ms.assetid: 56b65f2f-dc6e-4238-923f-ca44ec53c52f
ms.openlocfilehash: 10b00044c1c518641281e2e72cdb5a68474b5170
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975472"
---
# <a name="how-to-skew-an-element"></a>Gewusst wie: Neigen eines Elements
In diesem Beispiel wird gezeigt, wie ein-Element mit einem <xref:System.Windows.Media.SkewTransform> verzerrt wird. Eine Neigung ist eine Transformation, die den Koordinatenraum auf ungleichmäßige Art ausdehnt. Eine typische Verwendung eines <xref:System.Windows.Media.SkewTransform> ist das Simulieren der 3D-Tiefe in 2D-Objekten.  
  
 Verwenden <xref:System.Windows.Media.SkewTransform.CenterX%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.SkewTransform.CenterY%2A> , um den Mittelpunkt von anzugeben <xref:System.Windows.Media.SkewTransform> .  
  
 Verwenden Sie die-Eigenschaft und die-Eigenschaft, <xref:System.Windows.Media.SkewTransform.AngleX%2A> <xref:System.Windows.Media.SkewTransform.AngleY%2A> um den Neigungswinkel der x-Achse und der y-Achse anzugeben und um das aktuelle Koordinatensystem entlang dieser Achsen zu neigen.  
  
 Um die Auswirkung einer Schiefe-Transformation vorherzusagen, sollten Sie die <xref:System.Windows.Media.SkewTransform.AngleX%2A> x-Achsen Werte relativ zum ursprünglichen Koordinatensystem neigen. Daher wird <xref:System.Windows.Media.SkewTransform.AngleX%2A> die y-Achse für eine von 30 um 30 Grad über den Ursprung rotiert und die Werte in x-um 30 Grad von diesem Ursprung entfernt. Ebenso wird <xref:System.Windows.Media.SkewTransform.AngleY%2A> die y-Werte der Form durch eine von 30 um 30 Grad vom Ursprung entfernt. Beachten Sie, dass dieser Vorgang nicht dieselbe Wirkung erzielt, wie das Übersetzen (Bewegen) des Koordinatensystems um 30° in der X- oder Y-Achse.  
  
 Im folgenden Beispiel wird eine horizontale Neigung von 45 Grad auf ein <xref:System.Windows.Shapes.Rectangle> von einem Mittelpunkt von (0,0) angewendet.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[transformsSample#41](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/SkewTransformExample.xaml#41)]  
  
 Im folgenden Beispiel wird eine horizontale Neigung von 45 Grad auf ein <xref:System.Windows.Shapes.Rectangle> von einem Mittelpunkt von (25, 25) angewendet.  
  
 [!code-xaml[transformsSample#42](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/SkewTransformExample.xaml#42)]  
  
 Im folgenden Beispiel wird eine vertikale Neigung von 45 Grad auf ein <xref:System.Windows.Shapes.Rectangle> von einem Mittelpunkt von (25, 25) angewendet.  
  
 [!code-xaml[transformsSample#43](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/SkewTransformExample.xaml#43)]  
  
 Die folgenden Abbildungen zeigen die verschiedenen Neigungen, die in diesem Beispiel verwendet werden.  
  
 ![SkewTransform-Beispiele](./media/img-wcpsdk-graphicsmm-skewtransformexample.gif "img_wcpsdk_graphicsmm_skewtransformexample")  
Die drei SkewTransform-Beispiele veranschaulicht  
  
 Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Transform>
- <xref:System.Windows.Media.SkewTransform>
- [Übersicht über Transformationen](transforms-overview.md)
- [Artikel zu Vorgehensweisen](transformations-how-to-topics.md)
