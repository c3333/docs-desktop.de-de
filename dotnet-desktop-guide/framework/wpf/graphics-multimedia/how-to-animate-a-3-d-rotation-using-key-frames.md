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
# <a name="how-to-animate-a-3d-rotation-using-key-frames"></a><span data-ttu-id="792b1-102">Gewusst wie: Animieren einer 3D-Drehung mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="792b1-102">How to: Animate a 3D Rotation Using Key Frames</span></span>
<span data-ttu-id="792b1-103">Im folgenden Beispiel <xref:System.Windows.Media.Animation.Rotation3DAnimationUsingKeyFrames> wird verwendet, um ein 3D-Objekt zu drehen, während seine Achse der Drehung animiert, was zu einem "wackeln" führt.</span><span class="sxs-lookup"><span data-stu-id="792b1-103">In the following example, <xref:System.Windows.Media.Animation.Rotation3DAnimationUsingKeyFrames> is used to make a 3D object rotate while its axis of rotation animates resulting in a "wobble".</span></span> <span data-ttu-id="792b1-104">Diese Animation verwendet die folgenden Keyframes:</span><span class="sxs-lookup"><span data-stu-id="792b1-104">This animation uses the following key frames:</span></span>  
  
1. <span data-ttu-id="792b1-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> wird verwendet, um eine glatte, lineare interpolung zwischen-Werten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="792b1-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> is used to create a smooth, linear interpolation between values.</span></span>  
  
2. <span data-ttu-id="792b1-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> wird verwendet, um plötzliche "Sprünge" zwischen Werten zu erstellen (keine interpolung).</span><span class="sxs-lookup"><span data-stu-id="792b1-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> is used to create sudden "jumps" between values (no interpolation).</span></span>  
  
3. <span data-ttu-id="792b1-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> wird verwendet, um einen variablen Übergang zwischen Werten in Abhängigkeit von der-Eigenschaft zu erstellen <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> .</span><span class="sxs-lookup"><span data-stu-id="792b1-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> is used to create a variable transition between values depending on the <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="792b1-108">Im folgenden Beispiel beginnt dieser Teil der Animation langsam, aber bis zum Ende des Zeit Segments beschleunigt die Geschwindigkeit exponentiell.</span><span class="sxs-lookup"><span data-stu-id="792b1-108">In the example below, this part of the animation starts off slow but toward the end of the time segment, speeds up exponentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="792b1-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="792b1-109">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#Rotation3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotation3DAnimationUsingKeyFramesExample.xaml#rotation3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="792b1-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="792b1-110">See also</span></span>

- [<span data-ttu-id="792b1-111">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="792b1-111">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="792b1-112">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="792b1-112">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="792b1-113">Animieren einer 3D-Drehung mit Storyboards</span><span class="sxs-lookup"><span data-stu-id="792b1-113">Animate a 3D Rotation Using Storyboards</span></span>](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [<span data-ttu-id="792b1-114">Animieren einer 3D-Drehung mit Rotation3DAnimation</span><span class="sxs-lookup"><span data-stu-id="792b1-114">Animate a 3D Rotation Using Rotation3DAnimation</span></span>](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [<span data-ttu-id="792b1-115">Animieren einer 3D-Drehung mit Quaternionen</span><span class="sxs-lookup"><span data-stu-id="792b1-115">Animate a 3D Rotation Using Quaternions</span></span>](how-to-animate-a-3-d-rotation-using-quaternions.md)
- [<span data-ttu-id="792b1-116">Animieren einer 3D-Drehung mit Keyframes (QuaternionAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="792b1-116">Animate a 3D Rotation Using Key Frames (QuaternionAnimationUsingKeyFrames)</span></span>](animate-a-3-d-rotation-quaternionanimationusingkeyframes.md)
