---
title: 'Gewusst wie: Animieren einer Matrix mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], Matrix properties with key frames
- Matrix properties [WPF], animating with key frames
- key frames [WPF], animating Matrix properties with
ms.assetid: b851a4c7-ecb1-420e-9203-83e7afd037fd
ms.openlocfilehash: eb596cf728f8a7cc1964963b8509f42bdd7a392a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977314"
---
# <a name="how-to-animate-a-matrix-by-using-key-frames"></a>Gewusst wie: Animieren einer Matrix mithilfe von Keyframes
In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.MatrixTransform.Matrix%2A> Eigenschaft eines <xref:System.Windows.Media.MatrixTransform> mithilfe von Keyframes animiert wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.MatrixTransform.Matrix%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.MatrixTransform> . Im Beispiel wird das <xref:System.Windows.Media.MatrixTransform> -Objekt verwendet, um die Darstellung und Position eines zu transformieren <xref:System.Windows.Controls.Button> .  
  
 Diese Animation verwendet die <xref:System.Windows.Media.Animation.DiscreteMatrixKeyFrame> -Klasse, um zwei Keyframes zu erstellen und mit Ihnen die folgenden Aktionen durchführen zu können:  
  
1. Animiert den ersten <xref:System.Windows.Media.Matrix> während der ersten 0,2 Sekunden. Im Beispiel werden die <xref:System.Windows.Media.Matrix.M11%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.Matrix.M12%2A> der geändert <xref:System.Windows.Media.Matrix> . Diese Änderung bewirkt, dass die Schaltfläche gestreckt wird und verzerrt wird. Das Beispiel ändert auch die <xref:System.Windows.Media.Matrix.OffsetX%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.Matrix.OffsetY%2A> , sodass die Schaltfläche die Position ändert.  
  
2. Animiert den zweiten <xref:System.Windows.Media.Matrix> um 1,0 Sekunden. Die Schaltfläche wird an eine andere Position verschoben, während die Schaltfläche nicht mehr verzerrt oder gestreckt wird.  
  
3. Wiederholt die Animation unbegrenzt.  
  
> [!NOTE]
> Keyframes, die vom- <xref:System.Windows.Media.Animation.DiscreteMatrixKeyFrame> Objekt abgeleitet werden, erzeugen plötzliche Sprünge zwischen Werten, d. h., dass die Bewegung der Animation ruckartig ist.  
  
 [!code-xaml[keyframes_snip#MatrixAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/MatrixAnimationUsingKeyFramesExample.xaml#matrixanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.MatrixTransform.Matrix%2A>
- <xref:System.Windows.Media.MatrixTransform>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
