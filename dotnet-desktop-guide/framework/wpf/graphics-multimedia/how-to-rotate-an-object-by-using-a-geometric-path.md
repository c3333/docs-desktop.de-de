---
title: 'Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
ms.assetid: cb31ca4d-f05a-4c6b-9a18-4b6faaf38d45
ms.openlocfilehash: a351fdc936f634b7c57ba5a49e51501f7572a3c9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978015"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path"></a>Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads
Dieses Beispiel zeigt, wie Sie ein Objekt entlang eines geometrischen Pfads drehen, der durch ein-Objekt definiert wird <xref:System.Windows.Media.PathGeometry> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden drei- <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> Objekte verwendet, um ein Rechteck entlang eines geometrischen Pfads zu verschieben.  
  
- Der erste <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animiert eine <xref:System.Windows.Media.RotateTransform> , die auf das Rechteck angewendet wird. Die Animation generiert Winkelwerte. Das Rechteck dreht (schwenkt) sich entlang der Pfadkonturen.  
  
- Die anderen beiden-Objekte animieren den <xref:System.Windows.Media.TranslateTransform.X%2A> -Wert und den- <xref:System.Windows.Media.TranslateTransform.Y%2A> Wert eines-Objekts <xref:System.Windows.Media.TranslateTransform> , das auf das Rechteck angewendet wird. Sie verschieben das Rechteck horizontal und vertikal entlang des Pfads.  
  
 [!code-xaml[PathAnimationGallery_snippet#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/rotateanimationusingpathexample.xaml#rotateanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/RotateAnimationUsingPathExample.cs#rotateanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/RotateAnimationUsingPathExample.vb#rotateanimationusingpathwholepage)]  
  
 Eine andere Möglichkeit zum Drehen eines Objekts mithilfe eines geometrischen Pfads besteht darin, ein <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> -Objekt zu verwenden und seine- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> Eigenschaft auf festzulegen `true` . Weitere Informationen und ein Beispiel finden Sie unter [Drehen eines Objekts mithilfe eines geometrischen Pfads (Matrix Animation)](how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).  
  
 Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Beispiel einer Pfadanimation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations)
- [Gewusst-wie-Themen zur Pfadanimation](path-animation-how-to-topics.md)
