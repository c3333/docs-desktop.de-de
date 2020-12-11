---
title: 'Gewusst wie: Animieren eines Objekts auf einem Pfad (MatrixAnimation)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (matrix animation)
- matrix animation [WPF]
ms.assetid: 7000e697-1414-468c-b915-cf66062fc49e
ms.openlocfilehash: 7dfc233fe60e1cea293edc44a2bba79dc6962f7c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977276"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation"></a>Gewusst wie: Animieren eines Objekts auf einem Pfad (MatrixAnimation)
In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> Klasse verwendet wird, um ein Objekt entlang eines durch einen definierten Pfades zu animieren <xref:System.Windows.Media.PathGeometry> .  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird Folgendes ausgeführt, um ein Objekt entlang eines Pfads zu animieren:  
  
- Wendet ein <xref:System.Windows.Media.MatrixTransform> auf das-Objekt an, um es zu verschieben.  
  
- Definiert den Pfad mithilfe eines <xref:System.Windows.Media.PathGeometry> .  
  
- Erstellt eine <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> und verwendet diese, um die- <xref:System.Windows.Media.Matrix> Eigenschaft des zu animieren <xref:System.Windows.Media.MatrixTransform> . Der <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> <xref:System.Windows.Media.PathGeometry> verwendet, und verwendet ihn, um <xref:System.Windows.Media.Matrix> Werte zu generieren.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexample.xaml#matrixanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExample.cs#matrixanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExample.vb#matrixanimationusingpathwholepage)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations). Weitere Informationen zu geometrischen Pfaden finden Sie in der [Übersicht](geometry-overview.md)über die Geometrie.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Beispiel einer Pfadanimation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations)
- [Gewusst-wie-Themen zur Pfadanimation](path-animation-how-to-topics.md)
