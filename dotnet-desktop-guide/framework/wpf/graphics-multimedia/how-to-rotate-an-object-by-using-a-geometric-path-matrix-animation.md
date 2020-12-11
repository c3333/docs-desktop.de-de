---
title: 'Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads (MatrixAnimation)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
- matrix animation [WPF]
ms.assetid: 877dc9aa-6bdc-4beb-8772-3efaec32c0f0
ms.openlocfilehash: 63dc873a2b840ea3f870a8c60c5691ab271c1c9f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974860"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation"></a><span data-ttu-id="efdeb-102">Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads (MatrixAnimation)</span><span class="sxs-lookup"><span data-stu-id="efdeb-102">How to: Rotate an Object by Using a Geometric Path (Matrix Animation)</span></span>
<span data-ttu-id="efdeb-103">In diesem Beispiel wird gezeigt, wie ein <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> -Objekt und ein- <xref:System.Windows.Media.MatrixTransform> Objekt verwendet werden, um ein Objekt entlang eines durch ein-Objekt definierten geometrischen Pfads zu drehen <xref:System.Windows.Media.PathGeometry> .</span><span class="sxs-lookup"><span data-stu-id="efdeb-103">This example shows how to use a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> and a <xref:System.Windows.Media.MatrixTransform> to rotate (pivot) an object along a geometric path defined by a <xref:System.Windows.Media.PathGeometry> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="efdeb-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="efdeb-104">Example</span></span>  
 <span data-ttu-id="efdeb-105">Im folgenden Beispiel wird das- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> Objekt verwendet, um die- <xref:System.Windows.Media.MatrixTransform.Matrix%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.MatrixTransform> .</span><span class="sxs-lookup"><span data-stu-id="efdeb-105">The following example uses the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object to animate the <xref:System.Windows.Media.MatrixTransform.Matrix%2A> property of a <xref:System.Windows.Media.MatrixTransform>.</span></span> <span data-ttu-id="efdeb-106">Das <xref:System.Windows.Media.MatrixTransform> wird auf eine Schaltfläche angewendet und bewirkt, dass es sich entlang eines gekrümmten Pfads bewegt.</span><span class="sxs-lookup"><span data-stu-id="efdeb-106">The <xref:System.Windows.Media.MatrixTransform> is applied to a button and causes it to move along a curved path.</span></span> <span data-ttu-id="efdeb-107">Da die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> Eigenschaft auf festgelegt ist `true` , dreht sich das Rechteck entlang der Tangente des Pfads.</span><span class="sxs-lookup"><span data-stu-id="efdeb-107">Because the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> property is set to `true`, the rectangle rotates along the tangent of the path.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathdoesrotatewithtangentexample.xaml#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathDoesRotateWithTangentExample.cs#matrixanimationusingpathdoesrotatewithtangentwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathDoesRotateWithTangentExample.vb#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 <span data-ttu-id="efdeb-108">Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span><span class="sxs-lookup"><span data-stu-id="efdeb-108">For the complete sample, see [Path Animation Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span></span>  
  
 <span data-ttu-id="efdeb-109">In der Code Version des vorangehenden Beispiels <xref:System.Windows.Media.Animation.Storyboard> wurde verwendet, um den zu animieren <xref:System.Windows.Media.EllipseGeometry> , auch wenn nur eine Animation angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="efdeb-109">The code version of the preceding sample used a <xref:System.Windows.Media.Animation.Storyboard> to animate the <xref:System.Windows.Media.EllipseGeometry>, even though only one animation was applied.</span></span> <span data-ttu-id="efdeb-110">Eine einfachere Möglichkeit, eine einzelne Animation auf eine Eigenschaft im Code anzuwenden, ist die Verwendung der- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="efdeb-110">An easier way to apply a single animation to a property in code is to use the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method.</span></span> <span data-ttu-id="efdeb-111">Ein Beispiel finden Sie unter [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="efdeb-111">For an example, see [Animate a Property Without Using a Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efdeb-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efdeb-112">See also</span></span>

- [<span data-ttu-id="efdeb-113">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="efdeb-113">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="efdeb-114">Gewusst-wie-Themen zur Pfadanimation</span><span class="sxs-lookup"><span data-stu-id="efdeb-114">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
- [<span data-ttu-id="efdeb-115">Beispiel einer Pfadanimation</span><span class="sxs-lookup"><span data-stu-id="efdeb-115">Path Animation Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations)
