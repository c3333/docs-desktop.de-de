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
# <a name="how-to-animate-camera-position-and-direction-using-key-frames"></a><span data-ttu-id="f7dc4-102">Gewusst wie: Animieren von Kameraposition und -richtung mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="f7dc4-102">How to: Animate Camera Position and Direction Using Key Frames</span></span>
<span data-ttu-id="f7dc4-103">Im folgenden Beispiel <xref:System.Windows.Media.Animation.Point3DAnimationUsingKeyFrames> wird verwendet, um die Position eines <xref:System.Windows.Media.Media3D.PerspectiveCamera> in einer 3D-Szene zu animieren.</span><span class="sxs-lookup"><span data-stu-id="f7dc4-103">In the following example, <xref:System.Windows.Media.Animation.Point3DAnimationUsingKeyFrames> is used to animate the position of a <xref:System.Windows.Media.Media3D.PerspectiveCamera> in a 3D scene.</span></span> <span data-ttu-id="f7dc4-104">Außerdem <xref:System.Windows.Media.Animation.Vector3DAnimationUsingKeyFrames> wird verwendet, um die Richtung zu animieren, die die Kamera in der 3D-Szene zeigt.</span><span class="sxs-lookup"><span data-stu-id="f7dc4-104">In addition, <xref:System.Windows.Media.Animation.Vector3DAnimationUsingKeyFrames> is used to animate the direction the camera is pointing in the 3D scene.</span></span> <span data-ttu-id="f7dc4-105">Beide Animationen verwenden mehrere Keyframes, die eine Reihe von Animationseffekten erzeugen:</span><span class="sxs-lookup"><span data-stu-id="f7dc4-105">Both of these animations use several key frames which create a series of animation effects:</span></span>  
  
1. <span data-ttu-id="f7dc4-106"><xref:System.Windows.Media.Animation.LinearPoint3DKeyFrame> und <xref:System.Windows.Media.Animation.LinearVector3DKeyFrame> werden verwendet, um eine glatte, lineare Interpolations zwischen Werten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7dc4-106"><xref:System.Windows.Media.Animation.LinearPoint3DKeyFrame> and <xref:System.Windows.Media.Animation.LinearVector3DKeyFrame> are used to create a smooth, linear interpolation between values.</span></span>  
  
2. <span data-ttu-id="f7dc4-107"><xref:System.Windows.Media.Animation.DiscretePoint3DKeyFrame> und <xref:System.Windows.Media.Animation.DiscreteVector3DKeyFrame> werden verwendet, um plötzliche "Sprünge" zwischen Werten zu erstellen (keine interpolung).</span><span class="sxs-lookup"><span data-stu-id="f7dc4-107"><xref:System.Windows.Media.Animation.DiscretePoint3DKeyFrame> and <xref:System.Windows.Media.Animation.DiscreteVector3DKeyFrame> are used to create sudden "jumps" between values (no interpolation).</span></span>  
  
3. <span data-ttu-id="f7dc4-108"><xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame> und <xref:System.Windows.Media.Animation.SplineVector3DKeyFrame> werden verwendet, um einen variablen Übergang zwischen Werten in Abhängigkeit von der-Eigenschaft zu erstellen <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame.KeySpline%2A> .</span><span class="sxs-lookup"><span data-stu-id="f7dc4-108"><xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame> and <xref:System.Windows.Media.Animation.SplineVector3DKeyFrame> are used to create a variable transition between values depending on the <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="f7dc4-109">Im folgenden Beispiel beginnt die Animation langsam, aber bis zum Ende des Zeit Segments beschleunigt die Geschwindigkeit exponentiell.</span><span class="sxs-lookup"><span data-stu-id="f7dc4-109">In the example below, the animation starts off slow but toward the end of the time segment, speeds up exponentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7dc4-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7dc4-110">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationUsingKeyFramesExample.xaml#pointvector3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="f7dc4-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7dc4-111">See also</span></span>

- [<span data-ttu-id="f7dc4-112">Animieren der Kameraposition und –richtung in 3D-Szenen</span><span class="sxs-lookup"><span data-stu-id="f7dc4-112">Animate Camera Position and Direction in a 3D Scene</span></span>](how-to-animate-camera-position-and-direction-in-a-3d-scene.md)
- [<span data-ttu-id="f7dc4-113">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="f7dc4-113">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
