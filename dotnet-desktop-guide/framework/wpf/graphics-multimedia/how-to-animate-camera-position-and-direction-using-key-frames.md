---
title: 'Gewusst wie: Animieren von Kameraposition und -richtung mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], camera direction with key frames
- key frames [WPF], animating camera direction
- animation [WPF], camera position with key frames
- camera position [WPF], animating with key frames
- key frames [WPF], animating camera position
- camera direction [WPF], animating with key frames
ms.assetid: 5753024e-0057-454d-947f-43ea686879c7
ms.openlocfilehash: 28471f9b42140a6c75b043d33939503528b63194
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977767"
---
# <a name="how-to-animate-camera-position-and-direction-using-key-frames"></a>Gewusst wie: Animieren von Kameraposition und -richtung mithilfe von Keyframes
Im folgenden Beispiel <xref:System.Windows.Media.Animation.Point3DAnimationUsingKeyFrames> wird verwendet, um die Position eines <xref:System.Windows.Media.Media3D.PerspectiveCamera> in einer 3D-Szene zu animieren. Außerdem <xref:System.Windows.Media.Animation.Vector3DAnimationUsingKeyFrames> wird verwendet, um die Richtung zu animieren, die die Kamera in der 3D-Szene zeigt. Beide Animationen verwenden mehrere Keyframes, die eine Reihe von Animationseffekten erzeugen:  
  
1. <xref:System.Windows.Media.Animation.LinearPoint3DKeyFrame> und <xref:System.Windows.Media.Animation.LinearVector3DKeyFrame> werden verwendet, um eine glatte, lineare Interpolations zwischen Werten zu erstellen.  
  
2. <xref:System.Windows.Media.Animation.DiscretePoint3DKeyFrame> und <xref:System.Windows.Media.Animation.DiscreteVector3DKeyFrame> werden verwendet, um plötzliche "Sprünge" zwischen Werten zu erstellen (keine interpolung).  
  
3. <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame> und <xref:System.Windows.Media.Animation.SplineVector3DKeyFrame> werden verwendet, um einen variablen Übergang zwischen Werten in Abhängigkeit von der-Eigenschaft zu erstellen <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame.KeySpline%2A> . Im folgenden Beispiel beginnt die Animation langsam, aber bis zum Ende des Zeit Segments beschleunigt die Geschwindigkeit exponentiell.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationUsingKeyFramesExample.xaml#pointvector3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Animieren der Kameraposition und –richtung in 3D-Szenen](how-to-animate-camera-position-and-direction-in-a-3d-scene.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
