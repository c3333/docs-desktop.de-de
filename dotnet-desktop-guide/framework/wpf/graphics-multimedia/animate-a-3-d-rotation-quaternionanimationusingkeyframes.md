---
title: 'Gewusst wie: Animieren einer 3D-Drehung mithilfe von Keyframes (QuaternionAnimationUsingKeyFrames)'
ms.date: 03/30/2017
helpviewer_keywords:
- 3D translations [WPF], animating [WPF], with key frames (QuaternionAnimationUsingKeyFrames)
- key frames [WPF], QuaternionAnimationUsingKeyFrames
- animation [WPF], 3D translations [WPF], with key frames (QuaternionAnimationUsingKeyFrames)
ms.assetid: 09e5707b-7523-4a08-9aa7-bb13cbedccdf
ms.openlocfilehash: 5273183aaa49a743cc401dec0b4b16bae09e3129
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977643"
---
# <a name="how-to-animate-a-3d-rotation-using-key-frames-quaternionanimationusingkeyframes"></a><span data-ttu-id="8bd39-102">Gewusst wie: Animieren einer 3D-Drehung mithilfe von Keyframes (QuaternionAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="8bd39-102">How to: Animate a 3D Rotation Using Key Frames (QuaternionAnimationUsingKeyFrames)</span></span>
<span data-ttu-id="8bd39-103">Im folgenden Beispiel <xref:System.Windows.Media.Animation.QuaternionAnimationUsingKeyFrames> wird verwendet, um ein 3D-Objekt zu drehen.</span><span class="sxs-lookup"><span data-stu-id="8bd39-103">In the following example, <xref:System.Windows.Media.Animation.QuaternionAnimationUsingKeyFrames> is used to make a 3D object rotate.</span></span> <span data-ttu-id="8bd39-104">Diese Animation verwendet die folgenden Keyframes:</span><span class="sxs-lookup"><span data-stu-id="8bd39-104">This animation uses the following key frames:</span></span>  
  
1. <span data-ttu-id="8bd39-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> wird verwendet, um eine glatte, lineare interpolung zwischen-Werten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8bd39-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> is used to create a smooth, linear interpolation between values.</span></span>  
  
2. <span data-ttu-id="8bd39-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> wird verwendet, um plötzliche "Sprünge" zwischen Werten zu erstellen (keine interpolung).</span><span class="sxs-lookup"><span data-stu-id="8bd39-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> is used to create sudden "jumps" between values (no interpolation).</span></span>  
  
3. <span data-ttu-id="8bd39-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> wird verwendet, um einen variablen Übergang zwischen Werten in Abhängigkeit von der-Eigenschaft zu erstellen <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> .</span><span class="sxs-lookup"><span data-stu-id="8bd39-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> is used to create a variable transition between values depending on the <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="8bd39-108">Im folgenden Beispiel beginnt dieser Teil der Animation langsam, aber bis zum Ende des Zeit Segments beschleunigt die Geschwindigkeit exponentiell.</span><span class="sxs-lookup"><span data-stu-id="8bd39-108">In the example below, this part of the animation starts off slow but toward the end of the time segment, speeds up exponentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8bd39-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8bd39-109">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationUsingKeyFramesExample.xaml#quaternionanimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="8bd39-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bd39-110">See also</span></span>

- [<span data-ttu-id="8bd39-111">Animieren einer 3D-Drehung mit Storyboards</span><span class="sxs-lookup"><span data-stu-id="8bd39-111">Animate a 3D Rotation Using Storyboards</span></span>](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [<span data-ttu-id="8bd39-112">Animieren einer 3D-Drehung mit Rotation3DAnimation</span><span class="sxs-lookup"><span data-stu-id="8bd39-112">Animate a 3D Rotation Using Rotation3DAnimation</span></span>](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [<span data-ttu-id="8bd39-113">Animieren einer 3D-Drehung mit Quaternionen</span><span class="sxs-lookup"><span data-stu-id="8bd39-113">Animate a 3D Rotation Using Quaternions</span></span>](how-to-animate-a-3-d-rotation-using-quaternions.md)
- [<span data-ttu-id="8bd39-114">Animieren einer 3D-Drehung mithilfe von Keyframes (Rotation3DAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="8bd39-114">Animate a 3D Rotation Using Key Frames (Rotation3DAnimationUsingKeyFrames)</span></span>](how-to-animate-a-3-d-rotation-using-key-frames.md)
- [<span data-ttu-id="8bd39-115">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="8bd39-115">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="8bd39-116">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="8bd39-116">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
