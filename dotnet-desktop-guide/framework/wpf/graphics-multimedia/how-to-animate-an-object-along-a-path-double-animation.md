---
title: 'Gewusst wie: Verschieben eines Objekts auf einem Pfad (DoubleAnimation)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (double animation)
- double animation [WPF]
ms.assetid: 5a3c4a99-f303-42ad-a52a-e4794bb1798e
ms.openlocfilehash: 084caac26fd68b6914ec3858652ec44557a0dbd7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977278"
---
# <a name="how-to-animate-an-object-along-a-path-double-animation"></a>Gewusst wie: Verschieben eines Objekts auf einem Pfad (DoubleAnimation)
In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> Klasse verwendet wird, um ein Objekt entlang eines durch einen definierten Pfades zu verschieben <xref:System.Windows.Media.PathGeometry> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden zwei- <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> Objekte verwendet, um ein Rechteck entlang eines geometrischen Pfads zu verschieben:  
  
- Der erste <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animiert die <xref:System.Windows.Media.TranslateTransform.X%2A> des, das <xref:System.Windows.Media.TranslateTransform> auf das Rechteck angewendet wird. Das Rechteck wird hierdurch horizontal am Pfad entlang verschoben.  
  
- Die zweite <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animiert die <xref:System.Windows.Media.TranslateTransform.Y%2A> der <xref:System.Windows.Media.TranslateTransform> auf das Rechteck angewendeten. Das Rechteck wird hierdurch vertikal am Pfad entlang verschoben.  
  
 [!code-xaml[PathAnimationGallery_snippet#DoubleAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/doubleanimationusingpathexample.xaml#doubleanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/DoubleAnimationUsingPathExample.cs#doubleanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/DoubleAnimationUsingPathExample.vb#doubleanimationusingpathwholepage)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).  
  
 Eine andere Möglichkeit zum Verschieben eines Objekts mithilfe eines geometrischen Pfads ist die Verwendung eines- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> Objekts. Ein Beispiel finden Sie unter [Animieren eines Objekts entlang eines Pfads (Matrix Animation)](how-to-animate-an-object-along-a-path-matrix-animation.md).  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Gewusst-wie-Themen zur Pfadanimation](path-animation-how-to-topics.md)
