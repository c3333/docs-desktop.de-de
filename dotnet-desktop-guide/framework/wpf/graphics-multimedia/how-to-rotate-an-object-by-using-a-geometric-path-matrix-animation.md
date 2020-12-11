---
title: 'Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads (MatrixAnimation)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
- matrix animation [WPF]
ms.assetid: 877dc9aa-6bdc-4beb-8772-3efaec32c0f0
ms.openlocfilehash: 63dc873a2b840ea3f870a8c60c5691ab271c1c9f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974860"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation"></a>Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads (MatrixAnimation)
In diesem Beispiel wird gezeigt, wie ein <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> -Objekt und ein- <xref:System.Windows.Media.MatrixTransform> Objekt verwendet werden, um ein Objekt entlang eines durch ein-Objekt definierten geometrischen Pfads zu drehen <xref:System.Windows.Media.PathGeometry> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird das- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> Objekt verwendet, um die- <xref:System.Windows.Media.MatrixTransform.Matrix%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.MatrixTransform> . Das <xref:System.Windows.Media.MatrixTransform> wird auf eine Schaltfläche angewendet und bewirkt, dass es sich entlang eines gekrümmten Pfads bewegt. Da die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> Eigenschaft auf festgelegt ist `true` , dreht sich das Rechteck entlang der Tangente des Pfads.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathdoesrotatewithtangentexample.xaml#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathDoesRotateWithTangentExample.cs#matrixanimationusingpathdoesrotatewithtangentwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathDoesRotateWithTangentExample.vb#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).  
  
 In der Code Version des vorangehenden Beispiels <xref:System.Windows.Media.Animation.Storyboard> wurde verwendet, um den zu animieren <xref:System.Windows.Media.EllipseGeometry> , auch wenn nur eine Animation angewendet wurde. Eine einfachere Möglichkeit, eine einzelne Animation auf eine Eigenschaft im Code anzuwenden, ist die Verwendung der- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> Methode. Ein Beispiel finden Sie unter [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Gewusst-wie-Themen zur Pfadanimation](path-animation-how-to-topics.md)
- [Beispiel einer Pfadanimation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations)
