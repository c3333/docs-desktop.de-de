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
# <a name="how-to-animate-a-3d-rotation-using-storyboards"></a><span data-ttu-id="b3244-102">Gewusst wie: Animieren einer 3D-Drehung mit Storyboards</span><span class="sxs-lookup"><span data-stu-id="b3244-102">How to: Animate a 3D Rotation Using Storyboards</span></span>
<span data-ttu-id="b3244-103">Im folgenden Beispiel wird gezeigt, wie ein 3D-Objekt gedreht wird, während es durch Animieren der-Eigenschaft <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> und <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> der-Eigenschaft eines Objekts gedreht wird <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> .</span><span class="sxs-lookup"><span data-stu-id="b3244-103">The following example shows how to make a 3D object rotate while it "wobbles" by animating the <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> and <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> properties of an <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> object.</span></span> <span data-ttu-id="b3244-104">Dieses <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> Objekt gibt die Drehung der Drehung des 3D-Objekts an, sodass das Animieren seiner Eigenschaften den gewünschten Rotations Effekt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b3244-104">This <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> object specifies the rotation transform of the 3D object and so animating its properties creates the desire rotation effect.</span></span> <span data-ttu-id="b3244-105">Innerhalb des Storyboards <xref:System.Windows.Media.Animation.DoubleAnimation> wird zum Animieren der Eigenschaft verwendet, <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> während zum <xref:System.Windows.Media.Animation.Vector3DAnimation> Animieren der Eigenschaft verwendet wird <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> .</span><span class="sxs-lookup"><span data-stu-id="b3244-105">Within the Storyboard, <xref:System.Windows.Media.Animation.DoubleAnimation> is used to animate the <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> property while <xref:System.Windows.Media.Animation.Vector3DAnimation> is used to animate the <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b3244-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b3244-106">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#Rotate3DUsingAxisAngleRotation3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotat3DUsingAxisAngleRotation3DExample.xaml#rotate3dusingaxisanglerotation3dexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="b3244-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3244-107">See also</span></span>

- [<span data-ttu-id="b3244-108">Animieren einer 3D-Drehung mit Rotation3DAnimation</span><span class="sxs-lookup"><span data-stu-id="b3244-108">Animate a 3D Rotation Using Rotation3DAnimation</span></span>](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [<span data-ttu-id="b3244-109">Animieren einer 3D-Drehung mithilfe von Keyframes (Rotation3DAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="b3244-109">Animate a 3D Rotation Using Key Frames (Rotation3DAnimationUsingKeyFrames)</span></span>](how-to-animate-a-3-d-rotation-using-key-frames.md)
- [<span data-ttu-id="b3244-110">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="b3244-110">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="b3244-111">Übersicht über Storyboards</span><span class="sxs-lookup"><span data-stu-id="b3244-111">Storyboards Overview</span></span>](storyboards-overview.md)
