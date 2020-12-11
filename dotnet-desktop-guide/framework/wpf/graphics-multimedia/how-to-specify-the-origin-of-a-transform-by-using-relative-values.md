---
title: 'Gewusst wie: Angeben des Ursprungs einer Transformation mithilfe von relativen Werten'
ms.date: 03/30/2017
helpviewer_keywords:
- origins of Transforms [WPF]
- Transforms [WPF], origins of
- graphics [WPF], origins of Transforms
ms.assetid: f4dbc29d-93c7-41cd-96d8-5cfd8624b470
ms.openlocfilehash: 48b3b0df8dab8516873495a996074eae57ffe00f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975467"
---
# <a name="how-to-specify-the-origin-of-a-transform-by-using-relative-values"></a><span data-ttu-id="5dd2f-102">Gewusst wie: Angeben des Ursprungs einer Transformation mithilfe von relativen Werten</span><span class="sxs-lookup"><span data-stu-id="5dd2f-102">How to: Specify the Origin of a Transform by Using Relative Values</span></span>
<span data-ttu-id="5dd2f-103">In diesem Beispiel wird gezeigt, wie relative Werte verwendet werden, um den Ursprung eines-Werts anzugeben <xref:System.Windows.UIElement.RenderTransform%2A> , der auf ein angewendet wird <xref:System.Windows.FrameworkElement> .</span><span class="sxs-lookup"><span data-stu-id="5dd2f-103">This example shows how to use relative values to specify the origin of a <xref:System.Windows.UIElement.RenderTransform%2A> that is applied to a <xref:System.Windows.FrameworkElement>.</span></span>  
  
 <span data-ttu-id="5dd2f-104">Wenn Sie ein mithilfe der-Eigenschaft drehen, skalieren oder neigen <xref:System.Windows.FrameworkElement> <xref:System.Windows.UIElement.RenderTransform%2A> , wird die Transformation von der Standardeinstellung auf die linke obere Ecke des Elements angewendet.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-104">When you rotate, scale, or skew a <xref:System.Windows.FrameworkElement> by using the <xref:System.Windows.UIElement.RenderTransform%2A> property, the default setting applies the transform to the upper-left corner of the element.</span></span> <span data-ttu-id="5dd2f-105">Wenn Sie von der Mitte des Elements aus drehen, skalieren oder neigen möchten, können Sie dies ändern, indem Sie für den Mittelpunkt der Transformation den Mittelpunkt des Elements festlegen.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-105">If you want to rotate, scale, or skew from the center of the element, you can compensate by setting the center of the transform to the center of the element.</span></span> <span data-ttu-id="5dd2f-106">Für diese Lösung müssen Sie jedoch die Größe des Elements kennen.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-106">However, that solution requires that you know the size of the element.</span></span> <span data-ttu-id="5dd2f-107">Eine einfachere Möglichkeit, eine Transformation auf den Mittelpunkt eines Elements anzuwenden, besteht darin, die zugehörige- <xref:System.Windows.UIElement.RenderTransformOrigin%2A> Eigenschaft auf (0,5, 0,5) festzulegen, anstatt einen Mittelwert für die Transformation selbst festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-107">An easier way of applying a transform to the center of an element is to set its <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property to (0.5, 0.5), instead of setting a center value on the transform itself.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5dd2f-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5dd2f-108">Example</span></span>  
 <span data-ttu-id="5dd2f-109">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.RotateTransform> , um <xref:System.Windows.Controls.Button> 45 Grad im Uhrzeigersinn zu drehen.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-109">The following example uses a <xref:System.Windows.Media.RotateTransform> to rotate a <xref:System.Windows.Controls.Button> 45 degrees clockwise.</span></span> <span data-ttu-id="5dd2f-110">Da in dem Beispiel kein Mittelpunkt angegeben ist, dreht sich die Schaltfläche um den Punkt (0, 0), die obere linke Ecke.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-110">Because the example does not specify a center, the button rotates about the point (0, 0), which is its upper-left corner.</span></span> <span data-ttu-id="5dd2f-111">Der <xref:System.Windows.Media.RotateTransform> wird auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft angewendet.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-111">The <xref:System.Windows.Media.RotateTransform> is applied to the <xref:System.Windows.UIElement.RenderTransform%2A> property.</span></span>  
  
 <span data-ttu-id="5dd2f-112">In der folgenden Abbildung wird das Transformationsergebnis für das folgende Beispiel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-112">The following illustration shows the transformation result for the example that follows.</span></span>  
  
 <span data-ttu-id="5dd2f-113">![Eine mit RenderTransform transformierte Schaltfläche](./media/graphicsmm-rendertransformwithdefaultcenter.png "graphicsmm_RenderTransformWithDefaultCenter")</span><span class="sxs-lookup"><span data-stu-id="5dd2f-113">![A button transformed using RenderTransform](./media/graphicsmm-rendertransformwithdefaultcenter.png "graphicsmm_RenderTransformWithDefaultCenter")</span></span>  
<span data-ttu-id="5dd2f-114">Eine Drehung um 45 Grad im Uhrzeigersinn unter Verwendung der RenderTransform-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5dd2f-114">A 45 degree clockwise rotation by using the RenderTransform property</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample1)]  
  
 <span data-ttu-id="5dd2f-115">Im folgenden Beispiel wird auch ein-Wert verwendet <xref:System.Windows.Media.RotateTransform> , um <xref:System.Windows.Controls.Button> 45 Grad im Uhrzeigersinn zu drehen. in diesem Beispiel wird jedoch der <xref:System.Windows.UIElement.RenderTransformOrigin%2A> der Schaltfläche auf (0,5, 0,5) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-115">The following example also uses a <xref:System.Windows.Media.RotateTransform> to rotate a <xref:System.Windows.Controls.Button> 45 degrees clockwise; however, this example sets the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> of the button to (0.5, 0.5).</span></span> <span data-ttu-id="5dd2f-116">Dadurch erfolgt die Drehung um den Mittelpunkt der Schaltfläche, nicht um die obere linke Ecke.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-116">As a result, the rotation is applied to the center of the button instead of to the upper-left corner.</span></span>  
  
 <span data-ttu-id="5dd2f-117">In der folgenden Abbildung wird das Transformationsergebnis für das folgende Beispiel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-117">The following illustration shows the transformation result for the example that follows.</span></span>  
  
 <span data-ttu-id="5dd2f-118">![Eine um ihren Mittelpunkt transformierte Schaltfläche](./media/graphicsmm-rendertransformrelativecenter.png "graphicsmm_RenderTransformRelativeCenter")</span><span class="sxs-lookup"><span data-stu-id="5dd2f-118">![A button transformed about its center](./media/graphicsmm-rendertransformrelativecenter.png "graphicsmm_RenderTransformRelativeCenter")</span></span>  
<span data-ttu-id="5dd2f-119">Eine Drehung um 45 Grad unter Verwendung der RenderTransform-Eigenschaft mit einem RenderTransformOrigin von (0.5, 0.5)</span><span class="sxs-lookup"><span data-stu-id="5dd2f-119">A 45 degree rotation by using the RenderTransform property with a RenderTransformOrigin of (0.5, 0.5)</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample2)]  
  
 <span data-ttu-id="5dd2f-120">Weitere Informationen zum Transformieren von <xref:System.Windows.FrameworkElement> Objekten finden Sie in der [Übersicht über Transformationen](transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5dd2f-120">For more information about transforming <xref:System.Windows.FrameworkElement> objects, see the [Transforms Overview](transforms-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5dd2f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd2f-121">See also</span></span>

- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="5dd2f-122">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="5dd2f-122">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="5dd2f-123">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="5dd2f-123">How-to Topics</span></span>](transformations-how-to-topics.md)
