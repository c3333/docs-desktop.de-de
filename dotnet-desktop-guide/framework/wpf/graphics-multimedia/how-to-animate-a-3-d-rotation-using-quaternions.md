---
title: 'Gewusst wie: Animieren einer 3D-Drehung mit Quaternionen'
ms.date: 03/30/2017
helpviewer_keywords:
- quaternions [WPF]
- animation [WPF], 3D translations [WPF], with quaternions
- 3D translations [WPF], animating [WPF], with quaternions
ms.assetid: adca9cb1-066b-4de8-abbb-6b4007579ee7
ms.openlocfilehash: 0d229b0a714cc53459943fae751ab4d4f787d7d8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977321"
---
# <a name="how-to-animate-a-3d-rotation-using-quaternions"></a>Gewusst wie: Animieren einer 3D-Drehung mit Quaternionen
Dieses Beispiel zeigt, wie Sie eine Drehung eines 3D-Objekts mit Quaternionen animieren.  
  
 Der folgende Code zeigt einen, der <xref:System.Windows.Media.Media3D.QuaternionRotation3D> als Wert für die- <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> Eigenschaft eines verwendet wird <xref:System.Windows.Media.Media3D.RotateTransform3D> .  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline1)]  
  
 Dies <xref:System.Windows.Media.Media3D.QuaternionRotation3D> wird mit einem <xref:System.Windows.Media.Animation.QuaternionAnimation> in einem animiert, <xref:System.Windows.Media.Animation.Storyboard> das den folgenden Code verwendet.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline2)]  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt das gesamte Beispiel.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Erstellen einer 3D-Szene](how-to-create-a-3-d-scene.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
- [Übersicht über Transformationen](transforms-overview.md)
- [Animieren einer 3D-Drehung mit Storyboards](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [Animieren einer 3D-Drehung mit Rotation3DAnimation](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
