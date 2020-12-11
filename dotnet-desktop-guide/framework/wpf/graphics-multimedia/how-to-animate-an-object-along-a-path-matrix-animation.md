---
title: 'Gewusst wie: Animieren eines Objekts auf einem Pfad (MatrixAnimation)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (matrix animation)
- matrix animation [WPF]
ms.assetid: 7000e697-1414-468c-b915-cf66062fc49e
ms.openlocfilehash: 7dfc233fe60e1cea293edc44a2bba79dc6962f7c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977276"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation"></a><span data-ttu-id="63ea5-102">Gewusst wie: Animieren eines Objekts auf einem Pfad (MatrixAnimation)</span><span class="sxs-lookup"><span data-stu-id="63ea5-102">How to: Animate an Object Along a Path (Matrix Animation)</span></span>
<span data-ttu-id="63ea5-103">In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> Klasse verwendet wird, um ein Objekt entlang eines durch einen definierten Pfades zu animieren <xref:System.Windows.Media.PathGeometry> .</span><span class="sxs-lookup"><span data-stu-id="63ea5-103">This example shows how to use the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> class to animate an object along a path that is defined by a <xref:System.Windows.Media.PathGeometry>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="63ea5-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="63ea5-104">Example</span></span>  
 <span data-ttu-id="63ea5-105">In diesem Beispiel wird Folgendes ausgeführt, um ein Objekt entlang eines Pfads zu animieren:</span><span class="sxs-lookup"><span data-stu-id="63ea5-105">The following example animates an object along a path by doing the following:</span></span>  
  
- <span data-ttu-id="63ea5-106">Wendet ein <xref:System.Windows.Media.MatrixTransform> auf das-Objekt an, um es zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="63ea5-106">Applies a <xref:System.Windows.Media.MatrixTransform> to the object in order to move it.</span></span>  
  
- <span data-ttu-id="63ea5-107">Definiert den Pfad mithilfe eines <xref:System.Windows.Media.PathGeometry> .</span><span class="sxs-lookup"><span data-stu-id="63ea5-107">Defines the path by using a <xref:System.Windows.Media.PathGeometry>.</span></span>  
  
- <span data-ttu-id="63ea5-108">Erstellt eine <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> und verwendet diese, um die- <xref:System.Windows.Media.Matrix> Eigenschaft des zu animieren <xref:System.Windows.Media.MatrixTransform> .</span><span class="sxs-lookup"><span data-stu-id="63ea5-108">Creates a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> and uses it to animate the <xref:System.Windows.Media.Matrix> property of the <xref:System.Windows.Media.MatrixTransform>.</span></span> <span data-ttu-id="63ea5-109">Der <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> <xref:System.Windows.Media.PathGeometry> verwendet, und verwendet ihn, um <xref:System.Windows.Media.Matrix> Werte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="63ea5-109">The <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> takes the <xref:System.Windows.Media.PathGeometry> and uses it to generate <xref:System.Windows.Media.Matrix> values.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexample.xaml#matrixanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExample.cs#matrixanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExample.vb#matrixanimationusingpathwholepage)]  
  
 <span data-ttu-id="63ea5-110">Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span><span class="sxs-lookup"><span data-stu-id="63ea5-110">For the complete sample, see [Path Animation Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span></span> <span data-ttu-id="63ea5-111">Weitere Informationen zu geometrischen Pfaden finden Sie in der [Übersicht](geometry-overview.md)über die Geometrie.</span><span class="sxs-lookup"><span data-stu-id="63ea5-111">For more information about geometric paths, see the [Geometry Overview](geometry-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63ea5-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63ea5-112">See also</span></span>

- [<span data-ttu-id="63ea5-113">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="63ea5-113">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="63ea5-114">Beispiel einer Pfadanimation</span><span class="sxs-lookup"><span data-stu-id="63ea5-114">Path Animation Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations)
- [<span data-ttu-id="63ea5-115">Gewusst-wie-Themen zur Pfadanimation</span><span class="sxs-lookup"><span data-stu-id="63ea5-115">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
