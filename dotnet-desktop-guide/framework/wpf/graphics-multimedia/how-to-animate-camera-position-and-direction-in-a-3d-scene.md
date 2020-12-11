---
title: 'Gewusst wie: Animieren der Kameraposition und -richtung in 3D-Szenen'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], camera position in 3D scenes
- camera direction [WPF], animating in 3D scenes
- 3D scenes [WPF], animating camera position
- 3D scenes [WPF], animating camera direction
- camera position [WPF], animating in 3D scenes
- animation [WPF], camera direction in 3D scenes
ms.assetid: 480224b7-a5e5-4165-ba7f-ef760ddff94a
ms.openlocfilehash: 5ce94e154cd5aa29b59260f893ec2b63a08db0fc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977273"
---
# <a name="how-to-animate-camera-position-and-direction-in-a-3d-scene"></a>Gewusst wie: Animieren der Kameraposition und -richtung in 3D-Szenen
Im folgenden Beispiel wird gezeigt, wie Sie die Position einer Kamera animieren und die Richtung animieren, in der Sie auf eine 3D-Szene zeigt. Dies erfolgt mithilfe von <xref:System.Windows.Media.Animation.Point3DAnimation> und <xref:System.Windows.Media.Animation.Vector3DAnimation> , um die-Eigenschaft und die-Eigenschaft des zu animieren <xref:System.Windows.Media.Media3D.ProjectionCamera.Position%2A> <xref:System.Windows.Media.Media3D.ProjectionCamera.LookDirection%2A> <xref:System.Windows.Media.Media3D.PerspectiveCamera> . Sie können eine Animation wie diese verwenden, um die Ansicht einer Szene von Onlooker als Reaktion auf ein Ereignis zu ändern.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationExample.xaml#pointvector3danimationexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.Vector3DAnimation>
- <xref:System.Windows.Media.Animation.Point3DAnimation>
- [Animieren von Kameraposition und –richtung mithilfe von Keyframes](how-to-animate-camera-position-and-direction-using-key-frames.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
