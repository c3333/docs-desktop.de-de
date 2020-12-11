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
# <a name="how-to-animate-a-3d-rotation-using-quaternions"></a><span data-ttu-id="e116d-102">Gewusst wie: Animieren einer 3D-Drehung mit Quaternionen</span><span class="sxs-lookup"><span data-stu-id="e116d-102">How to: Animate a 3D Rotation Using Quaternions</span></span>
<span data-ttu-id="e116d-103">Dieses Beispiel zeigt, wie Sie eine Drehung eines 3D-Objekts mit Quaternionen animieren.</span><span class="sxs-lookup"><span data-stu-id="e116d-103">This example shows how to animate a rotation of a 3D object using quaternions.</span></span>  
  
 <span data-ttu-id="e116d-104">Der folgende Code zeigt einen, der <xref:System.Windows.Media.Media3D.QuaternionRotation3D> als Wert für die- <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> Eigenschaft eines verwendet wird <xref:System.Windows.Media.Media3D.RotateTransform3D> .</span><span class="sxs-lookup"><span data-stu-id="e116d-104">The code below shows a <xref:System.Windows.Media.Media3D.QuaternionRotation3D> used as the value for the <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> property of a <xref:System.Windows.Media.Media3D.RotateTransform3D>.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline1)]  
  
 <span data-ttu-id="e116d-105">Dies <xref:System.Windows.Media.Media3D.QuaternionRotation3D> wird mit einem <xref:System.Windows.Media.Animation.QuaternionAnimation> in einem animiert, <xref:System.Windows.Media.Animation.Storyboard> das den folgenden Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="e116d-105">This <xref:System.Windows.Media.Media3D.QuaternionRotation3D> is animated with a <xref:System.Windows.Media.Animation.QuaternionAnimation> within a <xref:System.Windows.Media.Animation.Storyboard> using the code below.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline2)]  
  
## <a name="example"></a><span data-ttu-id="e116d-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e116d-106">Example</span></span>  
 <span data-ttu-id="e116d-107">Der folgende Code zeigt das gesamte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e116d-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="e116d-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e116d-108">See also</span></span>

- [<span data-ttu-id="e116d-109">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="e116d-109">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="e116d-110">Erstellen einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="e116d-110">Create a 3D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="e116d-111">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="e116d-111">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="e116d-112">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="e116d-112">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="e116d-113">Animieren einer 3D-Drehung mit Storyboards</span><span class="sxs-lookup"><span data-stu-id="e116d-113">Animate a 3D Rotation Using Storyboards</span></span>](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [<span data-ttu-id="e116d-114">Animieren einer 3D-Drehung mit Rotation3DAnimation</span><span class="sxs-lookup"><span data-stu-id="e116d-114">Animate a 3D Rotation Using Rotation3DAnimation</span></span>](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
