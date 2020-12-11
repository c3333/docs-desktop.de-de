---
title: 'Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
ms.assetid: cb31ca4d-f05a-4c6b-9a18-4b6faaf38d45
ms.openlocfilehash: a351fdc936f634b7c57ba5a49e51501f7572a3c9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978015"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path"></a><span data-ttu-id="4c180-102">Gewusst wie: Drehen eines Objekts mithilfe eines geometrischen Pfads</span><span class="sxs-lookup"><span data-stu-id="4c180-102">How to: Rotate an Object by Using a Geometric Path</span></span>
<span data-ttu-id="4c180-103">Dieses Beispiel zeigt, wie Sie ein Objekt entlang eines geometrischen Pfads drehen, der durch ein-Objekt definiert wird <xref:System.Windows.Media.PathGeometry> .</span><span class="sxs-lookup"><span data-stu-id="4c180-103">This example shows how to rotate (pivot) an object along a geometric path that is defined by a <xref:System.Windows.Media.PathGeometry> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4c180-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4c180-104">Example</span></span>  
 <span data-ttu-id="4c180-105">Im folgenden Beispiel werden drei- <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> Objekte verwendet, um ein Rechteck entlang eines geometrischen Pfads zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="4c180-105">The following example uses three <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objects to move a rectangle along a geometric path.</span></span>  
  
- <span data-ttu-id="4c180-106">Der erste <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animiert eine <xref:System.Windows.Media.RotateTransform> , die auf das Rechteck angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c180-106">The first <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animates a <xref:System.Windows.Media.RotateTransform> that is applied to the rectangle.</span></span> <span data-ttu-id="4c180-107">Die Animation generiert Winkelwerte.</span><span class="sxs-lookup"><span data-stu-id="4c180-107">The animation generates angle values.</span></span> <span data-ttu-id="4c180-108">Das Rechteck dreht (schwenkt) sich entlang der Pfadkonturen.</span><span class="sxs-lookup"><span data-stu-id="4c180-108">It makes the rectangle rotate (pivot) along the contours of the path.</span></span>  
  
- <span data-ttu-id="4c180-109">Die anderen beiden-Objekte animieren den <xref:System.Windows.Media.TranslateTransform.X%2A> -Wert und den- <xref:System.Windows.Media.TranslateTransform.Y%2A> Wert eines-Objekts <xref:System.Windows.Media.TranslateTransform> , das auf das Rechteck angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c180-109">The other two objects animate the <xref:System.Windows.Media.TranslateTransform.X%2A> and <xref:System.Windows.Media.TranslateTransform.Y%2A> values of a <xref:System.Windows.Media.TranslateTransform> that is applied to the rectangle.</span></span> <span data-ttu-id="4c180-110">Sie verschieben das Rechteck horizontal und vertikal entlang des Pfads.</span><span class="sxs-lookup"><span data-stu-id="4c180-110">They make the rectangle move horizontally and vertically along the path.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/rotateanimationusingpathexample.xaml#rotateanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/RotateAnimationUsingPathExample.cs#rotateanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/RotateAnimationUsingPathExample.vb#rotateanimationusingpathwholepage)]  
  
 <span data-ttu-id="4c180-111">Eine andere Möglichkeit zum Drehen eines Objekts mithilfe eines geometrischen Pfads besteht darin, ein <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> -Objekt zu verwenden und seine- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> Eigenschaft auf festzulegen `true` .</span><span class="sxs-lookup"><span data-stu-id="4c180-111">Another way to rotate an object by using a geometric path is to use a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object and set its <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> property to `true`.</span></span> <span data-ttu-id="4c180-112">Weitere Informationen und ein Beispiel finden Sie unter [Drehen eines Objekts mithilfe eines geometrischen Pfads (Matrix Animation)](how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).</span><span class="sxs-lookup"><span data-stu-id="4c180-112">For more information and an example, see [Rotate an Object by Using a Geometric Path (Matrix Animation)](how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).</span></span>  
  
 <span data-ttu-id="4c180-113">Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span><span class="sxs-lookup"><span data-stu-id="4c180-113">For the complete sample, see [Path Animation Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c180-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c180-114">See also</span></span>

- [<span data-ttu-id="4c180-115">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="4c180-115">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="4c180-116">Beispiel einer Pfadanimation</span><span class="sxs-lookup"><span data-stu-id="4c180-116">Path Animation Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations)
- [<span data-ttu-id="4c180-117">Gewusst-wie-Themen zur Pfadanimation</span><span class="sxs-lookup"><span data-stu-id="4c180-117">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
