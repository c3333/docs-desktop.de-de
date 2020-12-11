---
title: 'Gewusst wie: Animieren eines Objekts entlang eines Pfads (PointAnimation)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (point animation)
- point animation [WPF]
ms.assetid: 1fa3f817-35bc-41a1-b366-f5a20b70da0c
ms.openlocfilehash: eff0c24a9369ffaa0cfca1cc46af4eff39f58a38
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977275"
---
# <a name="how-to-animate-an-object-along-a-path-point-animation"></a>Gewusst wie: Animieren eines Objekts entlang eines Pfads (PointAnimation)
Dieses Beispiel zeigt, wie ein- <xref:System.Windows.Media.Animation.PointAnimationUsingPath> Objekt verwendet wird, um einen <xref:System.Windows.Point> entlang eines gekrümmten Pfads zu animieren.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.EllipseGeometry> entlang eines durch einen definierten Pfades verschoben <xref:System.Windows.Media.PathGeometry> . Die-Eigenschaft der Ellipse <xref:System.Windows.Media.EllipseGeometry.Center%2A> , die einen <xref:System.Windows.Point> Wert annimmt, gibt ihre Position an. zum Verschieben der Ellipse-Geometrie animieren Sie Ihre- <xref:System.Windows.Media.EllipseGeometry.Center%2A> Eigenschaft. Im Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.PointAnimationUsingPath> , um die <xref:System.Windows.Media.EllipseGeometry> -Eigenschaft des-Objekts zu animieren <xref:System.Windows.Media.EllipseGeometry.Center%2A> .  
  
 [!code-xaml[PathAnimationGallery_snippet#PointAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/pointanimationusingpathexample.xaml#pointanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#PointAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/PointAnimationUsingPathExample.cs#pointanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#PointAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/PointAnimationUsingPathExample.vb#pointanimationusingpathwholepage)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).  
  
 In der Code Version des vorangehenden Beispiels <xref:System.Windows.Media.Animation.Storyboard> wurde verwendet, um den zu animieren <xref:System.Windows.Media.EllipseGeometry> , auch wenn nur eine Animation angewendet wurde. Eine <xref:System.Windows.Media.Animation.Storyboard> ist oft die einfachste Möglichkeit, mehrere Animationen anzuwenden, da diese Animationen durch denselben gesteuert werden können <xref:System.Windows.Media.Animation.Storyboard> . Eine einfachere Möglichkeit, eine einzelne Animation auf eine Eigenschaft anzuwenden, wenn Sie Code verwenden, ist jedoch die Verwendung der- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> Methode. Ein Beispiel finden Sie unter [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Siehe auch

- [Beispiel einer Pfadanimation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations)
- [Übersicht über Animationen](animation-overview.md)
- [Gewusst-wie-Themen zur Pfadanimation](path-animation-how-to-topics.md)
