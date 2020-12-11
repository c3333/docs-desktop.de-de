---
title: 'Gewusst wie: Animieren einer 3D-Drehung mit Storyboards'
ms.date: 03/30/2017
helpviewer_keywords:
- Storyboards [WPF]
- 3D translations [WPF], animating [WPF], with Storyboards
- animation [WPF], 3D translations [WPF], with Storyboards
ms.assetid: 1020e44e-e21e-49a8-be53-53cbc1910e83
ms.openlocfilehash: 088f1a33cfc73a706ffed55ffff6494adaf8fca4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977317"
---
# <a name="how-to-animate-a-3d-rotation-using-storyboards"></a>Gewusst wie: Animieren einer 3D-Drehung mit Storyboards
Im folgenden Beispiel wird gezeigt, wie ein 3D-Objekt gedreht wird, während es durch Animieren der-Eigenschaft <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> und <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> der-Eigenschaft eines Objekts gedreht wird <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> . Dieses <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> Objekt gibt die Drehung der Drehung des 3D-Objekts an, sodass das Animieren seiner Eigenschaften den gewünschten Rotations Effekt erzeugt. Innerhalb des Storyboards <xref:System.Windows.Media.Animation.DoubleAnimation> wird zum Animieren der Eigenschaft verwendet, <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> während zum <xref:System.Windows.Media.Animation.Vector3DAnimation> Animieren der Eigenschaft verwendet wird <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> .  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[Animation3DGallery_snip#Rotate3DUsingAxisAngleRotation3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotat3DUsingAxisAngleRotation3DExample.xaml#rotate3dusingaxisanglerotation3dexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Animieren einer 3D-Drehung mit Rotation3DAnimation](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [Animieren einer 3D-Drehung mithilfe von Keyframes (Rotation3DAnimationUsingKeyFrames)](how-to-animate-a-3-d-rotation-using-key-frames.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
- [Übersicht über Storyboards](storyboards-overview.md)
