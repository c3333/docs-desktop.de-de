---
title: 'Gewusst wie: Angeben des Ursprungs einer Transformation mithilfe von relativen Werten'
ms.date: 03/30/2017
helpviewer_keywords:
- origins of Transforms [WPF]
- Transforms [WPF], origins of
- graphics [WPF], origins of Transforms
ms.assetid: f4dbc29d-93c7-41cd-96d8-5cfd8624b470
ms.openlocfilehash: 48b3b0df8dab8516873495a996074eae57ffe00f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975467"
---
# <a name="how-to-specify-the-origin-of-a-transform-by-using-relative-values"></a>Gewusst wie: Angeben des Ursprungs einer Transformation mithilfe von relativen Werten
In diesem Beispiel wird gezeigt, wie relative Werte verwendet werden, um den Ursprung eines-Werts anzugeben <xref:System.Windows.UIElement.RenderTransform%2A> , der auf ein angewendet wird <xref:System.Windows.FrameworkElement> .  
  
 Wenn Sie ein mithilfe der-Eigenschaft drehen, skalieren oder neigen <xref:System.Windows.FrameworkElement> <xref:System.Windows.UIElement.RenderTransform%2A> , wird die Transformation von der Standardeinstellung auf die linke obere Ecke des Elements angewendet. Wenn Sie von der Mitte des Elements aus drehen, skalieren oder neigen möchten, können Sie dies ändern, indem Sie für den Mittelpunkt der Transformation den Mittelpunkt des Elements festlegen. Für diese Lösung müssen Sie jedoch die Größe des Elements kennen. Eine einfachere Möglichkeit, eine Transformation auf den Mittelpunkt eines Elements anzuwenden, besteht darin, die zugehörige- <xref:System.Windows.UIElement.RenderTransformOrigin%2A> Eigenschaft auf (0,5, 0,5) festzulegen, anstatt einen Mittelwert für die Transformation selbst festzulegen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.RotateTransform> , um <xref:System.Windows.Controls.Button> 45 Grad im Uhrzeigersinn zu drehen. Da in dem Beispiel kein Mittelpunkt angegeben ist, dreht sich die Schaltfläche um den Punkt (0, 0), die obere linke Ecke. Der <xref:System.Windows.Media.RotateTransform> wird auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft angewendet.  
  
 In der folgenden Abbildung wird das Transformationsergebnis für das folgende Beispiel angezeigt.  
  
 ![Eine mit RenderTransform transformierte Schaltfläche](./media/graphicsmm-rendertransformwithdefaultcenter.png "graphicsmm_RenderTransformWithDefaultCenter")  
Eine Drehung um 45 Grad im Uhrzeigersinn unter Verwendung der RenderTransform-Eigenschaft  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample1)]  
  
 Im folgenden Beispiel wird auch ein-Wert verwendet <xref:System.Windows.Media.RotateTransform> , um <xref:System.Windows.Controls.Button> 45 Grad im Uhrzeigersinn zu drehen. in diesem Beispiel wird jedoch der <xref:System.Windows.UIElement.RenderTransformOrigin%2A> der Schaltfläche auf (0,5, 0,5) festgelegt. Dadurch erfolgt die Drehung um den Mittelpunkt der Schaltfläche, nicht um die obere linke Ecke.  
  
 In der folgenden Abbildung wird das Transformationsergebnis für das folgende Beispiel angezeigt.  
  
 ![Eine um ihren Mittelpunkt transformierte Schaltfläche](./media/graphicsmm-rendertransformrelativecenter.png "graphicsmm_RenderTransformRelativeCenter")  
Eine Drehung um 45 Grad unter Verwendung der RenderTransform-Eigenschaft mit einem RenderTransformOrigin von (0.5, 0.5)  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample2)]  
  
 Weitere Informationen zum Transformieren von <xref:System.Windows.FrameworkElement> Objekten finden Sie in der [Übersicht über Transformationen](transforms-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Transform>
- [Übersicht über Transformationen](transforms-overview.md)
- [Artikel zu Vorgehensweisen](transformations-how-to-topics.md)
