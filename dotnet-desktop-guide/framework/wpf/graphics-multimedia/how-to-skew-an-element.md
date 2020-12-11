---
title: 'Gewusst wie: Neigen eines Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- skewing elements [WPF]
- graphics [WPF], skewing elements
- classes [WPF], SkewTransform
ms.assetid: 56b65f2f-dc6e-4238-923f-ca44ec53c52f
ms.openlocfilehash: 10b00044c1c518641281e2e72cdb5a68474b5170
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975472"
---
# <a name="how-to-skew-an-element"></a><span data-ttu-id="90366-102">Gewusst wie: Neigen eines Elements</span><span class="sxs-lookup"><span data-stu-id="90366-102">How to: Skew an Element</span></span>
<span data-ttu-id="90366-103">In diesem Beispiel wird gezeigt, wie ein-Element mit einem <xref:System.Windows.Media.SkewTransform> verzerrt wird.</span><span class="sxs-lookup"><span data-stu-id="90366-103">This example shows how to use a <xref:System.Windows.Media.SkewTransform> to skew an element.</span></span> <span data-ttu-id="90366-104">Eine Neigung ist eine Transformation, die den Koordinatenraum auf ungleichmäßige Art ausdehnt.</span><span class="sxs-lookup"><span data-stu-id="90366-104">A skew, which is also known as a shear, is a transformation that stretches the coordinate space in a non-uniform manner.</span></span> <span data-ttu-id="90366-105">Eine typische Verwendung eines <xref:System.Windows.Media.SkewTransform> ist das Simulieren der 3D-Tiefe in 2D-Objekten.</span><span class="sxs-lookup"><span data-stu-id="90366-105">One typical use of a <xref:System.Windows.Media.SkewTransform> is for simulating 3D depth in 2D objects.</span></span>  
  
 <span data-ttu-id="90366-106">Verwenden <xref:System.Windows.Media.SkewTransform.CenterX%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.SkewTransform.CenterY%2A> , um den Mittelpunkt von anzugeben <xref:System.Windows.Media.SkewTransform> .</span><span class="sxs-lookup"><span data-stu-id="90366-106">Use the <xref:System.Windows.Media.SkewTransform.CenterX%2A> and <xref:System.Windows.Media.SkewTransform.CenterY%2A> properties to specify the center point of the <xref:System.Windows.Media.SkewTransform>.</span></span>  
  
 <span data-ttu-id="90366-107">Verwenden Sie die-Eigenschaft und die-Eigenschaft, <xref:System.Windows.Media.SkewTransform.AngleX%2A> <xref:System.Windows.Media.SkewTransform.AngleY%2A> um den Neigungswinkel der x-Achse und der y-Achse anzugeben und um das aktuelle Koordinatensystem entlang dieser Achsen zu neigen.</span><span class="sxs-lookup"><span data-stu-id="90366-107">Use the <xref:System.Windows.Media.SkewTransform.AngleX%2A> and <xref:System.Windows.Media.SkewTransform.AngleY%2A> properties to specify the skew angle of the x-axis and y-axis, and to skew the current coordinate system along these axes.</span></span>  
  
 <span data-ttu-id="90366-108">Um die Auswirkung einer Schiefe-Transformation vorherzusagen, sollten Sie die <xref:System.Windows.Media.SkewTransform.AngleX%2A> x-Achsen Werte relativ zum ursprünglichen Koordinatensystem neigen.</span><span class="sxs-lookup"><span data-stu-id="90366-108">To predict the effect of a skew transformation, consider that <xref:System.Windows.Media.SkewTransform.AngleX%2A> skews x-axis values relative to the original coordinate system.</span></span> <span data-ttu-id="90366-109">Daher wird <xref:System.Windows.Media.SkewTransform.AngleX%2A> die y-Achse für eine von 30 um 30 Grad über den Ursprung rotiert und die Werte in x-um 30 Grad von diesem Ursprung entfernt.</span><span class="sxs-lookup"><span data-stu-id="90366-109">Therefore, for an <xref:System.Windows.Media.SkewTransform.AngleX%2A> of 30, the y-axis rotates 30 degrees through the origin and skews the values in x- by 30 degrees from that origin.</span></span> <span data-ttu-id="90366-110">Ebenso wird <xref:System.Windows.Media.SkewTransform.AngleY%2A> die y-Werte der Form durch eine von 30 um 30 Grad vom Ursprung entfernt.</span><span class="sxs-lookup"><span data-stu-id="90366-110">Likewise, an <xref:System.Windows.Media.SkewTransform.AngleY%2A> of 30 skews the y- values of the shape by 30 degrees from the origin.</span></span> <span data-ttu-id="90366-111">Beachten Sie, dass dieser Vorgang nicht dieselbe Wirkung erzielt, wie das Übersetzen (Bewegen) des Koordinatensystems um 30° in der X- oder Y-Achse.</span><span class="sxs-lookup"><span data-stu-id="90366-111">Note that this is not the same effect as translating (moving) the coordinate system by 30 degrees in x- or y-.</span></span>  
  
 <span data-ttu-id="90366-112">Im folgenden Beispiel wird eine horizontale Neigung von 45 Grad auf ein <xref:System.Windows.Shapes.Rectangle> von einem Mittelpunkt von (0,0) angewendet.</span><span class="sxs-lookup"><span data-stu-id="90366-112">The following example applies a horizontal skew of 45 degrees to a <xref:System.Windows.Shapes.Rectangle> from a center point of (0,0).</span></span>  
  
## <a name="example"></a><span data-ttu-id="90366-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="90366-113">Example</span></span>  
 [!code-xaml[transformsSample#41](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/SkewTransformExample.xaml#41)]  
  
 <span data-ttu-id="90366-114">Im folgenden Beispiel wird eine horizontale Neigung von 45 Grad auf ein <xref:System.Windows.Shapes.Rectangle> von einem Mittelpunkt von (25, 25) angewendet.</span><span class="sxs-lookup"><span data-stu-id="90366-114">The following example applies a horizontal skew of 45 degrees to a <xref:System.Windows.Shapes.Rectangle> from a center point of (25,25).</span></span>  
  
 [!code-xaml[transformsSample#42](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/SkewTransformExample.xaml#42)]  
  
 <span data-ttu-id="90366-115">Im folgenden Beispiel wird eine vertikale Neigung von 45 Grad auf ein <xref:System.Windows.Shapes.Rectangle> von einem Mittelpunkt von (25, 25) angewendet.</span><span class="sxs-lookup"><span data-stu-id="90366-115">The following example applies a vertical skew of 45 degrees to a <xref:System.Windows.Shapes.Rectangle> from a center point of (25,25).</span></span>  
  
 [!code-xaml[transformsSample#43](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/SkewTransformExample.xaml#43)]  
  
 <span data-ttu-id="90366-116">Die folgenden Abbildungen zeigen die verschiedenen Neigungen, die in diesem Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90366-116">The following illustration shows the different skews that are used in this example.</span></span>  
  
 <span data-ttu-id="90366-117">![SkewTransform-Beispiele](./media/img-wcpsdk-graphicsmm-skewtransformexample.gif "img_wcpsdk_graphicsmm_skewtransformexample")</span><span class="sxs-lookup"><span data-stu-id="90366-117">![SkewTransform examples](./media/img-wcpsdk-graphicsmm-skewtransformexample.gif "img_wcpsdk_graphicsmm_skewtransformexample")</span></span>  
<span data-ttu-id="90366-118">Die drei SkewTransform-Beispiele veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="90366-118">The three SkewTransform examples illustrated</span></span>  
  
 <span data-ttu-id="90366-119">Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span><span class="sxs-lookup"><span data-stu-id="90366-119">For the complete sample, see [2D Transforms Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90366-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90366-120">See also</span></span>

- <xref:System.Windows.Media.Transform>
- <xref:System.Windows.Media.SkewTransform>
- [<span data-ttu-id="90366-121">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="90366-121">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="90366-122">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="90366-122">How-to Topics</span></span>](transformations-how-to-topics.md)
