---
title: 'Gewusst wie: Drehen von Elementen ohne Positionsänderung'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], spinning elements
- spinning elements [WPF]
ms.assetid: 1f011976-8b07-4c31-9faf-019e0ddaa24c
ms.openlocfilehash: a1b515822391de08ec8ed8ff0ff1f0086874dc02
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978192"
---
# <a name="how-to-make-an-element-spin-in-place"></a><span data-ttu-id="77e7e-102">Gewusst wie: Drehen von Elementen ohne Positionsänderung</span><span class="sxs-lookup"><span data-stu-id="77e7e-102">How to: Make an Element Spin in Place</span></span>
<span data-ttu-id="77e7e-103">In diesem Beispiel wird gezeigt, wie ein Element mit einem <xref:System.Windows.Media.RotateTransform> und einem gedreht wird <xref:System.Windows.Media.Animation.DoubleAnimation> .</span><span class="sxs-lookup"><span data-stu-id="77e7e-103">This example shows how to make an element spin by using a <xref:System.Windows.Media.RotateTransform> and a <xref:System.Windows.Media.Animation.DoubleAnimation>.</span></span>  
  
 <span data-ttu-id="77e7e-104">Im folgenden Beispiel wird der <xref:System.Windows.Media.RotateTransform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft des-Elements angewendet.</span><span class="sxs-lookup"><span data-stu-id="77e7e-104">The following example applies the <xref:System.Windows.Media.RotateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of the element.</span></span> <span data-ttu-id="77e7e-105">Im Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um den von zu animieren <xref:System.Windows.Media.RotateTransform.Angle%2A> <xref:System.Windows.Media.RotateTransform> .</span><span class="sxs-lookup"><span data-stu-id="77e7e-105">The example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to animate the <xref:System.Windows.Media.RotateTransform.Angle%2A> of the <xref:System.Windows.Media.RotateTransform>.</span></span> <span data-ttu-id="77e7e-106">Damit das Element gedreht wird, wird im Beispiel die- <xref:System.Windows.UIElement.RenderTransformOrigin%2A> Eigenschaft des-Elements auf den Punkt (0,5, 0,5) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="77e7e-106">To make the element spin in place, the example sets the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property of the element to the point (0.5, 0.5).</span></span>  
  
## <a name="example"></a><span data-ttu-id="77e7e-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="77e7e-107">Example</span></span>  
 [!code-xaml[transformanimations_snip#11](~/samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/RotateAboutCenterExample.xaml#11)]  
  
 <span data-ttu-id="77e7e-108">Das komplette Beispiel, das weitere Transformations Beispiele enthält, finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span><span class="sxs-lookup"><span data-stu-id="77e7e-108">For the complete sample, which includes more transformation examples, see [2D Transforms Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77e7e-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77e7e-109">See also</span></span>

- [<span data-ttu-id="77e7e-110">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="77e7e-110">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="77e7e-111">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="77e7e-111">Transforms Overview</span></span>](transforms-overview.md)
