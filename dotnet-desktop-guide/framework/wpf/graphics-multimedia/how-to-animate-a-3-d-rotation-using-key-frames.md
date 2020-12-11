---
title: 'Gewusst wie: Animieren einer 3D-Drehung mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], 3D translations [WPF], with key frames (Rotation3DAnimation)
- key frames [WPF], Rotation3DAnimation
- 3D translations [WPF], animating [WPF], with key frames (Rotation3DAnimation)
ms.assetid: 6f671b95-7f30-4836-9a4f-aeb7dc30121f
ms.openlocfilehash: 2b9059df079125c34c70237c0f600751020044c6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976189"
---
# <a name="how-to-animate-a-3d-rotation-using-key-frames"></a>Gewusst wie: Animieren einer 3D-Drehung mithilfe von Keyframes
Im folgenden Beispiel <xref:System.Windows.Media.Animation.Rotation3DAnimationUsingKeyFrames> wird verwendet, um ein 3D-Objekt zu drehen, während seine Achse der Drehung animiert, was zu einem "wackeln" führt. Diese Animation verwendet die folgenden Keyframes:  
  
1. <xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> wird verwendet, um eine glatte, lineare interpolung zwischen-Werten zu erstellen.  
  
2. <xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> wird verwendet, um plötzliche "Sprünge" zwischen Werten zu erstellen (keine interpolung).  
  
3. <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> wird verwendet, um einen variablen Übergang zwischen Werten in Abhängigkeit von der-Eigenschaft zu erstellen <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> . Im folgenden Beispiel beginnt dieser Teil der Animation langsam, aber bis zum Ende des Zeit Segments beschleunigt die Geschwindigkeit exponentiell.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[Animation3DGallery_snip#Rotation3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotation3DAnimationUsingKeyFramesExample.xaml#rotation3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Animieren einer 3D-Drehung mit Storyboards](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [Animieren einer 3D-Drehung mit Rotation3DAnimation](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [Animieren einer 3D-Drehung mit Quaternionen](how-to-animate-a-3-d-rotation-using-quaternions.md)
- [Animieren einer 3D-Drehung mit Keyframes (QuaternionAnimationUsingKeyFrames)](animate-a-3-d-rotation-quaternionanimationusingkeyframes.md)
